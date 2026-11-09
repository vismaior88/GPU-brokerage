# AI-chip diversion and enforcement cases, 2023–2026: lessons for a broker
_Last checked: 2026-11-09_

> Purpose: recognise the patterns so you can refuse the deal. Charges described as "alleged" are unproven; defendants are presumed innocent. Nothing here describes how to evade controls.

## Summary

- **Every US criminal case found involves physical hardware** (GPUs or servers) routed to China through a third country with false paperwork. I found **no US prosecution to date of anyone for renting or brokering cloud access** — consistent with remote access not yet being an "export" (see `export-controls.md`).
- **The defendants look like you would look to a prosecutor:** small US companies, often one-person LLCs or resellers, acting as middlemen. Individuals were charged personally in every case [1][2][3][4][5].
- **Recurring routes:** Malaysia, Singapore, Thailand, Hong Kong, Taiwan; the UAE and other hubs appear in BIS guidance and reporting [1][3][4][6].
- **Recurring red flags:** newly formed company; buyer with no AI/data-centre history; stated end user absent from the conversation; payer different from customer; money arriving from China/Hong Kong; freight forwarder or virtual office as consignee; relabelling; a data centre that cannot be shown to exist.
- **Cloud rental by Chinese firms is the live policy fight.** The White House said (July 2026) that Moonshot AI used Blackwell chips in Thailand; CNBC reported (5 Nov 2026) it then sought 8,000+ Blackwell GPUs from European neoclouds, offering 30–50% more upfront than other customers [7]. Singapore-based neocloud Megaspeed is under US and Singapore investigation; no charges, and it denies wrongdoing [8][9].
- **Suppliers do catch this.** In the March 2026 Thai case, the server maker noticed a China-based company on the email thread and the chip maker could not verify the Thai buyer; the order was not completed and three people were charged anyway [5].
- **Recommendation:** treat any buyer who pays a premium, is in a hurry, hides the end user, or is a new entity in a Southeast Asian or Gulf hub as a refusal by default. Treat any supplier in those hubs with unexplained hardware as a refusal too.

## Details

### A. US criminal cases (hardware diversion)

| Case | What happened (as alleged or admitted) | Who | Red flags present |
|---|---|---|---|
| **ALX Solutions** (C.D. Cal., charged Aug 2025) [2][10] | GPUs shipped via freight forwarders in Singapore and Malaysia to China; goods described as generic "computer parts". | Two Chinese nationals in California (Chuan Geng, Shiwei Yang) charged. Outcome **unverified**. | Company formed shortly after controls tightened; failed a BIS end-use check in Singapore; ~$1M paid by a China-based company; freight forwarders as consignees. |
| **Operation Gatekeeper / Hao Global LLC** (S.D. Tex., announced 8 Dec 2025) [1] | At least $160M of Nvidia H100/H200 GPUs exported or attempted, Oct 2024–May 2025. Straw purchasers; paperwork naming US or third-country customers; Nvidia labels removed and replaced with a fake brand ("SANDKYAN"); goods misdescribed. | **Alan Hao Hsu and his Texas LLC pleaded guilty** (10 Oct 2025); faces up to 10 years. Benlin Yuan (CEO of a Virginia IT firm, subsidiary of a Beijing company) and Fanyue Gong (New York tech company owner) charged; Yuan faces up to 20 years. >$50M seized. Later outcomes **unverified**. | >$50M in wires from China to a small Texas LLC; relabelling; US-subsidiary-of-Chinese-parent; instructions to inspectors not to mention China; cover stories for detained goods. |
| **Janford Realtor LLC** (Florida, charged Nov 2025) [2][11] | A "real estate" front company bought GPUs (about 400 A100s, plus H200s) and used fake Malaysia/Thailand end-user contracts. | Two US citizens and two Chinese nationals charged. Outcome **unverified**. | Company's stated business unrelated to chips; ~$4M wired from China; fake end-user contracts. |
| **Supermicro-linked case** (S.D.N.Y., unsealed 19 Mar 2026) [3][12] | ~$2.5B of GPU servers (2024–25) ordered through a Southeast Asian company, shipped via Taiwan, repackaged in unmarked boxes and sent to China; "dummy" servers and false documents shown to auditors. | Co-founder/executive Yih-Shyan "Wally" Liaw, Taiwan GM Ruei-Tsang Chang (fugitive), third-party intermediary Ting-Wei Sun — conspiracy to violate ECRA. **The company itself was not charged.** | Intermediary company as nominal buyer; repackaging; staged inventory for inspections; insiders overriding compliance. |
| **Thai front-company case** (N.D. Cal., Mar 2026) [5] | Attempt to buy 750 servers (~$170M; 600 with controlled GPUs) "for a Thai client", plus a second 500-server attempt for another Thai company. A false non-diversion certificate was signed. Order never completed. | Stanley Yi Zheng (Hong Kong), Matthew Kelly and Tommy Shad English (US citizens) — conspiracy and smuggling. | No one from the "Thai customer" on emails; China-based company copied instead; chip maker could not verify end user; messages about chip prices in China. |
| **Earthmade Computer** (C.D. Cal., indicted 29 Sep 2026) [4][13] | ~$300M of Nvidia-GPU servers bought from US distributors and routed via Malaysia and Singapore to China in 2023–24 with false paperwork. | Owner Greg Lui: conspiracy to violate ECRA, smuggling, money-laundering conspiracy; up to 50 years in total. Reported ~$176M received from two Malaysian shipping companies (**figure unverified**). | Small reseller with sudden nine-figure volumes; payments from logistics companies rather than end users; hub routing. |

**What these tell a broker**
1. Intermediaries are the target. Not being the manufacturer or the end user protects no one.
2. A guilty plea came from a single-owner LLC [1]. Corporate form did not protect the owner.
3. Attempts are charged even when no goods ship [5].
4. Money-laundering and smuggling counts get added, raising exposure beyond ECRA's 20 years [4].
5. Signing a false end-use certificate is itself evidence of willfulness [5].

### B. Third-country diversion and investigations

- **Singapore:** In Feb 2025 Singapore charged three men with fraud for misrepresenting the end destination of Dell/Supermicro servers (about US$390M) that moved on to Malaysia; trial outcome **unverified** [9][14]. Singapore police said on 30 Oct 2026 that their investigation into **Megaspeed** remains ongoing [9].
- **Megaspeed (Singapore/Indonesia/Malaysia neocloud):** Founded 2023, shortly after the first chip rules; reportedly bought billions of dollars of Nvidia chips and rents compute from Southeast Asian data centres. Bloomberg (Dec 2025) reported US scrutiny of its ownership and possible diversion. On 9 Nov 2026 press reports said a Commerce inquiry was moved to DOJ after contact from Nvidia's general counsel, and that US intelligence believes a co-founder has Chinese intelligence ties. **No charges. Megaspeed and Nvidia deny diversion; Megaspeed says BIS and Malaysian inspections found no violations** [8][9]. Lesson: a neocloud can be a "core Nvidia partner" and still be a compliance question mark — partner status is not due diligence.
- **Malaysia / Thailand:** repeated destination in the cases above; US pressure on both governments to monitor GPU flows was widely reported in 2025 (details **unverified** this session).
- **UAE / Gulf:** moved to a more favourable country group by a BIS rule effective 10 Jul 2026, but advanced chips still need a licence except for approved entities [15]. Treat as hub risk.
- **BIS's own view:** controls were extended beyond China to address PRC entities acquiring chips "through transshipment and diversion, and by accessing datacenters with advanced ICs" [6].

### C. Chinese firms accessing chips through overseas cloud rental

| Report | What is reported | Legal status |
|---|---|---|
| Moonshot AI — Thailand (White House statement, July 2026) and Europe (CNBC, 5 Nov 2026) [7] | Accessed Blackwell chips via a Thai facility; then discussed renting 8,000+ Blackwell GPUs from European neoclouds for inference and possibly training; offered 30–50% more upfront. No provider named; deals not confirmed. | Not charged. CNBC: current law does not give regulators broad authority over overseas cloud access. |
| Alibaba, ByteDance, Tencent renting overseas capacity [16] | Carnegie-cited reporting says large Chinese platforms obtain compute in Malaysia/Thailand and elsewhere; one outlet reports a Tencent–Oracle lease of 100,000 GPUs (**unverified, single weak source**). | Not unlawful per se today; hardware exports *to* these entities need a licence anywhere in the world [17]. |
| US government review (Bloomberg, 7 Aug 2026) [18] | A US agency is reviewing Chinese AI firms' access via overseas data centres. | Policy review; secondary source only (**unverified**). |
| Nvidia "51% non-Chinese" requirement for cloud partners (FT, via CNBC) [7] | Suppliers reportedly must keep Chinese customers a minority. | Commercial policy (**unverified**). Means your suppliers may be contractually unable to take such customers. |
| Remote Access Security Act [19] | Would let BIS license remote access. Passed House 369–22; Senate pending. | **Proposed.** A premium paid by a Chinese renter is partly a hedge against this law [7] — i.e. the customer expects to be cut off. |

**Why this matters even though it is "legal":** BIS has said foreign parties who train models for China-headquartered firms that could support military/WMD uses "may be added to the Entity List, even where no violation of the EAR occurs" [20]. A US LLC with "knowledge" faces the §744.6 support rule. And the next rule may apply to existing contracts.

### D. Supplier-side lessons (Section 6, item 6 overlap)

1. **Ask where the chips came from.** If a supplier outside the big clouds cannot name its OEM/distributor or show purchase evidence, the hardware may be diverted. Brokering access to chips you have reason to know were unlawfully exported engages General Prohibition 10.
2. **Verify the data centre exists.** BIS red flags include a data centre that cannot affirm power, cooling and space, and an unknown installation address [6]. Ask for facility name, address, colocation provider and a tier/audit document.
3. **Screen supplier owners,** not just the company: Consolidated Screening List, ultimate parent HQ, date of incorporation (post-Oct 2022 is a BIS flag) [6].
4. **Ask who else they serve.** BIS flags an IaaS provider that "does not or cannot affirm that users of its services are not headquartered in the PRC" [6]. Such a supplier can be Entity-Listed overnight, stranding your customers.
5. **Location risk:** avoid capacity physically in China, Hong Kong, Macau, Russia, Belarus, Iran. Apply extra checks to Malaysia, Thailand, Indonesia, Singapore, UAE.
6. **Insiders defeat paperwork.** The Supermicro-linked case alleges staged "dummy" servers for auditors [3]. A certificate alone proves little; consistency across documents, payments and people proves more.
7. **Big suppliers do refuse.** Expect Tier-1 clouds and serious neoclouds to demand your customer's KYC. That is a feature: prefer suppliers who ask.

## Consolidated red flags (drawn from the cases and BIS guidance)

**Who the customer is**
- Company formed after October 2022, or weeks before the deal [2][6]
- No website, thin website, or English and Chinese versions that differ [6]
- Line of business unrelated to AI (real estate, trading, logistics) [2][11]
- Residential, virtual-office or freight-forwarder address [6]
- Headquarters or ultimate parent in China/HK/Macau — or refusal to say [6][17]
- US or third-country "subsidiary" of a Chinese IT company [1]
- Shares an address with a listed party [6]

**How the deal behaves**
- The named end user never appears; an agent or "consultant" speaks for them [5]
- Someone from an unrelated (especially China-based) company is copied in [5]
- Payment from a third party, a logistics firm, or from China/Hong Kong [1][2][4]
- Willingness to pay well above market, or large prepayment with little negotiation [7]
- Urgency, very large first order, no technical questions
- Cannot or will not describe workload, users, or user locations [2]
- Requests to keep the end user confidential from the supplier
- Asks you to sign or pass on certificates you cannot personally verify [5]
- Asks whether access can be used from China, or mentions VPNs/proxies

**Hardware and supplier**
- Any request to ship, store, relabel or re-invoice hardware [1][3]
- Goods described vaguely ("computer parts", "adapters") [1][2]
- Data centre that cannot be located or cannot show power/cooling [6]
- Supplier cannot explain chip provenance or cannot affirm its users are not PRC-headquartered [6]
- Capacity in a diversion hub offered far below market price
- Someone tells you not to mention China [1]

**Rule of thumb:** one unresolved red flag = pause and ask in writing. Two = refuse. Keep the notes.

## Questions for a lawyer / accountant

1. If I refer a customer and later learn it was a front for a restricted party, what is my exposure and should I self-disclose?
2. What written record of screening is enough to show I did not "self-blind"?
3. May I rely on a supplier's own KYC as a referral partner, or must I run my own?

## Sources
1. US DOJ, "U.S. Authorities Shut Down Major China-Linked AI Tech Smuggling Network" (8 Dec 2025) — https://www.justice.gov/opa/pr/us-authorities-shut-down-major-china-linked-ai-tech-smuggling-network — checked 2026-11-09
2. Morrison Foerster, "Managing Export Control Risks in the AI Chip Ecosystem" (9 Feb 2026) — https://www.mofo.com/resources/insights/260209-managing-export-control-risks-in-the-ai-chip-ecosystem — checked 2026-11-09
3. The Register, "Supermicro co-founder arrested, charged over $2.5B Nvidia GPU sales to China" (20 Mar 2026) — https://www.theregister.com/2026/03/20/supermicro_nvidia_gpu_charges/ — search summary, checked 2026-11-09 (DOJ release not retrieved)
4. Courthouse News, "California man charged with smuggling $300 million in restricted AI hardware to China" — https://courthousenews.com/california-man-charged-with-smuggling-300-million-in-restricted-ai-hardware-to-china/ ; indictment — https://www.courthousenews.com/wp-content/uploads/2026/10/greg-lui-indictment.pdf — search summary, checked 2026-11-09
5. The Register, "Three more charged with trying to smuggle GPUs to China" (26 Mar 2026) — https://www.theregister.com/on-prem/2026/03/26/three-more-charged-with-trying-to-smuggle-gpus-to-china/5224160 — checked 2026-11-09
6. BIS, Industry Guidance to Prevent Diversion of Advanced Computing ICs (13 May 2025) — https://www.bis.gov/media/documents/si-counter-diversion-industry-guidance-may-13-2025.pdf — read in full 2026-11-09
7. CNBC, "Chinese AI lab Moonshot turned to Europe for Nvidia Blackwell access amid U.S. China curbs" (5 Nov 2026) — https://www.cnbc.com/2026/11/05/moonshot-ai-nvidia-chips-europe-china.html — checked 2026-11-09
8. CNBC, "What is Megaspeed?…" (9 Nov 2026) — https://www.cnbc.com/2026/11/09/megaspeed-nvidia-jensen-huang-alice-huang.html — checked 2026-11-09
9. SCMP, "Singapore firm Megaspeed back in the spotlight…" — https://www.scmp.com/week-asia/politics/article/3373840/singapore-firm-megaspeed-back-spotlight-over-nvidia-scandal-china-chip-allegations ; Philadelphia Inquirer (NYT), "Commerce Department chip inquiry was halted after Nvidia intervention" (9 Nov 2026) — https://www.inquirer.com/news/nation-world/nvidia-investigation-commerce-justice-ai-chinese-spy-megaspeed-jensen-huang-trump-jeff-kessler-lutnick-20261109.html — search summaries, checked 2026-11-09
10. Courthouse News, "Chinese nationals charged with illegal exports of Nvidia chips" (Aug 2025) — https://www.courthousenews.com/chinese-nationals-charged-with-illegal-exports-of-nvidia-chips/ — search summary, checked 2026-11-09
11. The Register, "Four charged over alleged plot to smuggle Nvidia AI chips into China" (21 Nov 2025) — https://www.theregister.com/2025/11/21/nvidia_china_smuggling_charges/ — search summary, checked 2026-11-09
12. UPI, "3 indicted for smuggling AI-capable Nvidia chips to China" (20 Mar 2026) — https://www.upi.com/Top_News/World-News/2026/03/20/3-men-indicted-smuggling-ai-chips-china/9721774021211/ — search summary, checked 2026-11-09
13. SCMP, "US man arrested over alleged $300 million scheme to smuggle Nvidia AI servers to China" — https://scmp.com/news/us/article/3369637/us-man-arrested-over-alleged-300-million-scheme-smuggle-nvidia-ai-servers-china — search summary, checked 2026-11-09
14. Fortune, "Singapore charges three with fraud…" (28 Feb 2025) — https://fortune.com/asia/2025/02/28/singapore-charges-fraud-nvidia-chip-smuggling ; (3 Mar 2025) — https://fortune.com/asia/2025/03/03/singapore-probes-potential-fraud-in-nvidia-ai-chip-shipments/ — search summaries, checked 2026-11-09
15. Greenberg Traurig, "Navigating GPU Export Controls and AI Use Restrictions in Data Center Operations" (22 Sep 2026) — https://www.gtlaw.com/en/insights/2026/9/navigating-gpu-export-controls-and-ai-use-restrictions-in-data-center-operations — checked 2026-11-09
16. ForkLog, "China Accesses Nvidia Chips via Overseas Data Centers" (citing Carnegie) — https://forklog.com/en/china-accesses-nvidia-chips-via-overseas-data-centers/ ; kantan.news (Tencent–Oracle claim) — https://kantan.news/news/nvidia-imposes-51-requirement-on-overseas-cloud-operations-for-chinese-companies — secondary, **unverified**, checked 2026-11-09
17. BIS, Guidance on license requirements for D:5/Macau-headquartered entities (31 May 2026) — https://www.bis.gov/media/documents/bis-guidance-may-31-2026.pdf — read in full 2026-11-09
18. Secondary summary of Bloomberg (7 Aug 2026) — https://www.kucoin.com/news/flash/us-reviews-chinese-ai-firms-access-to-nvidia-chips-via-overseas-data-centers — **unverified**, checked 2026-11-09
19. Freshfields, "Remote Access or Remote Possibility?" (30 Jul 2026) — https://www.freshfields.com/en/our-thinking/blogs/a-fresh-take/remote-access-or-remote-possibility-rasa-and-the-future-of-cloud-export-controls-102nfbw — checked 2026-11-09
20. BIS, Policy Statement on… Commodities Used to Train AI Models (13 May 2025) — https://www.bis.gov/media/documents/ai-policy-statement-training-ai-models-may-13-2025 — read in full 2026-11-09
