# Market landscape and competitors (Q5, Q3)
_Last checked: 2026-11-09_

## Summary

- **The intermediary layer is crowded and well funded.** Since 2025, venture money has poured into exactly the role the founder wants to play: Andromeda ($1.5B valuation), Hydra Host ($100M Series A), SF Compute ($40M Series A), Ornn ($33M seed, reportedly raising at ~$1B), plus BGC Group's institutional desk. A solo broker cannot compete with these on technology, price discovery, or large deals.
- **Fee levels in the market are visible and set a ceiling.** SF Compute reportedly takes ~10% per transaction; Compute Exchange charges the provider only; Shadeform is described as zero-fee to the buyer (paid by the provider side); Vast.ai and io.net take roughly 0–20% depending on source. A buyer-paid broker fee above ~3–5% on top of a supplier price will be hard to defend when "free to the buyer" alternatives exist.
- **"Transparent fee broker" is already a marketing line** (CheapestGPU uses it word for word), but that site names no people, no fee, and no customers. The idea is not new; credible execution of it is still rare.
- **The market is tight in late 2026**, which changes what buyers need: the problem is less "find the cheapest price" and more "find anyone with real capacity, on acceptable terms, soon". That favours a human who chases supply, but it also means suppliers need brokers less.
- **Real gaps exist, but they are narrow:** (1) mid-size deals (roughly 8–128 GPUs, 3–12 months) that are too big for self-serve marketplaces and too small for the big desks; (2) EU-hosted / sovereignty-sensitive buyers; (3) buyers in the Balkans and wider CEE who are not served by any of the US players and speak the founder's languages; (4) vetting and paperwork (supplier verification, contract comparison, KYC) that platforms do not do for the buyer.
- **Honest answer to Q3:** today the founder has no real advantage. One can be built in 3–6 months from three things: a verified, up-to-date map of who actually has capacity (especially in the EU), speed and care on mid-size deals, and visible independence (disclosed commissions, written comparison of options). Without those, a buyer has no reason not to go direct.
- **Recommendation:** position as an independent sourcing adviser for mid-size, EU/CEE-relevant deals, paid mainly by supplier referral commission and fully disclosed. Do not try to look like a marketplace or an exchange.

## Details

### Q5. Who are the existing brokers and marketplaces?

There are five distinct groups. They are not all direct competitors; some are potential suppliers or data sources.

#### Comparison table

| Player | Type | What it does | How it charges | Funding / scale | Weaknesses (from a small buyer's view) |
|---|---|---|---|---|---|
| **SF Compute** | Marketplace with resale | Sells compute contracts and lets buyers resell unused reserved hours on a live market | Reported ~10% of each transaction [1] | $40M Series A (Nov 2025, DCVC and Wing; ~$300M valuation reported); says it manages >$100M of hardware, several thousand GPUs [1] | US-centric; standardised product; limited choice of location and contract terms; fee figure is from one article and may have changed |
| **Andromeda** | Broker / "market maker for compute" | Aggregates supply from many providers, tests hardware before it goes live | Not disclosed [2] | $1.5B valuation, Paradigm has put in $60M; ~20 staff; aims for up to 100,000 GPUs under management in 2026 [2] | Opaque pricing; aimed at Silicon Valley startups and research teams |
| **Shadeform** | Aggregator, increasingly a wholesale broker | One console and API across ~20+ GPU clouds; now earns much of its revenue structuring large bare-metal cluster deals, notably in Asia-Pacific [3] | Described as no fee to buyer (paid from provider rates); one third-party estimate says 6–12% markup. Conflicting, **(unverified)** [3][4] | Only ~$2M funding as of Nov 2025; 23 providers in testing [3] | No managed Slurm/Kubernetes, no health checks on provider machines (SemiAnalysis review) [3] |
| **Prime Intellect** | "Meta-cloud" plus research lab | Pulls GPU inventory from centralised and decentralised providers into one marketplace | Margin on rentals (marks up) [5] | ~$20M raised (seed + extension led by Founders Fund) [5] | Compute resale is a side business to its own AI research; crypto-adjacent |
| **Hydra Host** | Bare-metal marketplace + operator software (Brokkr) | Software for independent data centres to rent out GPUs, and a marketplace matching owners with renters | Not disclosed [6] | $100M Series A, June 2026 (Kindred, NVIDIA, ARK, Founders Fund and others) [6] | Bare metal only, so the buyer needs its own engineering; wholesale focus |
| **Compute Exchange** | Auction exchange | Periodic auctions of GPU capacity; pricing calculator | Buyers pay nothing; providers pay a commission on completed trades [7] | Claims 80,000+ GPUs in supply "across dozens of providers" (company claim) [7]. No 2026 funding news found | Auction timing does not suit urgent needs; claims are self-reported |
| **Ornn** | Index + marketplace + derivatives | Publishes the Ornn Compute Price Index; marketplace aggregating capacity from large neoclouds; ICE plans futures on its index | Not disclosed | $33M seed June 2026 (a16z crypto); reported to be raising at up to ~$1B valuation [8][9] | Institutional focus; more a data source than a competitor for a small broker |
| **NVIDIA DGX Cloud Lepton** | Vendor-run marketplace | Routes developers to NVIDIA partner clouds through one interface | Providers set prices; no public rate card [10] | NVIDIA-backed; current provider roster **(unverified)** | Limited to NVIDIA's partner set; current status not confirmed from a 2026 primary source |
| **Vast.ai** | Peer-to-peer marketplace | Anyone can list GPUs; cheapest prices, mostly consumer and older data-centre cards | Host fee removed in June 2024 and replaced by an internal surcharge of undisclosed size [11]; third parties estimate 10–15% **(unverified)** | Large long-tail supply | Variable reliability and security; unsuitable for regulated or enterprise buyers; fraud risk on listings |
| **Akash** | Decentralised (crypto) marketplace | Reverse-auction for compute, paid in AKT or stablecoin | Protocol "take rate"; originally 4% (AKT) / 20% (USDC), later proposals cut or remove it. Current rate **(unverified)** [12] | Token network | Crypto payment rails; little enterprise contracting; small buyers need technical skill |
| **io.net** | Decentralised (crypto) marketplace | Aggregates GPUs from many owners | Sources conflict: 0–5% depending on payment method **(unverified)** [13] | Claims ~139,000 GPUs and ~$20M annualised revenue (March 2026, self-reported) [13] | Quality varies; token economics; hard to do KYC on the supply side |
| **Spheron** | Marketplace (crypto origins) | Aggregated GPU rental; very active content marketing | Says "no hidden fees"; no fee schedule found **(unverified)** | Funding not verified | Much of the public "comparison" content about competitors is written by Spheron itself, so treat it as marketing |
| **BGC Compute Infrastructure Markets** | Institutional inter-dealer broker | Launched 18 June 2026 to broker OTC buying, selling and hedging of compute and memory capacity; preparing to broker compute futures [14] | Not disclosed (standard brokerage commission model) | Division of BGC Group (listed global broker) | Serves institutions and large blocks; not interested in a 16-GPU startup deal |
| **Nodestream (Blockware)** | Hardware OTC desk | Brokers physical GPUs and servers, with KYB/AML and export-control checks; GPU rental to follow [15] | Not disclosed; deposit-secured deals | Claims $330M of hardware deals closed (company press release) [15] | Hardware, not compute time; accepts crypto |
| **Stoa Markets** | Hardware RFQ marketplace | Request-for-quote platform for GPUs and AI servers between vetted institutions (YC S26, launched July 2026) [16] | Not stated | Early stage | Hardware only; brand new |
| **CheapestGPU** | Small broker | "You pay what the data center charges, plus a transparent broker fee" | Fee size not stated [17] | Claims 340+ verified providers; no founders, company details or named customers on the site | Anonymous; claims cannot be checked. This is what the founder must not look like |
| **Architect / Liquid Compute / CME / ICE** | Derivatives venues | Futures and perpetuals on GPU rental indexes (see `pricing-and-indexes.md`) | Exchange fees | Architect $35M Series A; Liquid Compute $15M seed [9] | Financial hedging only; no physical capacity |

Notes on reliability: several fee numbers come from single secondary articles or from competitors' blogs. Before quoting any competitor's fee to a client, check that competitor's own pricing page.

#### What this means

1. **The founder's earlier note is confirmed in outline.** SF Compute's $40M Series A, BGC's division, transparent-fee brokers, and the futures projects are all real [1][14][17]. What the note understated is how much larger and better funded the broker layer has become in 2026 (Andromeda, Hydra Host, Ornn).
2. **Most serious intermediaries are paid by the supply side or by a spread**, not by an explicit buyer fee. Buyers are being trained to expect that sourcing is free.
3. **Most are US-based and US-focused.** Shadeform's shift to brokering large clusters in Asia-Pacific [3] shows where a tiny team found room: regions and deal types the big US players ignore.
4. **None of them is neutral in the way an adviser is.** A marketplace shows its own inventory; a platform that takes a spread benefits from a higher price. That is a real, if modest, opening.

### Where are the gaps?

| Gap | Why it exists | How real is it? |
|---|---|---|
| Mid-size deals (about 8–128 GPUs, 3–12 months) | Too large or too custom for self-serve; too small for neocloud enterprise sales teams and for BGC/Andromeda-type desks | Plausible, but in a tight market suppliers fill capacity with larger customers first, so small deals may simply be refused |
| EU-hosted and "sovereign" capacity | US marketplaces list mostly US capacity; EU buyers care about location, GDPR and contract law | Good fit for the founder's location; needs a verified list of EU suppliers (see supplier research) |
| Balkans / CEE buyers | No player targets them; language and trust matter | Real but small market; deal sizes likely modest |
| Buyer-side vetting and paperwork | Platforms do not compare contract terms, check a supplier's claims, or explain SLAs for the buyer | Real; it is labour, which is what a solo founder has |
| Honest multi-supplier comparison | Each platform shows only its own inventory | Real, but only valuable if the founder actually has access to more than one or two suppliers |

Gaps the founder should **not** chase: large clusters (hundreds of GPUs and up), hardware trading, derivatives, and anything that requires holding money or capacity.

### Q3. Why would a buyer use a small human broker?

**The sceptical view first.** Most buyers should not need one:

- A buyer wanting a handful of GPUs for hours or days is better served by a self-serve marketplace or a GPU cloud's website. There is no commission worth earning there either.
- A buyer wanting a large cluster has internal procurement and will be courted directly by neocloud sales teams and by funded brokers.
- Price transparency is now good: free indexes and comparison sites publish prices daily (see `pricing-and-indexes.md`). "I know the price" is no longer an advantage.
- A new solo broker with no track record adds counterparty risk in the buyer's eyes, not less. The market has fraud and anonymous brokers; the founder will be assumed to be one of them until proven otherwise.
- In a supply-constrained market, suppliers with waiting lists have little reason to pay referral commissions or to prioritise a small broker's customer.

**Where a human broker can honestly add value:**

1. **Search cost when capacity is scarce.** Finding which of 50+ providers actually has 32 H200s free in an EU data centre next month takes many emails. A broker who asks that question every week already knows.
2. **Contract and terms comparison.** Price per hour is the easy part. Minimum term, prepayment, cancellation, SLA credits, data location, support, and what happens on failure differ widely. Buyers without procurement staff value a plain side-by-side.
3. **Vetting.** Checking that the supplier is a real company, that the hardware is what is claimed, and getting test access before commitment.
4. **Negotiation leverage through repeat business.** Only true after the broker has brought a supplier several deals. Not true on day one.
5. **Local trust and language.** For Serbian-, Croatian-, Bosnian- and Montenegrin-speaking buyers, and for EU buyers who want a counterpart in their time zone.
6. **Independence, shown in writing.** Disclosing the commission received from each supplier, and showing options that pay the broker nothing, is something marketplaces structurally cannot do.

**How to build the advantage (in order):**

1. **Build a private, verified supply map**: for 20–30 suppliers, record current GPU types, locations, minimum deal size, lead time, who to email, and whether they pay referrals. Refresh it every two weeks. This is the core asset and costs only time.
2. **Publish useful, checkable content** (for example a monthly "EU GPU availability and price note") under the founder's real name with a real company address. This counters the "anonymous broker" problem directly.
3. **Standardise the deliverable**: a two-page written comparison of three or more options with index prices alongside, commission disclosed. This makes the service concrete and repeatable.
4. **Run compliance visibly** (KYC, sanctions screening, refusal policy). Suppliers increasingly need this from channel partners; it is a reason for a supplier to accept the founder.
5. **Collect proof**: the first two or three closed deals and written references matter more than any website.

**Recommendation for Q3 and Q5.** Do not compete on price discovery or technology. Compete on being a named, accountable person who knows current EU/CEE-relevant supply and does the legwork and paperwork on mid-size deals. Charge the buyer nothing for basic sourcing while the business is unproven (income from disclosed supplier commission); offer paid extras only once there are references. Expect that many suppliers will not pay a commission in the current tight market, and that the first deal may take months.

## Sources

1. eWeek, "SF Compute Raises $40M to Build Marketplace for AI Compute Capacity" — https://www.eweek.com/news/sf-compute-ai-funding/ (checked 2026-11-09)
2. Entrepreneur Loop, "On-Demand GPU Startup Andromeda Raises $60M From Paradigm at $1.5B Valuation" (19 Mar 2026) — https://entrepreneurloop.com/on-demand-gpu-startup-andromeda-1-5b-valuation/ (checked 2026-11-09)
3. SemiAnalysis ClusterMAX 2.0 review of Shadeform (6 Nov 2025) — https://clustermax.semianalysis.com/cloudreview/shadeform (checked 2026-11-09)
4. DeployBase, "Shadeform GPU pricing" (third-party estimate) — https://deploybase.ai/articles/shadeform-gpu-pricing (checked 2026-11-09, via search summary)
5. Sacra, Prime Intellect profile — https://sacra.com/c/prime-intellect (checked 2026-11-09, via search summary)
6. Hydra Host, "Hydra Host raises $100M Series A" — https://hydrahost.com/blog/news/hydra-host-raises-100m-series-a/ ; Business Wire release — https://www.businesswire.com/news/home/20260616230170/en/Hydra-Host- (checked 2026-11-09, via search summary)
7. Business Wire, Compute Exchange releases (Jan, Apr, Aug 2025) — https://www.businesswire.com/news/home/20250807645725/en/ ; interview — https://aistreet.beehiiv.com/p/compute-exchange-s-simeon-bochev-on-making-a-market-for-compute (checked 2026-11-09, via search summary)
8. SiliconANGLE, "Ornn raises $33M" (24 Jun 2026) — https://siliconangle.com/2026/06/24/ornn-raises-33m/ (checked 2026-11-09, via search summary)
9. Newcomer, "Compute crunch: startups aim to financialize" (2 Nov 2026, paywalled preview) — https://www.newcomer.co/p/compute-crunch-startups-aim-to-financialize (checked 2026-11-09)
10. Tom's Hardware, "Nvidia steps back from DGX Cloud" — https://www.tomshardware.com/tech-industry/nvidia-steps-back-from-dgx-cloud ; The New Stack on Lepton — https://thenewstack.io/developers-can-now-uber-gpus-with-nvidias-lepton-platform/ (checked 2026-11-09, via search summary)
11. Vast.ai, "June 2024 product update" — https://vast.ai/article/june-2024-product-update (checked 2026-11-09, via search summary)
12. Akash Network roadmap, AEP-23 / AEP-24 / AEP-76 — https://akash.network/roadmap/aep-24 ; https://akash.network/roadmap/aep-76/ (checked 2026-11-09, via search summary)
13. BlockEden, "DePIN revenue inflection" (Apr 2026) — https://blockeden.xyz/blog/2026/04/03/depin-revenue-inflection-enterprise-cloud-overflow-akash-ionet/ (checked 2026-11-09, via search summary; self-reported figures)
14. Business Wire, "BGC Group Launches Compute Infrastructure Markets" (18 Jun 2026) — https://www.businesswire.com/news/home/20260618743861/en/ ; Finance Magnates — https://www.financemagnates.com/institutional-forex/bgc-wants-to-turn-ai-computing-power-into-the-next-tradable-commodity/ (checked 2026-11-09, via search summary)
15. Nodestream press release on Fortune (19 Aug 2026) — https://fortune.com/press-releases/nodestream-verified-otc-marketplace-gpu-2026-08-19/ (checked 2026-11-09)
16. Runtimewire, "Stoa launched an RFQ marketplace for GPU and AI server trades" (10 Aug 2026) — https://runtimewire.com/article/stoa-markets-rfq-marketplace-gpus-ai-servers (checked 2026-11-09)
17. CheapestGPU home page — https://cheapestgpu.pages.dev/ (checked 2026-11-09)
