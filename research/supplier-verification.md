# Supplier verification and failure handling (Q8, Q9)
_Last checked: 2026-11-09_

## Summary

- **You cannot verify hardware yourself, and you do not need to.** Your job is to run a fixed process: company checks, a paid or free test window, a short list of standard commands the buyer's engineer runs, two reference calls, and written warranties. Never vouch for hardware you have not seen tested.
- **The cheapest strong check is a 24–72 hour test on the actual machines** before the buyer commits. Three tools cover most of it: `nvidia-smi` (what the GPU says it is), NVIDIA's `dcgmi diag` (hardware health, minutes to two hours), and a real workload or `gpu-burn` stress run [1][2][3].
- **Software-reported names can be faked.** Cross-check GPU name against memory size, serial numbers, and measured performance. Counterfeiters have physically re-etched cheaper chips to look like expensive ones well enough to fool repair technicians [9][10].
- **Independent signals exist.** NVIDIA publishes its Cloud Partner list [4], and SemiAnalysis's ClusterMAX (version 3.0, September 2026) rates GPU clouds on audit, performance, reliability and fault-tolerance testing [5]. A supplier on neither list is not bad, but needs the full checklist.
- **Documented fraud is real but the public record is uneven.** Well-sourced: relabeled H100/H200 units in a $160M US smuggling case [7][8]; counterfeit consumer cards [9][10][11]. Your earlier note about "A30s sold as A100s" – **I could not find a source for it (unverified).**
- **Standard supplier terms protect the supplier, not the buyer.** Example: RunPod's public terms give no uptime commitment, "as-is" service, and cap liability at $100 [6]. A rated EU provider was found charging customers during outages with no written SLA until called out [12]. Negotiate SLA, credits and exit rights **before** signing, in the order form.
- **Your protection as broker is structural:** you are not the provider and do not hold the buyer's money; the buyer contracts directly with the supplier; you document what you checked and what you did not; you keep a pre-screened backup supplier for every deal.
- **Recommendation:** adopt the one-page checklist at the end as a hard gate. No completed checklist, no introduction.

> **Research limits.** The shared web-search budget ran out during this work, so fraud examples and SLA norms are thinner than planned. Items marked (unverified) are from general industry knowledge and need a source before you repeat them to a buyer.

## Details

### Q8. How do I verify a supplier is real and the hardware is as described?

Work in four layers. Stop at the first layer that fails.

#### Layer 1 – Is the company real? (you, 1–2 hours, free)

| Check | How | Fail signal |
|---|---|---|
| Legal entity exists | Official company register of the country where it says it is incorporated; ask for registration number and registered address | No number, name mismatch, dissolved or newly reactivated shell. In the $160M smuggling case the front company had been dormant since 2014 and suddenly became active in high-end hardware [8] |
| Who owns and runs it | Ask for directors and owners above 25%; screen every name and the company on sanctions lists (see `/compliance/`) | Refusal; nominee-only structures; owners in sanctioned or embargoed jurisdictions |
| Where the hardware physically is | Data-centre operator name, city, and whether the supplier owns the GPUs, leases them, or resells someone else's | "Confidential"; location changes between calls; location in a high-risk jurisdiction |
| NVIDIA relationship | Is it on NVIDIA's Cloud Partner list [4]? If it claims "NVIDIA partner", ask which program and check NVIDIA's own listing | Claims a status NVIDIA does not list |
| Independent rating | Is it reviewed in ClusterMAX [5]? Read the review – they name specific weaknesses (see the Verda example [12]) | Not a failure on its own; most small suppliers are unrated |
| Footprint | Named customers, public status page, documentation, real staff on LinkedIn, age of domain | Stock photos, no documentation, no named engineers |
| Bank details | Account name matches the legal entity and country | Payment to a different company, a personal account, or crypto only |

#### Layer 2 – Test access before commitment

Ask for a **proof-of-concept window on the exact machines being sold** (not "similar" ones): typically 24–72 hours, free or at list price credited against the contract. A supplier that refuses any test for a multi-month deal is a no.

You do not run the tests. The buyer's engineer does, or a freelance ML engineer you pay for an hour. You make sure they happen and keep the output files.

#### Layer 3 – What to run (copy-paste list for the buyer's engineer)

| What it answers | Command / tool | What to look for |
|---|---|---|
| What does each GPU say it is? | `nvidia-smi` and `nvidia-smi -q` ; or `nvidia-smi --query-gpu=index,name,serial,uuid,memory.total,vbios_version,driver_version --format=csv` (exact field names: `nvidia-smi --help-query-gpu`) [1] | Model name, **memory size**, serial and UUID for every GPU; count matches the quote |
| Is the hardware healthy? | `nvidia-smi -q` error counters; `nvidia-smi --query-retired-pages=...`; `--query-remapped-rows=...` [1] | Lifetime ("aggregate") ECC errors, retired pages, remapped rows – signs of worn or ex-mining hardware |
| Vendor diagnostic | `dcgmi diag -r 3` (about 10–35 minutes on a 4–8 GPU Hopper server); `-r 4` for the longest test (up to about 2.25 hours on 8 GPUs) [2] | Any "Fail" on memory, PCIe, NVLink, power or thermal tests. Save JSON with `-j` |
| Does it hold under load? | `gpu-burn` for 1 hour: `docker run --rm --gpus all gpu-burn ./gpu_burn -m 50% 3600` [3] | Errors, throttling, a GPU dropping out |
| Does it perform like the real model? | Run the buyer's own training or inference job for a few hours and compare throughput with a known-good reference (the buyer's previous provider, or published MLPerf results for that GPU – unverified here) | More than roughly 10–15% below reference needs an explanation (unverified rule of thumb) |
| Cluster networking | `ibstat` (InfiniBand present and at the promised speed); `nvidia-smi topo -m`; a multi-node NCCL or training test (unverified here – standard tools) | "InfiniBand" quoted but Ethernet delivered; slow multi-node scaling |
| Storage and internet | `fio` on the shared filesystem; `iperf3` or a large download (unverified here – standard tools) | Throughput far below what the buyer's data pipeline needs |

**Why memory size matters.** The reported name can be spoofed by a hypervisor or modified firmware, but memory and performance are harder to fake together. From general knowledge (confirm against NVIDIA data sheets): A30 = 24 GB, A100 = 40 or 80 GB, H100 = 80 GB, H200 = 141 GB. A "GPU" that reports the right name but the wrong memory, or the right memory but half the throughput, is not what was sold. Also ask whether the buyer gets **bare metal or a virtual machine** – on a VM, some identity fields are hidden and the supplier controls what is reported.

**Serial numbers.** Ask the supplier for the server serial numbers and OEM (Dell, Supermicro, HPE, etc.). The buyer can ask the OEM or NVIDIA support to confirm that the serials are genuine and under warranty (process unverified – confirm with the OEM).

#### Layer 4 – References, site visits, contract warranties

- **References.** Two current customers running a similar size and workload. Ask them: Was delivery on time? How many outages? How fast is support? Were you ever billed during downtime? Would you renew?
- **Site visits.** Not affordable on your budget and rarely needed for established clouds. For an unknown regional supplier and a large deal, ask the **buyer** to visit, or accept a live video walk-through showing rack labels and server serial tags that match the `nvidia-smi` output. Balkan sites are the one case where you can go yourself cheaply.
- **Contract warranties (in the supplier–buyer contract; lawyer to draft).** The supplier warrants that: hardware is genuine and matches the stated model, count, memory, interconnect and location; it holds title or the right to provide it; the buyer may run acceptance tests in the first N days and cancel with a full refund if they fail; hardware is not subject to sanctions or export-control violations; and the location will not change without consent.

### Known fraud patterns

| Pattern | Sourced example | How the checklist catches it |
|---|---|---|
| **Relabeling of genuine high-end GPUs** to hide what they are | US Department of Justice, December 2025: in a scheme to export at least $160M of H100/H200 GPUs, workers allegedly removed NVIDIA labels and applied labels of a fake company, "SANDKYAN", and paperwork described the goods as generic computer parts. One defendant and his company pleaded guilty; two others were charged (allegations for those two) [7][8] | This is an export-control case, not a quality scam – but it shows labels and paperwork prove nothing. Check serials and ownership; treat odd provenance as a compliance red flag and walk away |
| **Counterfeit or re-marked cards** (cheaper chip dressed as an expensive one) | Repair shops found "RTX 4090" cards built on re-etched older chips with counterfeit memory, passing visual checks [9][10]; Chinese police arrested 22 people for refurbishing used mining cards as new [11] | Memory size + performance test + serial check with the OEM. Mainly a risk when buying physical hardware or renting from very small hosts |
| **Spoofed GPUs on marketplaces** (machine reports a GPU it does not have) | Decentralised marketplaces run recurring proof-of-work checks on hosts for this reason [13]. I recall a 2024 incident in which a marketplace reported a large number of fake GPU listings, but could not re-source it (unverified) | Never broker marketplace hosts without a workload test; prefer "datacenter-verified" hosts |
| **Capacity that does not exist yet** ("available next month") | No sourced case found in this session (unverified). Risk is highest with new builders, converting crypto miners, and announced-but-unbuilt campuses | Test access on the actual machines; no prepayment before acceptance; delivery date with a cancellation right |
| **Mislabeled model sold at a higher price** (your note: A30 sold as A100) | **No source found (unverified)** | `nvidia-smi` memory check takes 10 seconds |
| **Bait and switch after signing** (tested on good nodes, delivered others) | No sourced case found (unverified) | Serial numbers written into the order form; re-run `nvidia-smi` on day one |
| **Fake supplier / advance-fee** (broker-of-a-broker with no hardware) | No sourced case found (unverified) | Layer 1 checks; direct contract between buyer and the entity that owns or operates the hardware |

### Q9. What happens when a supplier fails to deliver or hardware underperforms?

#### What standard terms give the buyer (usually little)

- RunPod's public Terms of Service: service is "as-is and as-available", no uptime warranty for community cloud, fees non-refundable, and liability capped at the lesser of six months' fees or **$100** [6].
- SemiAnalysis found that Verda (DataCrunch), a rated Finnish provider, had "no written SLA with penalties" at the time of testing and charged customers for GPU time during outages; after publication Verda committed to credit at least 2x instance cost for downtime [12].
- Typical enterprise SLAs give service credits (a percentage of the monthly fee) as the **only** remedy, with no compensation for lost training time (general knowledge – unverified for specific providers).

So the protection has to be negotiated in the order form for any reserved deal.

#### What to negotiate for the buyer (before signing)

| Term | What to ask for |
|---|---|
| Acceptance test | N days after hand-over to run the Layer 3 tests; full refund and cancellation if they fail |
| Delivery date | A firm date; daily credits for delay; right to cancel with refund after X days late |
| Uptime SLA | A stated percentage per node and for the cluster network; credits that scale with downtime; no billing during outages |
| Hardware replacement | Failed GPU or node replaced within a stated time, or billing stops for it |
| Termination for cause | Right to exit after repeated SLA misses, with prepaid amounts refunded pro rata |
| Prepayment | Monthly in arrears or monthly in advance, not 6–12 months up front. If the supplier insists on a large prepayment, stage it against milestones or use a licensed third-party escrow (lawyer to advise; I did not verify any escrow provider) |
| Data exit | Time and bandwidth to copy data out at the end or on termination |
| No substitution | Model, count, interconnect and location fixed; changes need written consent |

#### How you protect the buyer and your own reputation

1. **Stay out of the contract chain.** Buyer contracts and pays the supplier directly. You are paid by the supplier (commission) and/or the buyer (disclosed fee). You never hold buyer funds. This is what makes you a broker and not a reseller with the reseller's liability.
2. **Say exactly what you did.** Give the buyer a one-page "supplier check summary": what you checked, what the buyer's engineer tested, what was not checked. Never write "verified" or "guaranteed". Your service agreement should state that you do not operate the hardware and do not warrant supplier performance (see `/legal/`).
3. **Always have a backup.** For every deal, name a second pre-screened supplier that could take the workload. Tell the buyer who it is. When something breaks, moving the buyer within days is the single thing that saves the relationship.
4. **Run the incident.** When a supplier misses: log dates and evidence, get the supplier's account manager and the buyer's engineer on one thread, help the buyer file the SLA claim within the contract's deadline, and escalate to the backup if a fix is not in sight within an agreed time.
5. **Put your money where the failure is.** Offer to waive or refund your own buyer-side fee for the affected period. It is small money and it is the only compensation fully in your control. Expect the supplier agreement to claw back commission on refunded revenue anyway.
6. **Keep a supplier scorecard.** Delivery on time, incidents, support response, billing accuracy. Drop suppliers that fail twice. Record it in `suppliers.csv` notes.
7. **Insurance.** Professional liability (errors and omissions) cover is worth pricing once you have revenue; it is probably outside the first-six-months budget (cost unverified).

**What you should not do:** promise an SLA in your own name, pay credits out of pocket beyond your fee, take prepayments, or quietly switch a buyer to another supplier without their written agreement.

**Recommendation for Q9:** for on-demand deals accept standard terms and rely on the test window and backup supplier. For any reserved deal over about three months, make acceptance testing, delay credits and termination-for-cause a condition of your introduction.

## One-page supplier due-diligence checklist

Copy for each supplier and each deal. All boxes in A–C must be ticked before introducing a buyer; D before the buyer signs.

**Supplier:** ____________  **Deal:** ____________  **Date:** ____________  **Checked by:** ____________

**A. Company (you)**
- [ ] Legal name, registration number and address confirmed in the official register
- [ ] Directors and owners (25%+) named; company and each person screened against sanctions and restricted-party lists; screenshot saved
- [ ] Not dormant-then-suddenly-active; trading history and real staff visible
- [ ] Bank account name and country match the legal entity; no crypto-only or third-party payee
- [ ] NVIDIA Cloud Partner list checked (yes / no / claimed but not listed)
- [ ] ClusterMAX or other independent review read (rating: ______ / none)

**B. Capacity (you, in writing from supplier)**
- [ ] GPU model, count, memory per GPU, CPU, RAM, storage, interconnect (InfiniBand / Ethernet speed)
- [ ] Bare metal or virtual machine
- [ ] Data-centre operator, city, country; jurisdiction acceptable under compliance policy
- [ ] Supplier owns / leases / resells the hardware (if reselling: from whom, and is resale permitted)
- [ ] Available now on the actual machines, or delivery date: ______
- [ ] Price, term, payment schedule, SLA document received

**C. References**
- [ ] Reference 1 called (similar size/workload): on-time delivery, outages, support, billing
- [ ] Reference 2 called
- [ ] Search for complaints, lawsuits, insolvency news

**D. Technical test (buyer's engineer; you collect the output files)**
- [ ] Test window on the actual machines: ______ hours
- [ ] `nvidia-smi` output saved: model, count, memory and serials match the quote
- [ ] Error counters / retired pages / remapped rows reviewed
- [ ] `dcgmi diag -r 3` (or `-r 4`) passed; JSON saved
- [ ] 1-hour stress run (`gpu-burn`) with no errors
- [ ] Buyer's own workload run; throughput acceptable to buyer
- [ ] Multi-node network and storage tested (clusters only)
- [ ] Server serial numbers recorded for the order form

**E. Contract (buyer and supplier; lawyer-reviewed for large deals)**
- [ ] Buyer contracts directly with supplier; you hold no funds
- [ ] Hardware warranty (genuine, as specified, location fixed, no substitution)
- [ ] Acceptance period with refund right
- [ ] Delivery date with delay credits and cancellation right
- [ ] Uptime SLA, credits, no billing during outages
- [ ] Termination for cause with pro-rata refund of prepayments
- [ ] Prepayment limited or staged / escrowed

**F. Your file**
- [ ] Backup supplier named and disclosed to buyer: ____________
- [ ] Supplier check summary sent to buyer (what was and was not checked)
- [ ] Commission and any buyer fee disclosed to buyer in writing
- [ ] Deal registered with supplier; confirmation saved

**Decision:** proceed / proceed with conditions / refuse. **Reason:** ____________

## Questions for a lawyer / accountant

1. Wording for my buyer agreement so that my supplier checks are "reasonable efforts" and not a warranty or guarantee of supplier performance.
2. Could I be liable for negligent misrepresentation if I pass on a supplier's hardware claims that turn out false? What disclaimer and record-keeping reduce that risk?
3. If a supplier's hardware has a suspicious origin (relabeled, no serials), what are my obligations under US export-control law, and should I report it?
4. Is recommending or arranging escrow something I can do without holding funds or needing a licence? Which escrow providers are properly licensed?
5. A short acceptance-test and delay-credit clause set I can hand to buyers as a negotiating template without it being legal advice.
6. Cost and usefulness of professional liability (E&O) insurance for a foreign-owned single-member US LLC.

## Sources

All checked 2026-11-09. "Search summary" means the page was read through a search-engine result because it could not be opened directly.

1. NVIDIA – nvidia-smi documentation, https://docs.nvidia.com/deploy/nvidia-smi/index.html
2. NVIDIA – DCGM Diagnostics user guide, https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-diagnostics.html
3. gpu-burn – Multi-GPU CUDA stress test, https://github.com/wilicc/gpu-burn
4. NVIDIA – Cloud Partners list, https://www.nvidia.com/en-us/data-center/gpu-cloud-computing/partners.md
5. SemiAnalysis – ClusterMAX (version 3.0, September 2026), https://clustermax.semianalysis.com/
6. RunPod – Terms of Service, https://www.runpod.io/legal/terms-of-service
7. US Department of Justice – "U.S. Authorities Shut Down Major China-Linked AI Tech Smuggling Network" (8 Dec 2025), https://www.justice.gov/opa/pr/us-authorities-shut-down-major-china-linked-ai-tech-smuggling-network
8. Introl – Operation Gatekeeper summary (trade blog; use DOJ release as primary), https://introl.com/blog/nvidia-160m-smuggling-prosecution-operation-gatekeeper-december-2025
9. Tom's Hardware forum thread on relabeled RTX 3080 Ti sold as RTX 4090, https://forums.tomshardware.com/threads/scam-nvidia-rtx-4090-uses-a-relabeled-rtx-3080-ti-gpu-counterfeit-memory-chips-%E2%80%94-repair-shop-exposes-troubling-new-swindle-thats-impossible-to-sp.3848712 (search summary; direct read blocked)
10. Guru3D – RTX 4090 counterfeit with laser etching and dummy silicon, https://www.guru3d.com/story/rtx-4090-counterfeit-uses-laser-etching-and-dummy-silicon-to-evade-detection/ (search summary)
11. 80.lv – 22 GPU counterfeiters arrested in China, https://80.lv/articles/22-gpu-counterfeiters-arrested-in-china (search summary)
12. SemiAnalysis ClusterMAX – Verda/DataCrunch review (ClusterMAX 2.0, Nov 2025), https://clustermax.semianalysis.com/cloudreview/verdadatacrunch
13. DEV Community – commentary on io.net's hourly proof-of-work host verification, https://dev.to/aicryptosystems/depin-gpu-market-the-reliability-score-is-not-the-model-answer-4e78 (search summary; secondary source)
