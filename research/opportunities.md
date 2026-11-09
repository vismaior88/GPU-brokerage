# Further business opportunities around GPU brokerage (kickoff brief, section 5)
_Last checked: 2026-11-09_

## Summary

- **Best add-ons to do now (cost almost nothing, low compliance risk):** (a) a South-East Europe (SEE) regional niche, using Serbian/English and local presence; (b) paid procurement advisory (sourcing, benchmarking, contract review) sold as a fixed fee; (c) a free weekly price/market note that later becomes a paid report. These three reinforce the core referral/broker business rather than distract from it.
- **Worth doing opportunistically, by referral only:** colocation referrals (operators publish programs paying 2–15% of monthly revenue or 3% of contract value [22][23]) and introductions of idle reserved capacity, but only where the original supplier consents in writing.
- **Later, once there is a track record:** inference-overflow brokerage, crypto-miner hosting introductions, GPU financing introductions. All three need credibility, technical depth or legal clearance the founder does not have on day one.
- **Avoid:** trading physical GPUs/servers (needs capital, and it is where export-control enforcement is concentrated [9][10]) and anything touching compute futures or swaps (regulated activity; and the contracts are not even trading yet).
- **Compute futures are NOT live as of today.** CME/Silicon Data announced in May 2026 and targeted 5 October 2026, but missed that date; the CFTC extended its review to 9 November 2026 and a secondary report says it has slipped again to January 2027 [1][2][3][4]. ICE/Ornn has no listing date [5]. The founder's note "launched May 2026" is wrong: May was the announcement.
- **The big-miner story is closed to a small broker.** Listed miners have signed $70–150bn of AI leases directly with Microsoft, AWS, Google-backed Fluidstack, CoreWeave and AMD [12][13]. Any role is with small, unlisted operators, and their problem is usually facility quality, not lack of a salesperson.
- **SEE has real, new, commercial supply to represent:** Orion telekom's AI Factory in Belgrade (NVIDIA B200) [16][17], ClusterPower in Romania [20], Synteq HPC in Sofia [21], plus public AI Factories (Slovenia, Bulgaria, Greece, Romania) and Serbia's antenna (SAIFA) that cannot be brokered but are useful to mention [14][15]. Montenegro has no GPU supply to broker [19].
- **New competitor to know about:** NVIDIA runs its own verified matching marketplace between buyers and NVIDIA Cloud Partners [30]. Together with SF Compute, Compute Exchange and BGC, the "pure matching" layer is getting crowded; the founder's edge has to be service, language and region, not a listing site.

## Details

Scoring and verdict terms: **Do now** = start within the first 90 days; **Later** = revisit after 3–5 closed deals; **Avoid** = do not pursue with current resources.

### 1. Secondary physical hardware (used H100s/servers) vs compute-time brokerage

**How it works.** Neoclouds, enterprises and failed projects sell retired GPU servers through IT-asset-disposal (ITAD) firms and specialist brokers. A broker either buys and resells (needs capital) or matches buyer and seller for a commission.

**Who does it.** BuySellRam (cluster liquidation) [8], American Compute (appraisals) [7], Compute Exchange, which opened a secondary market for used H100/A100 in July 2026 [6][8], plus general ITAD firms.

**Money and deal sizes.** Vendor/broker sources (not audited) put a used 8-GPU H100 server at roughly $150,000–$195,000 against $250,000–$320,000 new; one appraiser reports typical realised single-card sales around $14,250 and projects H100 value falling to 5–7% of list by 2028 [7][8]. Warranties on used units are short (30–365 days) [8]. Commission rates for hardware brokers: **(unverified)**.

**Risks.**
- *Export controls are far heavier than for compute time.* A physical advanced chip is a controlled item under the US Export Administration Regulations wherever it is in the world; every re-export or transfer needs classification, destination and end-user checks, and sometimes a licence. BIS's May 2025 guidance lists red flags aimed squarely at hardware resale (middlemen, residential addresses, refusal to disclose installation address, buyers without data-centre infrastructure) and uses the full "knowledge" standard, which includes ignoring a high probability of diversion [9]. BIS's own reporting describes cases of servers routed through intermediaries in South-East Asia [10]. Brokers and resellers are exactly who gets investigated.
- Rules are moving: BIS changed China licence policy in January 2026 and withdrew a broader interim rule in 2026 pending a replacement [10][11]. A solo founder cannot track this safely.
- Fraud (relabelled or damaged cards), fast depreciation, shipping/customs, VAT on goods, no warranty.
- Capital: one server is 75–100 times the founder's whole budget.

**Verdict: Avoid.** Highest capital need and highest legal exposure of all ten options. If a client asks, refer them to an established ITAD firm and take no fee unless a lawyer has cleared the structure.

### 2. Brokering idle reserved capacity (subleasing / resale)

**How it works.** A company that reserved a cluster for 12–36 months and no longer needs all of it wants to recover cost. Options: resell on a marketplace, sublease to a third party, or ask the provider to reassign the contract.

**Who does it.** SF Compute is the main example: customers resell unused reserved time on its market; SF Compute deducts a platform fee (a fixed part plus a percentage, not published, can vary by customer) and pays the seller in **platform credits, not cash** [24]. BGC Group launched "Compute Infrastructure Markets" in June 2026 for over-the-counter trading of compute and memory capacity [3][25]. Compute Exchange runs auctions for reserved capacity [6]. Fluence launched reserved-cluster auctions in September 2026 [26] (vendor source).

**Money.** Seller recovers part of sunk cost; intermediary takes a fee. A broker could charge the seller a success fee. Typical percentages for off-platform subleases: **(unverified)**. SF Compute claims customers recover about 25% of spend on average by reselling [24] (company claim).

**Risks.**
- *Contract restrictions are the whole problem.* Whether a reservation can be assigned or subleased "sits in the contract"; hyperscalers document no resale route for commitments or AWS Capacity Blocks [26] (vendor guide, secondary). Assume assignment and sublease are prohibited without supplier consent until the contract says otherwise.
- KYC is transferred to you in practice: the original supplier screened the first tenant, not the subtenant. A sublease to an unscreened party is a diversion red flag.
- Who is liable for uptime, data deletion between tenants, and payment default? Usually unclear.
- You compete with a funded marketplace (SF Compute) and a listed inter-dealer broker (BGC).

**Verdict: Later, and only as a three-party deal** (seller, new user, original supplier consenting in writing and doing its own onboarding of the new user). In that form it is just another sourcing channel for the core brokerage. Never arrange a "quiet" sublease.

### 3. Crypto/bitcoin miners converting to AI hosting

**How it works.** Miners own power connections and land. They either lease powered shells/colocation to AI tenants or buy GPUs and run a cloud themselves.

**Who.** IREN (Microsoft, ~$9.7bn; plus $2.8bn cloud contracts), Core Scientific (CoreWeave; AMD leases), TeraWulf, Cipher Digital (Fluidstack/Google, AWS), Hut 8, Applied Digital. Trackers put total signed AI/HPC contracts by listed miners between $70bn (March 2026) and $114–150bn (August 2026) [12][13].

**What they need.** The large ones do not need customers; they need capital. Conversion costs are quoted at $8–15m per MW and debt loads are heavy [12]. Smaller operators are the ones without tenants, but reports say the reason is site quality: remote locations, retail power prices ($0.12–0.15/kWh) and facilities never built for the density, redundancy and uptime AI tenants require [27] (mixed-quality sources). Tenants "are already waiting" for sites that can prove power and a Tier 3 shell [27].

**Can a small broker help?** Marginally. A small miner with a real GPU fleet and a decent facility is simply another supplier for the core brokerage: sign a referral agreement, verify hard (site evidence, test access, benchmarks). A miner with only power and a shed needs engineering and capital, not introductions.

**Risks.** Unproven operators, weak SLAs, counterparty insolvency, some sites in higher-risk jurisdictions. Hosting deals are multi-megawatt and negotiated by specialist data-centre brokers.

**Verdict: Later.** Do not chase miners as a segment. Add vetted small miner-clouds to `suppliers.csv` when they appear.

### 4. Regional and sovereign compute demand

**Global picture.** Deloitte expects over $100bn committed to sovereign AI compute in 2026 [28]. Saudi Arabia's HUMAIN and the UAE's G42/Khazna are building at very large scale; India's IndiaAI Mission subsidises GPU access through tenders; Cassava is building Africa's first NVIDIA-based AI factory in South Africa; Brazil has a national AI plan [28] (several of these figures come via secondary sources; treat as indicative).

**Honest read for a solo founder.** Gulf, India and Brazil deals are government-to-vendor, tender-driven, in the hundreds of millions, and local presence matters. The Gulf also carries the highest export-control sensitivity of any non-embargoed region. A cold-start broker in Montenegro has no edge there. **Avoid as a target market** for now; serve inbound buyers from these regions only after full KYC.

**South-East Europe: the one region where the founder has an edge.**

| Country | What exists (Nov 2026) | Brokerable? |
|---|---|---|
| Serbia | **Orion telekom AI Factory**, Belgrade: commercial GPU-as-a-Service on NVIDIA DGX B200, described as phase one of a larger sovereign AI Factory [16][17]. Third-party trackers list about $7.94/GPU-hour reserved and ~$9.92 on-demand for B200 [17] (aggregator data, confirm with Orion). | **Yes – commercial supplier.** Partner/reseller terms: (unverified). |
| Serbia | State Data Centre Kragujevac hosts the National AI Platform; €50m Eviden contract for a National AI Factory (BullSequana XH3000, ~300 GPUs) [18]. **SAIFA** EuroHPC antenna, kicked off 14 May 2026, runs 2026–2028, linked to Greece's Pharos [14][15]. | No – public allocation. Useful to point startups and researchers to. |
| Montenegro | No commercial GPU capacity found. State data centre being built by 4iG; energy utilities planning their own data centre in Nikšić; PM talks of "green data centres"; national AI strategy 2026–2030 in drafting [19]. | Nothing to broker. Possible demand side (government, telecoms, banks) later. |
| Croatia | **Pantheon AI**, Topusko: announced April 2026, 1 GW campus, "€50bn" headline (one outlet cites €12bn); company press-release based, target 2027 [29]. No Croatian EuroHPC AI Factory found (unverified). | Not yet – announcement, not capacity. Watch. |
| Slovenia | SLAIF EuroHPC AI Factory [14]. | No – public. |
| Greece | Pharos AI Factory on the DAEDALUS supercomputer, inaugurated October 2026; Kiefer (private) running DGX B200 for its own model work [15][31]. | Mostly no. |
| Bulgaria | BRAIN++ AI Factory (€90m, Sofia Tech Park); **Synteq HPC** opened a Sofia site (RTX-class GPUs); 9 GW of grid requests for data centres; IBM "gigafactory" talks at proposal stage [21][32]. | Synteq – yes, small scale. |
| Romania | **ClusterPower** (NVIDIA DGX-based, sells dedicated/reserved AI infrastructure; Hong Kong-based AIC took a stake in January 2026 for an 800 MW build-out); RO AI Factory (public) [14][20]. | Yes – commercial supplier. Note the Hong Kong investor in supplier due diligence. |

**How the money flows.** Same as the core business: referral commission from the local supplier, or a buyer-paid sourcing fee. The regional angle adds two services nobody global offers: (1) guiding local startups and universities to free public compute (SAIFA, Pharos, SLAIF, BRAIN++) and then to paid capacity when they outgrow it; (2) bringing EU buyers who want EU or near-EU hosting to SEE suppliers. Note Serbia and Montenegro are **outside the EU**: do not sell Serbian hosting as "EU data residency".

**Risks.** Small market (few buyers needing 8+ GPUs), suppliers few enough that buyers can call them directly, regional prices that look high against global neoclouds (Orion's listed B200 rate is well above the ~$3 H100 benchmark, though it is a different, newer chip).

**Verdict: Do now** as the positioning niche, not as a separate business. Be the known Serbian/English-speaking compute person in the region.

### 5. Inference-capacity brokerage (overflow for model providers)

**How it works.** Inference platforms and AI-application companies need extra GPUs quickly when traffic spikes or a model launch lands; a broker finds short-term dedicated capacity.

**Who does it.** Aggregators such as Shadeform route across many clouds [33]; SF Compute sells by the hour; NVIDIA's own matching system connects buyers to NVIDIA Cloud Partners [30]; neoclouds sell direct. I found **no public evidence** of how Together, Fireworks, Baseten or OpenRouter buy overflow, or that they use human brokers (unverified).

**Money.** Commission or margin on short reservations. Inference is said to be heading to ~70% of GPU-cloud spend by late 2026 [33] (vendor estimate). Capacity through late summer 2026 was reported as sold out in advance [33], so real overflow supply is scarce.

**Risks.** Buyers are sophisticated, want capacity in hours via API, need specific regions, latency and compliance (SOC 2, data handling). A solo non-engineer cannot support production inference incidents. Marketplaces do this better.

**Verdict: Later.** Take inference requests as normal brokerage deals (a reserved baseline of 8–64 GPUs is a perfectly good deal). Do not build a specialised "overflow desk".

### 6. Compute futures and hedging

**Status on 9 November 2026.**
- **CME / Silicon Data:** announced 12 May 2026; on 11 August set a 5 October 2026 start for H100 and B200 Rental Index futures (730 GPU-hours per contract, cash-settled) "pending regulatory review" [1][2]. CME missed 5 October. On 21 September the CFTC extended its review of the NYMEX filing by 45 days to **9 November**, citing "novel or complex issues" [3]. A secondary report (citing The Information) says CME agreed to a further 60-day extension, pointing to **January 2027** [4] – not confirmed against a CFTC document.
- **ICE / Ornn:** announced 19 May 2026. ICE's 29 September notice names OCPI H100 and B200 futures as first contracts but states **no listing date** [5].
- **Others:** Nodal Exchange (Compute Desk indexes) and Architect are also waiting. As of 21 October, "no US exchange has been cleared to list them" [3]. The CFTC's public consultation on compute derivatives closed on 20 October [3].
- **Brokers positioning:** BGC (OTC desk since June 2026), ADM Investor Services, Nanhua USA [3][25].

**Is there a role for a small unlicensed intermediary? No.** Under US law, a person who solicits or accepts orders for futures or swaps must register as an introducing broker with the CFTC and join the NFA; advising others on trading futures for pay generally triggers commodity trading advisor rules [34]. Arranging OTC compute swaps is the same territory. Penalties for acting unregistered: not researched in detail – ask a lawyer before going near this.

**What the founder can legitimately do:** read the free index data as a pricing reference for quotes, and mention to large buyers that hedging tools are coming, without recommending trades.

**Verdict: Avoid** as a business. Use the indexes as information only.

### 7. GPU financing introductions

**How it works.** GPU owners borrow against hardware plus customer contracts. Large deals: Magnetar/Blackstone-led private credit to CoreWeave SPVs; Macquarie-led $500m vehicle for Lambda (2024); Lambda's $926m investment-grade term loan; CoreWeave's $8.5bn A3-rated facility (March 2026) [35][36]. Pricing fell from about 14% in 2023 to SOFR+225 for the best credits [35] (commentary source).

**Small-ticket end (what a finder could touch).** American Compute, itself an intermediary that screens financing requests for lenders, lists USD.AI as the only lender with public sub-$20m GPU loans (12 loans, $200k–$16.4m), plus Sandton Capital ($5–150m) and Upper90 ($5–25m initial). Reported terms: 7–9% with investment-grade offtake, 10–12% with multi-year non-investment-grade offtake, 12–15% for spot-rental borrowers; up to 80% loan-to-value; 3–5 year tenor; minimum 1.15x debt-service cover [37] (single intermediary source, dated 10 October 2026). Lenders generally want a signed multi-year offtake contract [36].

**Do lenders pay finder fees?** I found **no published referral or finder programme** from any GPU lender (unverified either way). Equipment-finance brokers typically earn a percentage of the funded amount, but I have no verified GPU-specific figure.

**Licensing issues.** California already requires a licence to broker loans under its Financing Law, and a new law (AB 2116, signed 30 September 2026) extends licensing to commercial-financing brokers from 1 July 2028 [38]. Other US states and EU countries have their own rules. If a deal involves notes, SPV interests or equity, being paid a success fee can require securities broker-dealer registration. This must be cleared by a US lawyer before taking any fee.

**The real opening is indirect:** lenders need offtake contracts; a broker who brings a creditworthy multi-year buyer to a small neocloud is making that neocloud financeable. That is the core brokerage business, paid as a normal commission.

**Verdict: Later** (and only as flat-fee, lawyer-cleared introductions). Not a first-year income line.

### 8. Colocation and power brokerage

**How it works.** GPU owners (small neoclouds, enterprises with their own servers) need high-density rack space and power. Operators pay channel partners for referred customers.

**Who does it / what they pay (published programmes).**
- **Centersquare:** 12–15% of monthly eligible revenue up to 500 kW, 10% for 501–999 kW, 4% for 1–5 MW, 2% above 5 MW; 12-month minimum term; paid monthly [22].
- **DC BLOX:** one-time 3% of total contract value; deals above 18 cabinets or ~200 kW need a separately negotiated agreement [23].
- **Colo Solutions, TRG Datacenters, CoreSite:** one-time or residual commission options [23].
- Large commercial real-estate and telecom-agent firms dominate multi-megawatt deals (named firms not verified in this research).

**Money.** Recurring commission from the operator; the buyer usually pays nothing. A 200 kW AI deployment can produce a meaningful monthly residual, but figures depend on $/kW rates I did not verify.

**Risks.** AI-density space (liquid cooling, 50 kW+ per rack) is scarce; operators may not need a referrer for it. Deals are slow (months) and technical. Low compliance risk compared with hardware, but location still matters (do not help place controlled hardware in a risky jurisdiction or for an unscreened owner). Pure electricity brokerage is a separate, often licensed, energy-market activity – out of scope.

**Verdict: Later / opportunistic.** Sign one or two free colocation referral agreements once a real request appears; do not prospect for it.

### 9. Software and data tools a broker could sell later

| Tool | Who already does it | Realistic for the founder? |
|---|---|---|
| **Price tracker / index** | Silicon Data ($30.5m Series A; daily indexes on Bloomberg; enterprise subscription, redistribution licensed separately), Ornn (transaction-based OCPI, on Bloomberg), Compute Desk, SemiAnalysis; free list-price indexes from GetDeploying and GPUPerHour (CC BY 4.0) [39][40]. | **No.** Free and funded versions exist. Use them, cite them, do not rebuild them. |
| **Benchmarking / hardware verification** | American Compute (appraisals, diligence) [37]; providers' own tools. | Not as software. As a **service inside advisory** (run a scripted acceptance test with the buyer's engineer) – yes, later, with a freelance engineer. |
| **Procurement platform / marketplace** | SF Compute, Compute Exchange, Shadeform, Vast.ai, NVIDIA's matching system [6][24][30][33]. | **No.** Needs engineering and liquidity. |
| **Newsletter / market report** | Index providers publish blogs; few cover SEE or the small-buyer view. | **Yes.** Free to produce, builds the audience and credibility the brokerage needs. Check each data source's licence before republishing (Silicon Data restricts redistribution [39]; GPUPerHour's is open with attribution [40]). |

**Verdict: Do now** for a free newsletter (as marketing); **Later** for a paid regional report; **Avoid** building tracker or platform software.

### 10. Paid advisory / procurement consulting

**How it works.** The buyer pays a fixed or retainer fee for: requirements definition, a supplier long-list, running a mini-RFP, comparing quotes like-for-like, checking contract terms (term length, exit and reallocation rights, SLA credits, GPU-generation lock-in), and judging supplier solvency. Commentary in 2026 stresses that provider balance sheet and exit terms now matter as much as price; Gartner is cited as forecasting that over 80% of neoclouds will stop operating independently by 2030 [41].

**Who does it.** I found software-contract negotiation boutiques writing about AI compute and vendor guides, but **no dominant named GPU-procurement advisory firm and no published fee levels** (unverified) [41]. That absence is either a gap or a sign buyers do not yet pay for it; the founder should test with real offers.

**Money.** Buyer pays directly: a fixed project fee, or a share of documented savings. No supplier dependence, paid even if the buyer goes direct afterwards. This is revenue model 2/3 from the kickoff brief and the cleanest protection against being bypassed.

**Risks.** Credibility (cold start, non-engineer) – mitigate with a narrow scope, sample deliverables and a freelance technical reviewer. Liability for advice – cap it in the contract and state clearly that this is not legal advice. Conflict of interest if also taking supplier commission – disclose in writing every time, or rebate the commission.

**Verdict: Do now**, as a small fixed-price "sourcing sprint" offered alongside free referral-based sourcing.

### Other opportunities noticed

- **Public-compute navigation for SEE startups and researchers** (helping them apply to SAIFA/Pharos/EuroHPC calls). Cannot be brokered, and charging for access would be inappropriate, but a paid application-support service or free help as lead generation is legitimate. Do now as lead generation.
- **Supplier-side sales agent for one or two regional suppliers** (e.g. representing a SEE provider to Western buyers on commission). Same legal form as a referral agreement, more focus. Later, once a supplier relationship exists.
- **Supplier due-diligence reports for buyers** (ownership, sanctions screening, data-centre location, financial health) sold as a fixed-fee add-on. Fits the compliance work the founder must do anyway. Later.

### Ranking table

Scores 1–5. **For cost and risk, 5 is best (cheapest / safest)** so a higher total is better.

| # | Opportunity | Potential | Startup cost | Risk | Solo fit | Total | Verdict |
|---|---|---|---|---|---|---|---|
| 4 | SEE regional niche (positioning) | 3 | 5 | 4 | 5 | **17** | Do now |
| 10 | Paid advisory / procurement sprint | 3 | 5 | 4 | 4 | **16** | Do now |
| 9 | Newsletter / market note (not software) | 2 | 5 | 5 | 4 | **16** | Do now |
| 8 | Colocation referrals | 3 | 5 | 4 | 3 | **15** | Later / opportunistic |
| 2 | Idle reserved capacity (with supplier consent) | 3 | 4 | 3 | 3 | **13** | Later |
| 5 | Inference-overflow brokerage | 3 | 4 | 3 | 2 | **12** | Later |
| 3 | Small miner-clouds as suppliers | 2 | 5 | 3 | 2 | **12** | Later |
| 7 | GPU financing introductions | 3 | 4 | 2 | 2 | **11** | Later (lawyer first) |
| 4b | Gulf / India / LatAm / Africa sovereign deals | 4 | 2 | 2 | 1 | **9** | Avoid for now |
| 1 | Physical used hardware | 4 | 1 | 1 | 1 | **7** | Avoid |
| 6 | Compute futures / hedging intermediary | 2 | 1 | 1 | 1 | **5** | Avoid |

Scores are my judgement from the evidence above, not measured data.

### What I would do in the founder's place

I would not open any second business line in the first six months. I would run one business with three faces: free, commission-funded sourcing as the door-opener; a small fixed-fee "sourcing sprint" for buyers who want an independent comparison and contract check; and a short weekly note in English (with a Serbian edition) on GPU prices and SEE supply, citing the free indexes. I would make Orion telekom, ClusterPower and Synteq early supplier conversations alongside the global neoclouds, and use SAIFA and the regional AI Factories as free, helpful advice that earns trust with local startups and universities. I would say no, politely and in writing, to anyone asking me to find or sell physical GPUs, to sublease capacity without the supplier's consent, or to "hedge" compute for them. Colocation, financing and miner introductions I would keep as a list of contacts to pass on, taking a fee only after a lawyer has confirmed I may. The honest weak point is demand: SEE has few buyers needing more than a handful of GPUs, so the region is a credibility base and a supply story, while most paying buyers will still come from Western Europe and the US.

## Questions for a lawyer / accountant

1. If I introduce a GPU owner to a lender and receive a success fee, do I need a loan-broker licence (e.g. California Financing Law, incl. AB 2116 from July 2028) or securities broker-dealer registration? Is a flat, non-contingent fee safer?
2. Does introducing a buyer to a broker or exchange for compute futures or OTC compute swaps, or writing about hedging in a newsletter, risk "introducing broker" or "commodity trading advisor" status with the CFTC?
3. If I arrange a transfer of reserved capacity between two companies with the supplier's consent, who carries export-control/KYC responsibility, and what should my contract say?
4. If I ever match a buyer and seller of physical servers without touching the goods or the money, am I still exposed under the EAR (e.g. General Prohibition 10, "knowledge" standard)? (My working assumption: yes – hence "Avoid".)
5. For paid advisory: what liability cap and disclaimers are enforceable for a US LLC selling to EU and Serbian clients, and how must supplier commissions be disclosed?
6. Are colocation referral commissions from US operators US-source income for a non-resident-owned LLC? (accountant)
7. Can I republish index values (Ornn, Silicon Data, GetDeploying, GPUPerHour) in a newsletter, and under what licence terms?

## Sources

All checked 2026-11-09.

1. CME Group press release, "CME Group and Silicon Data Partner to Launch First Compute Futures" (12 May 2026) – https://www.cmegroup.com/content/cmegroup/en/media-room/press-releases/2026/5/12/cme_group_and_silicondatapartnertolaunchfirstcomputefutures.html
2. CME investor relations, 5 October 2026 launch announcement (11 Aug 2026) – https://investor.cmegroup.com/node/55686 ; The Next Web summary – https://thenextweb.com/news/cme-silicon-data-gpu-compute-futures-october-5
3. Finance Magnates, "Brokers Prepare for AI Computing Futures as US Regulator Closes Comment Window" (21 Oct 2026) – https://financemagnates.com/institutional-forex/brokers-prepare-for-ai-computing-futures-as-us-regulator-closes-comment-window
4. FourWeekMBA, "CME Delays Nvidia GPU Rental Futures Again, to January" (secondary, cites The Information) – https://fourweekmba.com/ai-cme-delays-nvidia-gpu-rental-futures-again-to-january/ ; CME NYMEX submission 26-370 – https://www.cmegroup.com/content/dam/cmegroup/market-regulation/rule-filings/2026/8/26-370.pdf
5. ICE Futures US exchange notice, Ornn compute (29 Sep 2026) – https://www.ice.com/publicdocs/futures_us/exchange_notices/ICE_Futures_US_Exchange_Notice_ORNN_Compute_4Q2026_20260929.pdf ; ICE press release (19 May 2026) – https://ir.theice.com/press/news-details/2026/ICE-and-Ornn-to-Launch-GPU-Compute-Futures-Contracts/default.aspx
6. Blockspace, "Compute Exchange launches used GPU marketplace" (page not readable directly; via search summary) – https://blockspace.media/insight/compute-exchange-launches-used-gpu-marketplace/ ; Finextra on Compute Exchange – https://finextra.com/pressarticle/104103/compute-exchange-opens-market-for-buying-and-selling-computer-power
7. American Compute, H100 appraisal – https://www.amcompute.com/appraisals/h100
8. Hashrate Index, used GPU market pricing – https://hashrateindex.com/blog/used-gpu-market-pricing-deprecation-secondary-ai/ ; BuySellRam, cluster liquidation – https://www.buysellram.com/blog/nvidia-a100-h100-h200-cluster-liquidation-maximize-roi-and-asset-recovery/ ; Introl, secondary GPU markets guide – https://introl.com/blog/secondary-gpu-markets-buying-selling-used-hardware-guide-2025
9. Arnold & Porter on BIS May 2025 guidance and red flags – https://www.arnoldporter.com/en/perspectives/advisories/2025/05/commerce-new-guidance-curb-adversaries-access-to-advanced-ai-tech ; Mayer Brown – https://www.mayerbrown.com/en/insights/publications/2025/05/us-commerce-department-announces-new-export-compliance-expectations-related-to-artificial-intelligence
10. BIS FY2025 Annual Report – https://www.bis.gov/media/documents/fy2025-bis-annual-report.pdf ; Sandler Travis, "BIS to rescind rule on export controls for AI chips" – https://www.strtrade.com/trade-news-resources/str-trade-report/trade-report/may/bis-to-rescind-rule-on-export-controls-for-ai-chips
11. Covington, BIS revised licence review policy for China/Macau (Jan 2026) – https://www.cov.com/en/news-and-insights/insights/2026/01/us-commerce-department-revises-license-review-policy-for-exports-of-certain-advanced-computing-commodities-to-china-and-macau
12. Cointelegraph, "Hut 8, IREN deals lift AI-focused bitcoin mining stocks" – https://cointelegraph.com/news/hut-8-iren-deals-lift-ai-focused-bitcoin-mining-stocks ; Let's Data Science, "$70 billion in contracts" – https://letsdatascience.com/news/bitcoin-miners-pivot-to-ai-with-70-billion-in-contracts-7c4c0706
13. Forklog, miners shift to AI – https://forklog.com/en/news/bitcoin-miners-shift-to-ai-amid-profitability-pressure (the $114bn Sandmark and $150bn Bernstein tallies came via search summaries of aggregator pages; treat as indicative)
14. EuroHPC JU, AI Factory Antennas – https://www.eurohpc-ju.europa.eu/ai-factory-antennas_en ; selection announcement (13 Oct 2025) – https://www.eurohpc-ju.europa.eu/eurohpc-ju-selects-ai-factory-antennas-broaden-ai-factories-initiative-2025-10-13_en ; Slovenia government on SLAIF – https://www.gov.si/en/news/2025-03-12-slovenia-among-the-digital-giants-a-new-supercomputer-and-ai-factory-to-boost-technological-power/
15. Institute of Physics Belgrade, "SAIFA project officially launched" – https://hpc.ipb.ac.rs/news/saifa-project-officially-launched ; Institute Mihajlo Pupin, SAIFA – https://www.pupin.rs/naucnoistrazivacki-projekti/evropski-ni-projekti/saifa/
16. Orion telekom, "Orion telekom launches a sovereign AI Factory" (page returned an error on direct fetch; via search summary) – https://oriontelekom.rs/orion-telekom-launches-a-sovereign-ai-factory/ ; Biznis.rs – https://biznis.rs/biznis/orion-telekom-i-nvidia-grade-novu-ai-infrastrukturu-u-srbiji/
17. GetDeploying, Orion AI Factory listing (prices) – https://getdeploying.com/orion-ai-factory
18. Scientific Computing World, Eviden €50m Serbia National AI Factory – https://www.scientific-computing.com/article/eviden-signs-50-million-euro-contract-build-serbias-national-ai-factory ; Serbian Office for IT and eGovernment, Kragujevac data centre – https://www.ite.gov.rs/tekst/en/35/government-data-centredr-location-in-kragujevac.php
19. Balkan Green Energy News, Montenegrin utilities' data centre – https://balkangreenenergynews.com/montenegrin-energy-utilities-plan-joint-data-center/ ; "green data centers" – https://balkangreenenergynews.com/spajic-montenegro-wants-to-be-country-of-green-data-centers/ ; TelcoTitans, 4iG state data centre – https://www.telcotitans.com/infrawatch/4ig-lands-deal-to-build-montenegrin-gov-backed-data-centre/10319.article
20. Baxtel, AIC–ClusterPower 800 MW – https://baxtel.com/news/aic-partners-with-romania-s-clusterpower-on-800mw-data-center-build-out-2026-01-05 ; btw.media on ClusterPower – https://btw.media/en/cluster-power-reserves-the-megawatt-before-the-rack
21. Blackridge Research, Synteq HPC Sofia – https://www.blackridgeresearch.com/news-releases/crunchbits-rebrands-as-synteq-hpc-launches-dallas-sofia-data-centers ; CMS, data centres in Bulgaria – https://cms.law/en/bgr/legal-updates/data-centres-in-bulgaria-what-ai-offtakers-expect-from-developers
22. Centersquare Referral Partner Program Guide – https://csquare.com/hubfs/CenterSquare/docs/Centersquare_ReferralPartnerProgramGuide.pdf
23. DC BLOX referral programme – https://www.dcblox.com/referral-program/ ; Colo Solutions – https://www.colosolutions.com/partner-and-referral-program/ ; CoreSite channel brochure – https://www.coresite.com/hubfs/-website-documents/product-brochures/CoreSite_Why-CoreSite_Channel.pdf
24. SF Compute docs, reselling – https://docs.sfcompute.com/preview/guides/reselling ; SF Compute, realised discount – https://sfcompute.com/news/realized-discount
25. Markets Media, "BGC Group launches Compute Infrastructure Markets" – https://www.marketsmedia.com/bgc-group-launches-compute-infrastructure-markets/
26. Spheron (vendor), reserved GPU contracts and resale routes – https://www.spheron.network/blog/reserved-gpu-bidding-on-spheron-capacity-blocks-and-msas-202/ ; Fluence auctions report – https://book.st-hakky.com/en/news/fluence-gpu-auction-price-discovery
27. Cointelegraph Magazine, miners and AI data centres – https://cointelegraph.com/magazine/bitcoin-miners-ai-data-centers-power-infrastructure ; Hackernoon, miner-to-GPU migration – https://hackernoon.com/the-great-pivot-in-mining-inside-the-miner-to-gpu-migration
28. Deloitte TMT Predictions 2026, tech sovereignty – https://www.deloitte.com/global/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/tech-sovereignty.html ; PwC Strategy&, GCC compute sovereignty – https://www.strategyand.pwc.com/m1/en/industries/technology/gcc-compute-sovereignty.html ; IFC, data centre and AI investment in emerging markets – https://www.ifc.org/content/dam/ifc/doc/2026/data-center-and-ai-investment-in-emerging-markets.pdf
29. Capacity, Pantheon AI Croatia campus – https://capacityglobal.com/news/pantheon-ai-croatia-data-centre-campus/ ; Baxtel (lower figure) – https://baxtel.com/posts/pantheon-plans-behind-the-meter-data-center-development-in-croatia
30. NVIDIA Compute MatchMake System – https://computematch.nvidia.com/
31. Euronews, DAEDALUS inauguration (19 Oct 2026) – https://www.euronews.com/2026/10/19/daedalus-greece-unveils-new-supercomputer-as-it-eyes-role-in-europes-ai-race ; Proto Thema on Kiefer – https://en.protothema.gr/2025/11/08/kiefer-supports-ai-innovation-in-greece-with-nvidia/
32. INSAIT, BRAIN++ AI Factory – https://insait.ai/bulgaria-will-have-its-own-ai-factory-a-project-for-90m-eur/ ; dig.watch, Bulgaria–IBM gigafactory talks – https://dig.watch/updates/bulgaria-eyes-ai-gigafactory-partnership-with-ibm
33. Cerebral Valley on Shadeform – https://cerebralvalley.beehiiv.com/p/gpu-clouds-everywhere-are-sold-out-shadeform-is-building-the-solution ; Spheron (vendor), GPU shortage 2026 – https://www.spheron.network/blog/gpu-shortage-2026/
34. NFA, "Who has to register" – https://www.nfa.futures.org/registration-membership/who-has-to-register/ ; CFTC, FCMs and IBs – https://www.cftc.gov/IndustryOversight/Intermediaries/FCMs/fcmib
35. Wing VC, "How the GPU Became Collateral" – https://www.wing.vc/content/how-the-gpu-became-collateral ; Capacity, CoreWeave debt – https://capacityglobal.com/news/coreweaves-debt-hits-35bn/
36. SemiAnalysis, "How to price a GPU loan" – https://newsletter.semianalysis.com/i/204512487/how-to-price-a-gpu-loan ; StorageNewsletter, Lambda $926m term loan – https://www.storagenewsletter.com/?p=305474
37. American Compute, lenders for GPU deployments under $20m (updated 10 Oct 2026) – https://www.amcompute.com/gpu-debt/lenders-under-20m
38. Holland & Knight, California commercial financing licensing (20 Oct 2026) – https://www.hklaw.com/en/insights/publications/2026/10/california-enacts-commercial-financing-licensing-requirement ; Morrison Foerster – https://www.mofo.com/resources/insights/261015-california-expands-california-financing-law
39. Silicon Data, Silicon Index and data licensing – https://www.silicondata.com/products/silicon-index?gpu=h100 ; https://www.silicondata.com/products/index-datasets
40. GetDeploying GPU price index – https://getdeploying.com/gpu-price-index ; GPUPerHour price index – https://gpuperhour.com/gpu-price-index
41. Capacity, neocloud consolidation explained – https://capacityglobal.com/news/neolcoud-consolidation-explained/ ; PYMNTS, CFOs and neocloud budgets – https://www.pymnts.com/?p=4176594 ; Spheron (vendor), reservation contract negotiation – https://www.spheron.network/blog/gpu-cluster-reservation-contract-negotiation-2026/
