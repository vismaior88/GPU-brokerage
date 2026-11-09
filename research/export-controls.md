# US export controls (EAR) for a GPU-capacity broker
_Last checked: 2026-11-09_

> Not legal advice. This is a research summary to help you decide which deals to refuse and when to pay for a US export-controls lawyer. It never describes ways around the rules.

## Summary

- **Your LLC is a "U.S. person" under the EAR, wherever you live.** The definition covers "any juridical person organized under the laws of the United States" [1]. You personally (non-US citizen, living in Montenegro) are probably not a "U.S. person" as an individual, but everything you do *as the LLC* is done by a U.S. person, and several EAR prohibitions apply to **any** person of any nationality [2][3].
- **Renting or brokering remote access to GPUs is, today, generally not itself an "export" of the chip.** That is the long-standing BIS position and the gap Congress calls the "cloud loophole" [4][5][6]. **This does not make China-linked deals safe.**
- **What does bite on you now:** (a) the U.S.-person "support" rule in §744.6, which covers "performing any contract, service, or employment" and "conducting negotiations in furtherance of" a prohibited end use [7]; (b) BIS's May 13, 2025 policy statement, which says a U.S. person may need a licence to provide any support or service when it has "knowledge" the activity may assist **training AI models for or on behalf of parties headquartered in China/D:5 or Macau** where the model will be used for a WMD or military-intelligence end use [8]; (c) Entity List and other end-user controls; (d) General Prohibition 10 (don't service or facilitate anything you know involves a violation) [3].
- **"Knowledge" includes willful blindness.** It means actual knowledge *or* "an awareness of a high probability", inferred from "conscious disregard" or "willful avoidance of facts" [1]. Not asking is not a defence.
- **Chinese-headquartered customers anywhere in the world are the core risk.** BIS confirmed on May 31, 2026 that *hardware* exports to any entity headquartered in, or with an ultimate parent in, a D:5 country or Macau need a licence even when the entity sits in Singapore, Europe or elsewhere [9]. Renting to them is not flatly banned today, but it is the exact activity BIS, the White House and Congress are targeting [6][10][11].
- **The law is moving against remote access.** The Remote Access Security Act passed the House 369–22 (Jan 12, 2026) and is pending in the Senate; it and the Chip Security Act may ride on the FY2027 defence bill. **Not enacted as far as I could verify** [5][6][12].
- **No US KYC rule for IaaS providers/resellers is in force.** The January 2024 proposed rule was never finalised (as far as I could verify) [13]. Suppliers will still push KYC onto you by contract.
- **Penalties are personal.** Civil: up to $374,474 per violation or twice the transaction value (no intent needed). Criminal (willful): up to $1 million and 20 years per violation. Plus denial of export privileges [14].
- **Recommendation:** adopt a hard rule — **no customer that is in, headquartered in, or ultimately owned/controlled from China, Hong Kong, Macau, Russia, Belarus, Iran, North Korea, Cuba, Syria or Venezuela, and no customer who will not prove who they are and what the workload is.** That costs you little business and removes most of the risk.

## Status board (as of 9 Nov 2026)

| Measure | Status | Note |
|---|---|---|
| Oct 2022 / Oct 2023 / Dec 2024 chip rules (ECCN 3A090, 4A090, .z items) | **In force** | Licence needed for China, Macau, and D:1/D:4/D:5 destinations (with A:5/A:6 carve-outs) [9][15] |
| Licence for D:5/Macau-**headquartered** entities worldwide (hardware) | **In force**, re-confirmed 31 May 2026 | §742.6(a)(6)(iii)(A); existing data-centre operations need not stop "until further notice" [9] |
| U.S.-person support controls, §744.6 | **In force** | [7] |
| May 13, 2025 BIS policy statement (AI training / IaaS) and diversion red-flag guidance | **In force** (guidance) | [8][15] |
| AI Diffusion Rule (Jan 2025: worldwide licensing tiers, model-weights ECCN 4E091) | **Not enforced**; BIS announced rescission 13 May 2025. Text reportedly still in the CFR; formal removal **unverified** | Replacement rule promised (July 2026 testimony) but not issued [9][16][17] |
| Jan 15, 2026 rule: H200 / MI325X-class chips to China — case-by-case review | **In force** | Licence conditions include KYC and **no remote access for military/Entity List parties**, listing of IaaS remote users [18] |
| Entity List "Affiliates Rule" (50% ownership) | **Suspended** to 10 Jan 2027 | Issued 29 Sep 2025, suspended 10 Nov 2025, extension published 9 Nov 2026 [19] |
| IaaS KYC / Customer Identification Program rule (EO 13984 / EO 14110) | **Proposed only** (Jan 2024), never finalised (status after May 2026 **unverified**) | EO 14110 was revoked Jan 2025 [13] |
| Remote Access Security Act (H.R. 2683 / S. 3519) | **Proposed** — passed House; Senate pending | Would let BIS license remote access [5][6] |
| Chip Security Act (location verification), AI OVERWATCH Act, MATCH Act | **Proposed** — in Senate FY2027 NDAA manager's package; final outcome **unverified** | [12][16] |
| GAIN AI Act | **Proposed / apparently dropped**; **unverified** | [12] |
| Nvidia reportedly requiring cloud partners to sell ≥51% to non-Chinese customers | Commercial policy, reported by FT via CNBC; **unverified** | [10] |

## Details

### Q22 — How the EAR reaches a US LLC run from Montenegro

- **The LLC:** a U.S. person. The §744.6 activity controls apply to it regardless of where the hardware sits or whether any item is "subject to the EAR" [1][7].
- **You personally:** the U.S.-person definition covers US citizens, green-card holders, protected individuals, and "any person in the United States" [1]. If none applies, you are not individually a U.S. person — but you are the person acting for one, and BIS and DOJ charge individuals, not just companies (see the cases file).
- **Rules that apply to everyone, including foreigners:** the EAR follows the *item*. Nvidia/AMD AI chips remain "subject to the EAR" in a foreign data centre. Anyone who causes, aids, abets, conspires in, or acts with knowledge of a violation commits a violation (§764.2), and General Prohibition 10 bars selling, financing, ordering, transporting, forwarding or "otherwise servicing" an item with knowledge a violation has occurred or will occur [2][3].
- **Montenegrin/EU law** is separate and outside this file — ask local counsel.

### Section 6.1 — Which chips, which destinations

- **Controlled items:** advanced ICs in ECCN **3A090.a/.b**; computers/servers containing them in **4A090.a/.b**; and ".z" items such as servers under 5A992.z [8][9][15]. In practice: essentially all current data-centre AI GPUs (A100, H100, H200, Blackwell and peers). Exact classification is the exporter's job.
- **Destinations for hardware:** licence required for China, Macau and other D:1/D:4/D:5 destinations (carve-outs for A:5/A:6 countries), and for D:5/Macau-headquartered entities **anywhere** [9][15]. H200-class chips to China can now be licensed case by case under strict conditions; anything stronger remains effectively blocked [18].
- **You will not ship hardware.** Never agree to source, forward, hold or pay for physical GPUs or servers on someone's behalf — that is where almost every prosecution sits.

### Section 6.1 — Is providing or brokering cloud access an "export"?

**Generally no — today.** BIS advisory opinions (2009, 2011, 2014) treat providing computing capacity as a service, not an export of the hardware; law-firm alerts in 2026 still describe remote access by restricted-country users as generally not licensable under current law [4][5][6]. **But these restrictions still apply:**

| Rule | What it means for a broker |
|---|---|
| **§744.6 U.S.-person support** [7] | No U.S. person may "support" WMD end uses anywhere or a **military-intelligence end use/user** in China, Russia, Belarus, Burma, Cambodia, Venezuela or E:1/E:2 countries. "Support" includes performing any contract or service and conducting negotiations you know may assist. Brokering fits that language. |
| **May 13, 2025 policy statement** [8] | A U.S. person providing any support/service, with knowledge it may assist training AI models for D:5/Macau-headquartered parties, may need a licence where there is knowledge of WMD/military-intelligence use. BIS also says foreign providers doing this can be **Entity-Listed "even where no violation of the EAR occurs."** |
| **Entity List / MEU List / Part 744 end-user controls** | Never arrange anything for a listed party. The 50% Affiliates Rule is suspended, but a subsidiary of a listed party is still a major red flag [19]. |
| **General Prohibition 10 / §764.2** [2][3] | If the supplier's chips were diverted or exported unlawfully and you have reason to know, your brokering is itself a violation. |
| **Model weights / AI-training outputs** | The 4E091 control from the AI Diffusion Rule is not being enforced [9][17]; the Jan 2026 China licence conditions do restrict transfer of model weights by IaaS providers using licensed chips [18]. Low direct relevance to a broker; high relevance to who your supplier may serve. |
| **Supplier licence conditions and contracts** | Suppliers' export licences, Nvidia terms and cloud ToS often bar Chinese-HQ or military users. Breaching them through you ends the relationship and creates evidence of knowledge. |

**Chinese-owned subsidiaries outside China; Chinese firms renting overseas capacity**

- **Legally restricted now:** any deal with an Entity-Listed party; any deal where you know or have reason to know the workload supports military-intelligence or WMD end uses; anything involving hardware moving to a D:5/Macau-HQ entity; any role in a deal you have reason to know involves diverted chips.
- **Not clearly prohibited, but high-risk:** arranging ordinary commercial compute for a non-listed company headquartered in or owned from China (including its Singapore, Cayman or EU subsidiary). BIS's guidance treats "IaaS provider cannot affirm its users are not headquartered in the PRC" as a red flag [15], the White House publicly named a Chinese lab for using Blackwell chips in Thailand [10], and US agencies are reviewing the practice [11]. A solo broker cannot realistically verify the absence of military links for a Chinese AI lab — so "reason to know" exposure is real.
- **Honest view:** for a <$2k solo operation this segment is not worth it. Refuse it and say so on your website.

### Section 6.2 / 6.4 — KYC duties and the proposed IaaS rule

- **No statutory KYC programme applies to you today.** The Jan 2024 proposal would have required US IaaS providers *and their foreign resellers* to run a Customer Identification Program for foreign customers [13]. A pure referral partner is probably not a "reseller"; a broker who contracts and re-bills might be. Not in force, so this is a design consideration, not an obligation.
- **BIS "Know Your Customer" guidance (Supp. No. 3 to Part 732) does apply as the standard you will be judged by.** Core points: you need not investigate every customer, but if red flags appear you must inquire and resolve them; you may not "self-blind"; do not tell staff or partners to avoid learning facts [8][15][20]. BIS's 2025 list adds AI-chip red flags: customer incorporated after Oct 2022, no web presence, residential or virtual-office address, unknown installation/usage location, refusal to disclose HQ or ultimate parent, data centre that cannot show power/cooling, IaaS provider that cannot affirm its users are not PRC-headquartered [15].
- **Minimum practical KYC for you:** legal name, registration number, registered and operating address, ultimate beneficial owners and ultimate parent HQ, website/domain age, who will use the compute and for what, where users are located, source of payment (must match the customer); screen every party against the US Consolidated Screening List; get a signed end-use/end-user statement; keep records for 5 years. Repeat for suppliers (see cases file).

### Section 6.8 — "Knowledge", penalties, self-disclosure

- **Knowledge** (§772.1): "positive knowledge" or "an awareness of a high probability of its existence or future occurrence", inferred from "conscious disregard of facts" or "willful avoidance of facts" [1]. "Reason to know" is a variant of the same term. In plain words: if a reasonable person in your seat would have suspected, you "knew".
- **Civil (administrative) penalties:** up to **$374,474 per violation or twice the transaction value, whichever is greater** (the 2025 figure; the 2026 inflation adjustment was cancelled government-wide) [14][21]. Strict liability — no intent required.
- **Criminal:** willful violations — up to **$1,000,000 and 20 years' imprisonment per violation** [14]. Smuggling and money-laundering counts are often added (see cases).
- **Other:** denial of export privileges (nobody may deal with you in EAR items — fatal for this business), Entity List designation, loss of banking and supplier relationships [14].
- **Small-company reality:** an LLC does not shield you personally from your own conduct; prosecutors have charged owners of one-person companies.
- **Voluntary self-disclosure (§764.5):** telling BIS promptly about a possible violation is a significant mitigating factor. If you ever think a completed deal was problematic, stop, preserve records, call a lawyer the same week [9].

## What this means for me

| Deals I must refuse | Deals needing a lawyer first | Deals that are generally fine |
|---|---|---|
| Customer, user or payer on the Entity List, MEU list, SDN list or other Consolidated Screening List entry | Customer incorporated in a neutral country but with Chinese/HK/Macau founders, investors or parent below obvious control | Customer headquartered and owned in the US, EU/EEA, UK, Switzerland, Canada, Japan, Australia and similar allied countries, using capacity in those countries |
| Customer located in, headquartered in, or ultimately owned from China, Hong Kong, Macau, Russia, Belarus, Iran, North Korea, Cuba, Syria, Venezuela | Customers or data centres in transshipment-risk hubs: Malaysia, Singapore, Thailand, Indonesia, Vietnam, UAE, Saudi Arabia, Turkey, Central Asia, Caucasus | Western Balkans customers (Serbia, Montenegro, etc.) with transparent local ownership, a real business, and an ordinary commercial workload — after screening |
| Any military, intelligence, weapons, surveillance or defence-research workload outside allied governments | Any request involving model-weight transfer to, or users in, a restricted country | Universities and startups you can verify from public records |
| Anyone who refuses to disclose owners, HQ, end users or workload, or who wants to pay through an unrelated third party or in cash/crypto | Becoming a contracting reseller (you re-bill) rather than a referral partner — changes your legal role | Referral-only deals where the supplier performs its own KYC and contracts directly with the customer |
| Any request to buy, hold, ship, relabel or re-export physical GPUs/servers | Any deal of unusual size from a company formed after Oct 2022 with no track record | — |
| A supplier that cannot say how it obtained its chips, or whose capacity sits in China/Russia | Any situation where you later learn a past deal may have involved a restricted party (self-disclosure question) | — |
| Anyone offering a premium "because we are Chinese" or asking you to hide the true end user | Anything once RASA or a replacement AI rule is enacted | — |

## Questions for a lawyer / accountant

1. As a non-US individual running a US LLC from Montenegro, do my own acts count as acts of a "U.S. person" under §744.6 in every case? Would a non-US entity change exposure, and should it?
2. Does a referral-fee or buyer-paid broker role amount to "support"/"conducting negotiations" under §744.6(b)(6), and to "servicing" under General Prohibition 10?
3. Is a blanket policy of refusing China/D:5-headquartered or -owned customers lawful and sufficient, and how deep must ownership checks go for a company my size?
4. What end-use certificate and contract clauses should I use, and what should I require from suppliers about chip provenance?
5. If the IaaS KYC rule or RASA is enacted, would a broker/reseller be covered?
6. Do Montenegrin or EU dual-use rules add anything?

## Sources
1. 15 CFR §772.1, definitions of "Knowledge" and "U.S. person" — https://www.law.cornell.edu/cfr/text/15/772.1 — checked 2026-11-09
2. 15 CFR §764.2 (violations: causing, aiding, abetting, acting with knowledge) — https://www.ecfr.gov/current/title-15/section-764.2 — cited from knowledge of the regulation; page not retrievable this session (**unverified text**)
3. 15 CFR §736.2(b)(10), General Prohibition Ten — https://www.ecfr.gov/current/title-15/section-736.2 — as above (**unverified text**); corroborated by [16]
4. BIS advisory opinions index (2009/2011/2014 cloud opinions) — https://www.bis.gov/advisory-opinions — via [5], checked 2026-11-09
5. Latham & Watkins, "What the Remote Access Security Act Means for Export Controls Compliance Programs" (20 Mar 2026) — https://www.lw.com/en/insights/what-the-remote-access-security-act-means-for-export-controls-compliance-programs — checked 2026-11-09
6. Freshfields, "Remote Access or Remote Possibility? RASA and the Future of Cloud Export Controls" (30 Jul 2026) — https://www.freshfields.com/en/our-thinking/blogs/a-fresh-take/remote-access-or-remote-possibility-rasa-and-the-future-of-cloud-export-controls-102nfbw — checked 2026-11-09
7. 15 CFR §744.6 — https://www.law.cornell.edu/cfr/text/15/744.6 — checked 2026-11-09
8. BIS, Policy Statement on Controls that May Apply to Advanced Computing ICs… Used to Train AI Models (13 May 2025) — https://www.bis.gov/media/documents/ai-policy-statement-training-ai-models-may-13-2025 — read in full 2026-11-09
9. BIS, Guidance Regarding Enforcement of License Requirements for Advanced Computing Items for Entities Headquartered in Country Group D:5 and Macau (31 May 2026) — https://www.bis.gov/media/documents/bis-guidance-may-31-2026.pdf — read in full 2026-11-09
10. CNBC, "Chinese AI lab Moonshot turned to Europe for Nvidia Blackwell access…" (5 Nov 2026) — https://www.cnbc.com/2026/11/05/moonshot-ai-nvidia-chips-europe-china.html — checked 2026-11-09
11. Bloomberg report of US review of Chinese firms' overseas data-centre access (7 Aug 2026), via secondary summary — https://www.kucoin.com/news/flash/us-reviews-chinese-ai-firms-access-to-nvidia-chips-via-overseas-data-centers — checked 2026-11-09 (**secondary; unverified**)
12. CRS, "FY2027 NDAA: Status of Legislative Activity" — https://www.congress.gov/crs-product/IN12704 ; ARI, "Senate NDAA Takes Major Step…" — https://ari.us/senate-ndaa-takes-major-step-to-strengthen-ai-chip-export-controls/ — search summaries only, checked 2026-11-09
13. Akin Gump, "Commerce Issues Proposed Rule on 'Malicious Cyber-Enabled Activities' and AI" (2024) — https://www.akingump.com/en/insights/alerts/commerce-issues-proposed-rule-on-malicious-cyber-enabled-activities-and-artificial-intelligence — checked 2026-11-09
14. BIS, Enforcement — Penalties — https://www.bis.gov/enforcement/penalties — checked 2026-11-09
15. BIS, Industry Guidance to Prevent Diversion of Advanced Computing ICs (13 May 2025) — https://www.bis.gov/media/documents/si-counter-diversion-industry-guidance-may-13-2025.pdf — read in full 2026-11-09
16. Greenberg Traurig, "Navigating GPU Export Controls and AI Use Restrictions in Data Center Operations" (22 Sep 2026) — https://www.gtlaw.com/en/insights/2026/9/navigating-gpu-export-controls-and-ai-use-restrictions-in-data-center-operations — checked 2026-11-09
17. Morrison Foerster, "Managing Export Control Risks in the AI Chip Ecosystem" (9 Feb 2026) — https://www.mofo.com/resources/insights/260209-managing-export-control-risks-in-the-ai-chip-ecosystem — checked 2026-11-09
18. BIS final rule, "Revision to License Review Policy for Advanced Computing Commodities", 91 FR 1684 (15 Jan 2026) — https://www.govinfo.gov/content/pkg/FR-2026-01-15/html/2026-00789.htm — checked 2026-11-09
19. Nixon Peabody, "BIS formally suspends the Affiliates Rule until January 10, 2027" (6 Nov 2026) — https://www.nixonpeabody.com/insights/alerts/2026/11/06/bis-formally-suspends-the-affiliates-rule-until-january-10-2027 ; Baker McKenzie — https://sanctionsnews.bakermckenzie.com/bis-extends-suspension-of-the-affiliates-rule-through-january-10-2027/ — search summaries, checked 2026-11-09
20. Supplement No. 3 to 15 CFR Part 732 (Know Your Customer guidance and red flags) — https://www.ecfr.gov/current/title-15/part-732 — page not retrievable this session; described via [8] and [15]
21. Federal Register, "Inflation Adjustments for Civil Money Penalties" (13 Jul 2026), noting OMB cancelled 2026 adjustments — https://www.federalregister.gov/documents/2026/07/13/2026-14060/inflation-adjustments-for-civil-money-penalties — search summary, checked 2026-11-09
22. Crowell & Moring, "BIS Confirms Advanced Chip License Requirements Extend to D:5 and Macau-Headquartered Entities Worldwide" (4 Jun 2026) — https://www.cmtradelaw.com/2026/06/bis-confirms-advanced-chip-license-requirements-extend-to-d5-and-macau-headquartered-entities-worldwide/ — checked 2026-11-09
