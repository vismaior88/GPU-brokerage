# Government and public data-centre compute: is there a business?
_Last checked: 2026-11-16_

Builds on `demand-side.md` (free public compute: "mention it, never broker it") and `opportunities.md` (SEE public AI Factories, Serbia's National AI Platform, SAIFA). Those files already cover the free allocation tracks (Playground / Fast Lane / Large Scale), Serbia's free platform for universities and park startups, and the regional AI Factory map. This file looks at the part they did not: **paid** access to public compute, what it costs, and whether a broker can make money from it.

## Summary

- **Direct answer: no, not as a brokerage.** Public and government compute in Europe *can* be bought by private companies, but the rules are written to stop a middleman. The EuroHPC access policy says commercial access is pay-per-use, priced on cost and "aligned with commercial offerings" of the host, capped at 20% of capacity, civilian only, and limited to users from eligible countries [1]. Bulgaria's Discoverer acceptable-use policy (June 2026) lists "reselling or sublicensing access" as prohibited [14]. Renting from a government centre and reselling is out.
- **The "governments are cheaper" assumption is mostly wrong for a paying company.** Public centres are *legally required not to undercut the market*: EuroHPC pricing must be "based on market prices" [1]; Discoverer's policy says prices "should not disrupt the market" [15]; HLRS charges industry "market-standard" rates plus a 10–30% support surcharge [12]. What is cheap is the **free** tier, and that is only for eligible SMEs, researchers and (in Serbia) domestic academics and park startups.
- **Where public prices are published, they are cheap only for old hardware.** CSC sells LUMI's AMD MI250X at €0.535/GPU-hour to companies [6]; Vega (Slovenia) lists about €4.51/node-hour (4× A100, roughly €1.13/GPU-hour) [9][10]; Norway's state-owned Sigma2 charges commercial users 35 NOK/GPU-hour (about $3.40 at current rates — approximate) on its non-LUMI GPUs [7]. None publishes an H100/H200/B200 commercial rate; JUPITER and Greece's DAEDALUS have **no settled commercial price** at all [13][17].
- **The founder's US LLC itself is not an eligible user** for EuroHPC access (eligibility is EU Member States plus Horizon/Digital Europe associated countries; the US is excluded) [1][5]. Serbia and Montenegro companies *are* eligible [5].
- **HPC is a poor fit for most commercial buyers anyway**: Slurm batch queues, multi-day wall-time limits, no root, no long-running inference endpoints, and popular partitions are oversubscribed (MareNostrum 5, JUPITER Booster, MeluXina GPU closed to new Fast Lane/Playground requests) [3][4].
- **Serbia's Kragujevac State Data Centre** gives free compute to domestic academics and startups and offers colocation "under commercial conditions" by letter of interest; no paid GPU service or price list was found [19][20][21]. **Montenegro** has no public GPU capacity; a 4iG-built state data centre is still at the costing stage [23].
- **What could actually work (small):** (1) free "public-compute navigation" as lead generation for the core brokerage — but EuroHPC National Competence Centres (NCCs), including NCC Serbia and NCC Montenegro, **already do this for free** [24][35], so it is hard to charge for; (2) treating commercially run, state-linked providers (LuxProvide/MeluXina, IT4I, CSC, state telecoms) as ordinary suppliers, *if* they agree to a referral fee — none publishes a partner programme.
- **Verdict: Avoid as a separate business line.** Keep public compute as an honest referral and a lead source inside the existing brokerage. Do not resell, do not bid in public procurement, do not do "business development" for state centres, and do not take success fees on public allocations.

## Details

### 1. Which public compute can a private company pay for?

**EuroHPC JU (all EuroHPC systems and AI Factories).** The Access Policy (version 2025.12) [1] sets three relevant routes:

- *Free* AI Factories "Industrial Innovation" access (Playground, Fast Lane, Large Scale) for AI SMEs and startups "for innovation purposes". Larger companies are not covered: "Other industrial applications can benefit from pay-per-use commercial access" [1][2].
- *Commercial access* (§5.4): "any entity can buy access", up to 20% of resources, no peer review, results stay private. Conditions: civilian applications only, users from eligible countries, sign an acceptable-use agreement. Pricing is "based on the actual systems' acquisition and operational costs... aligned with commercial offerings of the Hosting Entity". Requests go to the EuroHPC Peer-Review Sector, which then agrees the exact price case by case [1]. **No price list is published.**
- Eligibility: users "residing, established or located in a Member State or a third country associated to the Digital Europe Programme or to Horizon Europe" [1]. A third-party summary lists Serbia, Montenegro, the UK, Norway, Switzerland, Türkiye, Ukraine and others as eligible and says US organisations cannot apply [5].
- Nothing in the policy provides for intermediaries; applications are by the end-user organisation with its own Principal Investigator [1][5].

**National centres (hosting entities) that sell to industry:**

| Provider | Country | Who may buy | GPU type | Published commercial price | Resale allowed? | Source |
|---|---|---|---|---|---|---|
| EuroHPC JU commercial access (any JU system) | EU | Companies/orgs from eligible countries, civilian use | Varies by system | Not published; negotiated, "based on market prices" | Not provided for; AUP signed by user | [1] |
| CSC – LUMI-G | Finland | Companies (framed around Finnish firms; 20% of Finland's share) | AMD MI250X | **€0.535/GPU-hour** (1 GPU-hour = one MI250X module = 2 GCDs) + €1,000 project set-up | Not stated (unverified) | [6][8] |
| Sigma2 (state-owned) | Norway | "Commercial and research and industry users paying market price" | Non-LUMI national GPUs (type not stated on page); LUMI | **35 NOK/GPU-hour** national GPU; 5.35 NOK/GPU-hour LUMI | Not stated (unverified) | [7] |
| IZUM – Vega | Slovenia | Companies with economic activity; max 20% of Slovenian share | 4× A100 40 GB per node | **~€4.51/node-hour excl. VAT** (€5.50 incl.) ≈ €1.13/GPU-hour | Not stated (unverified) | [9][10] |
| HLRS – Hunter / Vulcan | Germany | Industry ("Aufgabengruppe 5") | AMD MI300A APU; A100; A30 | Industry: market rate by agreement **+10–30% support surcharge**. For reference, university users pay €8.15/node-hour for Hunter APU nodes | Not stated (unverified) | [12] |
| IT4Innovations – Karolina | Czechia | Commercial companies (lease contract) | 8× A100 per node | Not published; rental form, contract, access within 3 working days | Contract not reviewed (unverified) | [11] |
| JSC – JUPITER | Germany | Startups, SMEs, large firms via AI Factory | GH200 | **No final price**; commercial use was stalled for months; 20% cap | — | [13] |
| PetaSC – Discoverer / Discoverer+ | Bulgaria | Anyone eligible, civilian, max 20% | H200 (Discoverer+) | Not published; must be "comparable to market prices" | **No – "reselling or sublicensing access" prohibited** | [14][15] |
| LuxProvide – MeluXina | Luxembourg | Enterprises via commercial contract; pay-per-access | A100 | Not published (quote on request) | Not stated (unverified) | [16] |
| GRNET – DAEDALUS / Pharos | Greece | Business services planned for March 2027 | — | Pricing "not yet finalised" | — | [17] |
| SRCE – Supek | Croatia | Research-oriented access rules; no commercial track found | 4× A100 per node | None found | — | [18] |
| BSC – MareNostrum 5, CINECA – Leonardo, GENCI – Jean Zay, Romania | ES / IT / FR / RO | Not checked in detail: no public commercial price found in searches | H100 (MN5), A100 (Leonardo) | None found **(unverified)** | — | — |

**Serbia.** The National AI Platform at the State Data Centre in Kragujevac is free for universities, institutes and domestic startups in science and technology parks [21]. The second system went live on 30 April 2026 [21]; a third, French-financed system with 640 NVIDIA chips is due "in the coming months" (Biznis.rs, 27 Oct 2026), and the same article again says existing capacity is used free of charge [20]. Officials have said access for businesses ("privreda") will come, but **no paid compute terms or prices were found** (unverified). The Office for IT and eGovernment runs the centre and has offered **colocation "under commercial conditions"** since 2020: send a letter of interest to kancelarija@ite.gov.rs; about 1,200 racks, Tier IV claimed; no price list [19]. Commercial tenants include CETIN and Huawei [22]; private colocation operators (e.g. Data Cloud Technology, Telekom Srbija's mts) also sell space there on request (directory listings, unverified).

**Montenegro.** No public GPU or HPC capacity. Hungary's 4iG was chosen in March 2026 to design and operate a Tier III state data centre (~€54m package with other ICT work); costs and financing were still being defined [23]. The state energy companies plan a consolidated data centre in Nikšić that "may" be used commercially later [23]. Montenegrin users get EuroHPC time abroad through NCC Montenegro at the University of Donja Gorica, which offers consulting, training and free access support [24].

**UK and US.**
- UK AI Research Resource (Isambard-AI, Dawn): allocated by call, not sold. The open-access call (closed 17 July 2026) required UK-registered organisations; no paid tier is described [25]. A separate SME "cloud access call" gave up to £400,000 of credits at approved cloud providers to ~20 UK SMEs; it closed 24 July 2026 [26].
- US NAIRR pilot: free allocations for US-based researchers, educators and certain startups; no commercial sale found [27]. DOE national labs: not researched in depth; commercial use is normally via partnership agreements (unverified).

**Subsidies paid to private suppliers.**
- India's IndiaAI Mission empanels private providers and subsidises GPU-hours for eligible Indian users; reported effective rates range from about ₹65 to ₹150 per GPU-hour depending on source and tender [28]. Only for Indian entities (unverified detail); not a market for this founder.
- Portugal's InovIA gives vouchers of 1,000 GPU-hours on *public* systems, for non-profit pre-commercial work by entities in Portugal [29].
- FFplus (EuroHPC-funded) gives SMEs money for HPC/generative-AI experiments; the 2026 call closed 25 February 2026 [30].
- I found **no current EU or Western Balkans voucher that pays a private GPU cloud on a buyer's behalf**. The UK cloud call is the closest, and it is UK-only and closed [26].

**State-owned or state-controlled companies selling compute.** Deutsche Telekom (the German state holds a minority stake, unverified here) opened its Industrial AI Cloud in Munich in February 2026, with no public rates [31]. Gulf sovereign providers (HUMAIN, G42/Core42) are covered in `opportunities.md` and are a diversion-risk region under the compliance policy. These sell like any commercial cloud: treat them as normal suppliers, not as "government compute".

### 2. Is government compute cheaper for a paying company?

Not by design. EU state-aid rules let public machines sell only a limited share (20%) commercially and require market-based pricing so they do not crowd out private clouds [1][13][15].

- **Cheaper on paper, older hardware.** LUMI MI250X at €0.535/GPU-hour [6] is well below anything in the market, but it is a 2021-generation AMD part on a batch system. Vega's A100 at about €1.13/GPU-hour [9] is in line with the A100 market ($1.03–1.59 on index, see `pricing-and-indexes.md`).
- **Market-level for modern GPUs.** Sigma2's 35 NOK commercial rate (~$3.40, approximate conversion) is about the same as the H100 index ($3.01–3.37). HLRS adds 10–30% to "market-standard" prices [12].
- **No published price for H100/H200/B200/GH200 at any EuroHPC site.** Everything modern is "on request".
- **Negotiable?** Price is set case by case by the JU and the host [1], but within a cost/market formula. There is no sign of discounting to win volume, and capacity is the bottleneck: several AI partitions are closed to new requests due to demand [3][4].
- **Hidden costs:** set-up fees (CSC €1,000 [6]), support surcharges (HLRS [12]), whole-node billing (LUMI bills a full node even for a partial job [8]), Slurm queues and wall-time limits.

**Conclusion:** the only meaningful discount is **free** access, and it is tied to the end user's eligibility, so a broker cannot capture it.

### 3. Rules that block a broker

| Rule | Effect | Source |
|---|---|---|
| Resale/sublicensing prohibited | Discoverer AUP explicitly bans "reselling or sublicensing access" and running workloads outside the approved contract | [14] |
| Credentials personal | "Never share private keys or delegate login to another person" (Discoverer); UK AIRR requires every user to be named in the application | [14][25] |
| End-user eligibility | Access goes to entities established in eligible countries; the applicant company's own engineer is the PI | [1][5] |
| US LLC not eligible | The founder's US entity cannot itself hold EuroHPC access | [1][5] |
| 20% commercial cap, market pricing | Little room for volume or margin; state-aid constraints | [1][13][15] |
| Civilian use only; embargo screening | Matches the founder's policy, but adds certification for every user | [1][15] |
| Open science on free tiers | Free users (except SMEs on private innovation) must publish; Large Scale SMEs must still report results | [1] |
| Public procurement | State centres buy and sell through tenders and formal agreements; JUPITER was held up by "tendering hurdles" | [13] |
| Batch scheduling | Jobs run through Slurm queues (IT4I states this for leased capacity); wall-time limits (e.g. 2 days on Vega GPU per a third-party university guide, unverified); no persistent services | [11] |

Whether non-Discoverer centres also ban resale was **not verified** (CSC, IZUM, IT4I contracts not read). The default assumption should be "prohibited unless written permission" — check each contract.

### 4. Business models: what could work

1. **Fee-for-service help applying for free public compute.** Allowed, but weak. NCCs exist in every participating country, including NCC Serbia (IPB) and NCC Montenegro (UDG), and offer consulting, training and access support **free of charge** [24][35]; AI Factory Antennas such as SAIFA do onboarding (see `demand-side.md`). The application is short (Playground uses templates) [4]. Few startups will pay for what the NCC gives away. No private consultancy charging for EuroHPC applications was found. **Use it as free lead generation instead.**
2. **Referral to centres that sell commercial access.** Permitted in principle (it is a sales introduction, not resale), but none of the centres checked publishes a partner or referral programme [6][11][16]. Most likely candidates to ask: LuxProvide (commercial company), IT4I (standard lease contract), CSC. Money flow: centre pays a disclosed referral fee, *if* a public body is allowed to do that at all (unverified; may need a procurement process on their side). Buyers would mostly be EU firms that want confidential results on a European system.
3. **Business development for government data centres (selling spare capacity).** Not realistic. Commercial share is capped at 20%, demand already exceeds supply on AI partitions [3][4], pricing is fixed by formula, and paying a commission-based agent would likely need public procurement. In Serbia and Montenegro, approaching officials to win business for a client can count as lobbying, which requires registration (Serbia: a foreign entity must also be entered in a special register [32]; Montenegro: new 2024 law, register run by the Agency for Prevention of Corruption [33]).
4. **Bidding as a supplier in government compute procurement.** Not realistic for a non-EU single-member LLC with no capacity, no references and no balance sheet. Tenders for AI compute are vendor-scale (e.g. Serbia's Eviden contract, see `opportunities.md`). Avoid.
5. **Rent from a government centre and resell.** **Prohibited** where checked [14], against the end-user eligibility model [1], and economically pointless at market-based prices. Avoid.
6. **Colocation at Kragujevac for GPU owners.** Colocation is offered commercially [19], but the founder would be referring hardware owners to a state facility outside the EU, with no price list and an unknown referral policy. A cleaner version is referring to the private colocation operators inside the building on normal commercial terms (unverified that they pay referrals). Later at most.
7. **Helping buyers use subsidies at commercial suppliers.** The only programmes found are UK-only (closed) or India-only [26][28]. Nothing for the founder's region today. Watch.

### 5. Compliance and conflict-of-interest risks

- **FCPA.** The US LLC is covered. DOJ treats employees of state-owned or state-controlled entities as "foreign officials" (e.g. *Esquenazi*) [34]. Staff at the Serbian Office for IT, state data centres, university HPC centres, Sigma2, Telekom Srbija or Deutsche Telekom may count. No gifts, hospitality or payments to obtain allocations, capacity or contracts. DOJ narrowed its enforcement priorities in June 2025 but the statute was not repealed [34].
- **Local anti-bribery and lobbying law.** Serbian and Montenegrin criminal codes and anti-corruption laws apply locally; lobbying rules apply to influencing public decisions (see item 3) [32][33].
- **Success fees on public allocations.** A free allocation is a public resource, not cash. Charging a client a percentage "of the GPU-hours won" is hard to value, may look like selling access to a public good, and could breach programme rules (not verified either way). Charge only a flat fee for work done, if anything.
- **Conflict of interest.** Advising a client to apply for free compute and also earning a commission on paid compute pulls in opposite directions. Disclose both roles in writing, tell the client when free access fits better, and never steer them away from a free allocation they qualify for. This is already flagged in `demand-side.md`; this file adds that the risk is higher if the founder also ever takes a fee from a public centre.
- **Misrepresentation.** Never imply a special relationship with EuroHPC, an NCC or the Serbian government. Never apply on a client's behalf under their name or hold their credentials [14].
- **Sanctions/end use.** Public centres certify civilian use and embargo compliance [1][15]; the founder's own KYC still applies to anyone referred. Note Huawei is a tenant at Kragujevac [22]; this does not breach the founder's customer policy but matters for any EU buyer's data-residency or supply-chain review.

## Ranked opportunities

Scores 1–5; higher is better on every column (5 = high potential, low startup cost, low risk, good solo fit).

| # | Opportunity | Potential | Startup cost | Risk | Solo-founder fit | Decision |
|---|---|---|---|---|---|---|
| 1 | Free public-compute navigation (point clients to NCCs/SAIFA/AI Factories, then offer paid capacity when they outgrow it) | 2 | 5 | 4 | 5 | **Do now** (as lead generation, not revenue) |
| 2 | Referral to commercially run public/state-linked providers (LuxProvide, IT4I, CSC, state telecoms) — only if a written, disclosed referral agreement is offered | 2 | 4 | 3 | 4 | **Later** (one enquiry each, inside normal supplier outreach) |
| 3 | Kragujevac colocation referrals (via private operators in the building) | 1 | 4 | 3 | 3 | **Later** |
| 4 | Paid application-writing / onboarding consultancy | 1 | 4 | 3 | 4 | **Avoid** (NCCs do it free) |
| 5 | Helping buyers use compute subsidies at commercial suppliers | 1 | 4 | 3 | 3 | **Avoid for now** (no eligible scheme in region; watch) |
| 6 | Business development for government data centres | 1 | 3 | 1 | 2 | **Avoid** |
| 7 | Bidding in government compute procurement | 1 | 1 | 2 | 1 | **Avoid** |
| 8 | Rent from a government centre and resell | 1 | 2 | 1 | 2 | **Avoid** (prohibited) |

## Questions for a lawyer / accountant

1. Can a public HPC centre (e.g. LuxProvide, IT4I, CSC, IZUM) lawfully pay a commission to a non-EU referral agent, or would that need public procurement on their side? Does it change if LuxProvide is a private company owned by the state?
2. Under the FCPA and Serbian/Montenegrin law, which public-centre and state-telecom staff are "foreign officials"? What hospitality (coffee, event tickets) is acceptable when meeting them?
3. Would introducing a client to the Serbian Office for IT for colocation or future paid compute count as "lobbying" under Serbia's Law on Lobbying (or Montenegro's 2024 law)? Would the US LLC need to be entered in the foreign-lobbyist register?
4. If the founder helps a client apply for free EuroHPC or National AI Platform access, may the founder charge a flat fee? A success fee? Is either inconsistent with programme terms?
5. What disclosure language should the buyer agreement contain when the founder both advises on free public compute and earns a commission on paid compute?
6. Accountant: if a referral fee is ever paid by an EU public body to the US LLC, what withholding, VAT reverse-charge or invoicing rules apply (and how does this interact with the founder's Montenegrin tax residence)?

## Sources

1. EuroHPC JU, Access Policy, Version 2025.12 (PDF; §1.3, §2.1, §3.3, §5.4) — https://www.eurohpc-ju.europa.eu/document/download/30614065-6dd6-4206-8065-fc97948e5e2c_en?filename=EuroHPC%20JU%20Access%20Policy%20-%20Version%202025.12.pdf — checked 2026-11-16
2. EuroHPC JU, AI Factories access modes — https://eurohpc-ju.europa.eu/ai-factories/ai-factories-access-modes_en — checked 2026-11-16
3. EuroHPC JU, Fast Lane access – systems temporarily closed — https://www.eurohpc-ju.europa.eu/fast-lane-access-ai-factories-temporarily-closed_en — checked 2026-11-16
4. EuroHPC JU, Playground access – systems temporarily closed — https://www.eurohpc-ju.europa.eu/playground-access-ai-factories-temporarily-closed_en — checked 2026-11-16
5. EU AI Continent (euacc.ai), "Can I apply? AI Factories" (third-party summary, page dated 18 Oct 2026) — https://www.euacc.ai/can-i-apply/ai-factories — checked 2026-11-16
6. CSC, High-performance computing for companies (LUMI price list) — https://csc.fi/en/customers/high-performance-computing-for-companies/ — checked 2026-11-16
7. Sigma2, User contribution model (pricing, valid from 1 Oct 2025) — https://www.sigma2.no/node/106 — checked 2026-11-16
8. LUMI documentation, Billing policy — https://docs.lumi-supercomputer.eu/runjobs/lumi_env/billing — checked 2026-11-16 (via search summary)
9. IZUM, HPC Vega price list — https://vegadocs.vega.izum.si/price-list/ — checked 2026-11-16 (page returned 503 on direct fetch; figures from search snippet; confirm)
10. IZUM, HPC Vega architecture — https://doc.vega.izum.si/architecture — checked 2026-11-16 (via search summary)
11. IT4Innovations, Rental of computational resources — https://www.it4i.cz/en/industry-cooperation/portfolio-of-services/rental-of-it4innovations-computational-resources — checked 2026-11-16
12. HLRS, Entgeltordnung price overview from 04/2026 (PDF) — https://www.hlrs.de/fileadmin/start_computing/HLRS_Entgeltordnung_202604_Preisuebersicht.pdf — checked 2026-11-16
13. TechCentral.ie, "Red tape and complex funding model leave Germany's JUPITER supercomputer underused" (7 Jul 2026) — https://www.techcentral.ie/red-tape-and-complex-funding-model-leave-germanys-jupiter-supercomputer-underused/ — checked 2026-11-16
14. PetaSC, Discoverer Acceptable Use Policy v1.0 (8 Jun 2026), §5.3, §6 — https://docs.discoverer.bg/_downloads/4f6e6f119f308241c158462a8b844cdd/aup.pdf — checked 2026-11-16
15. PetaSC, Discoverer Access Policy, §3.6 — https://discoverer.bg/wp-content/uploads/2024/07/discoverer-access-policy.pdf — checked 2026-11-16
16. LuxProvide, MeluXina — https://www.luxprovide.lu/meluxina/ ; brochure — https://gouvernement.lu/dam-assets/documents/actualites/2022/06-juin/14-fayot-meluxina/brochure-sur-luxprovide-meluxina.pdf — checked 2026-11-16 (via search summary)
17. Euronews, "Daedalus: Greece unveils new supercomputer" (19 Oct 2026) — https://www.euronews.com/2026/10/19/daedalus-greece-unveils-new-supercomputer-as-it-eyes-role-in-europes-ai-race ; Magica — https://magica.com/news/greece-daedalus-supercomputer-business-access-march-2027 — checked 2026-11-16 (via search summary)
18. SRCE, Advanced computing — https://srce.unizg.hr/en/advanced-computing — checked 2026-11-16 (via search summary)
19. Government of Serbia, "State Data Centre in Kragujevac opens door to business entities" (1 Sep 2020) — https://www.srbija.gov.rs/vest/en/160516/state-data-centre-in-kragujevac-opens-door-to-business-entities.php — checked 2026-11-16
20. Biznis.rs, third supercomputer for Kragujevac (27 Oct 2026) — https://biznis.rs/vesti/srbija/srbija-do-kraja-godine-dobija-treci-superkompjuter-20-puta-snazniji-od-postojeceg/ — checked 2026-11-16
21. 021.rs, new supercomputer launched in Kragujevac (30 Apr 2026) — https://www.021.rs/info/srbija/442118/pusten-u-rad-novi-superkompjuter-u-data-centru-u-kragujevcu-bice-potrebne-dodatne-kolicine-struje — checked 2026-11-16
22. Biznis.rs, Huawei becomes user of State Data Centre — https://biznis.rs/vesti/huawei-postaje-korisnik-drzavnog-data-centra-u-kragujevcu-kineska-kompanija-siri-svoje-poslovanje-u-srbiji/ ; CETIN — https://biznis.rs/vesti/cetin-novi-korisnik-drzavnog-data-centra-u-kragujevcu/ — checked 2026-11-16 (via search summary)
23. bne IntelliNews, Montenegro selects 4iG for €54m ICT and data centre projects — https://new.intellinews.com/articles/montenegro-selects-hungary-s-4ig-group-for-54mn-ict-and-data-centre-projects-434012 ; Balkan Green Energy News, consolidated data centre — https://balkangreenenergynews.com/montenegros-epcg-dso-tso-to-establish-consolidated-data-center — checked 2026-11-16 (via search summary)
24. NCC Montenegro (UDG), "Are you ready to use HPC?" and About — https://eurocc.udg.edu.me/?p=1792 ; https://eurocc.udg.edu.me/about/ — checked 2026-11-16 (via search summary)
25. GOV.UK, AI Research Resource – AI open access call — https://www.gov.uk/government/publications/ai-research-resource/ai-open-access-call — checked 2026-11-16
26. GOV.UK, AI Research Resource – Cloud access call — https://www.gov.uk/government/publications/ai-research-resource/cloud-access-call — checked 2026-11-16
27. NAIRR Pilot, FAQ — https://nairrpilot.org/about/faq — checked 2026-11-16 (via search summary)
28. Communications Today (IndiaAI GPU-hours sanctioned) — https://www.communicationstoday.co.in/?p=424384 ; ThePrint — https://theprint.in/tech/indiaai-mission-9-model-builders-get-rs-1058-cr-of-govts-compute-subsidy-researchers-only-rs-10-cr/3076401/ ; Business Standard — https://business-standard.com/technology/artificial-intelligence/india-ai-compute-race-subsidised-gpu-capability-gap-126062900734_1.html — checked 2026-11-16 (via search summary)
29. FCCN, InovIA vouchers — https://rnca.fccn.pt/en/acesso/inovia/ — checked 2026-11-16
30. ETP4HPC, Second FFplus open call for innovation studies — https://etp4hpc.eu/2025/12/17/second-ffplus-open-call-for-innovation-studies/ — checked 2026-11-16 (via search summary)
31. Deutsche Telekom, Germany's first AI factory for industry goes live in Munich (Feb 2026) — https://www.telekom.com/de/newsroom/aktuelles/medieninformationen/2026/02/deutschlands-erste-ki-fabrik-fuer-die-industrie — checked 2026-11-16 (via search summary)
32. Serbia, Law on Lobbying (unofficial English, Agency for Prevention of Corruption) — https://www.acas.rs/storage/page_files/Law%20on%20Lobbying.pdf — checked 2026-11-16 (via search summary; 2025 amendments not reviewed)
33. CEE Legal Matters, "Reform of the Lobbying Act" (Montenegro) — https://ceelm.com/briefings/27119-reform-of-the-lobbying-act-one-step-closer-to-montenegro-s-eu-integration ; AALEP, Lobbying regulation in Montenegro — https://aalep.eu/node/3149 — checked 2026-11-16 (via search summary)
34. US DOJ/SEC, FCPA Resource Guide — https://www.justice.gov/criminal-fraud/fcpa-resource-guide ; Harvard Law School Forum, "DOJ Resumes FCPA Enforcement with New Guidelines" (25 Jun 2025) — https://corpgov.law.harvard.edu/2025/06/25/doj-resumes-fcpa-enforcement-with-new-guidelines/ — checked 2026-11-16 (via search summary)
35. NCC Montenegro, HPC4SME assessment tool (free report, NCC follow-up) — https://eurocc.udg.edu.me/hpc4sme-assessment-tool/ ; HLRS EuroCC project — https://www.hlrs.de/projects/detail/eurocc — checked 2026-11-16 (via search summary)
