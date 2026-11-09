# Supplier partner programs, why suppliers use brokers, and other capacity sources (Q6, Q4, Q7)
_Last checked: 2026-11-09_

## Summary

- **Public referral money in GPU cloud is thin and uneven.** Of 43 suppliers checked, only about ten publish a number. Published cash rates range from **1% for 6 months** (Hyperbolic) to **8–10% recurring** (Ingenuity) and **15% lifetime** (CloudSigma, whose GPU depth is unconfirmed). Most serious neoclouds publish no rate at all and negotiate case by case.
- **Your earlier notes mostly hold, with two corrections.** Ingenuity (8%/10%, 4%/5%), Nebius (64+ GPUs, more above 512), Cirrascale (monthly recurring), RunPod and Thunder Compute (3% in credits) are confirmed. **Crusoe's "affiliate program" is not confirmed** – the affiliate URL is dead; Crusoe lists "referral partnerships" with no terms. **RunPod's cash affiliate tier needs 25 paying referrals first** and its Terms of Service restrict "buying or purchasing agents" and resale without consent.
- **Self-serve programs (RunPod, Thunder, Massed Compute, Vast.ai, Latitude.sh) mostly pay in credits or small bounties.** They are built for content creators, not brokers. Do not build the business on them.
- **Realistically open to a brand-new one-person US LLC:** Ingenuity, Cirrascale, Nebius referral (if you can bring a 64+ GPU deal), CloudFerro referral, CloudSigma, OVHcloud referral path, Civo, Hydra Host, Hyperbolic, DigitalOcean (Registered tier). Not realistic at the start: CoreWeave, Lambda, Nscale, Fluidstack, Taiga Cloud.
- **Suppliers pay for introductions they could not get themselves.** The pattern in program terms is clear: minimum deal sizes (Nebius 64 GPUs; OVH €500–€100k MRR with 12-month commitment), lead qualification, and "not already in our pipeline" rules. They want new, committed, mid-size customers – not small on-demand users.
- **Honest caveat:** I could not verify current market tightness in this session. If prices are rising as your notes say, top suppliers with full order books have little reason to pay a new broker. Your leverage will be with second-tier, regional and newer suppliers that lack sales reach – exactly where verification (see `supplier-verification.md`) matters most.
- **Other capacity sources exist but are harder than they look.** Idle reserved capacity is already being intermediated (SF Compute sublease, Fluidstack). Ex-crypto miners have become large AI hosts selling to hyperscalers. Regional/sovereign suppliers (e.g. Orion Telekom in Belgrade) are the most plausible edge for a Serbian-speaking founder. University and public HPC capacity cannot be brokered.
- **Recommendation:** sign 3–5 referral agreements in this order: Ingenuity, Cirrascale, Nebius, one EU sovereign option (CloudFerro or OVHcloud), plus Hydra Host. Ask every supplier the same ten questions (listed below) and record answers in `suppliers/suppliers.csv`.

> **Research limits.** The shared web-search budget ran out part-way through. Some supplier pages blocked or failed direct reading (noted per source). Headquarters, data-centre locations and GPU model lists in `suppliers.csv` are from general knowledge unless the notes column says otherwise – confirm them on the first call. Nothing here was confirmed with a supplier directly; no supplier was contacted.

## Details

### Q6. Which suppliers run partner, referral or reseller programs, and on what terms?

Full list: `suppliers/suppliers.csv` (43 rows). The table below shows only suppliers with **published** terms.

| Supplier | Type | Published terms | Paid in | Good for a broker? |
|---|---|---|---|---|
| Ingenuity Cloud Services (THG) | Referral + reseller | 8% month-to-month, 10% on 12+ month terms in own/select data centres; 4% / 5% in partner data centres; "evergreen"; signed Referral Agreement and deal registration required; "no fees or commitment" to join [1][2] | Cash (payout timing not public) | **Yes – best documented** |
| Nebius | Referral | Applies to customer agreements of 64+ GPUs; higher above 512 GPUs. One version of the page stated 5% of customer payments for the first 12 months; the current page is reported as "discussed case by case" [3]. Separate Partner Program for resellers has no public numbers [4][5] | Cash (unverified) | Yes, for mid-size deals |
| Cirrascale | Referral | Monthly recurring commission on dedicated multi-GPU services; non-exclusive; worldwide; rate given only on request [6] | Cash, monthly | Yes – ask for the rate |
| CloudFerro (Poland) | Referral / VAR / MSP | Referral 5–20% commission; VAR discount 10–35%; MSP 15–40% [20] | Cash (unverified) | Yes – EU-hosted |
| CloudSigma (Switzerland) | Referral | 15% revenue share for the lifetime of the account [21] | Unverified | Maybe – confirm GPU inventory first |
| OVHcloud | Referral path | Referral fee at all three levels, % not public; referred deal minimum MRR €500 / €10,000 / €100,000 with 12-month commitment; about one referral per quarter expected [17] | Unverified | Yes – EU sovereign angle |
| Civo (UK) | Partner program | Mandatory deal registration, 90-day protection, no mandatory revenue commitment; current page gives no %. A 2021 press report gave 5% / 10% / 15–30% by tier – treat as outdated [19] | Unverified | Maybe |
| Hyperbolic | Referral | 1% of revenue for first 6 months; customer must sign within 180 days; paid quarterly [22] | Cash | Weak |
| OpenMetal | Referral | 10% of first month's MRR, capped at $2,500 per deal, one-time; lead owned 6 months; page says sole proprietors excluded [28] | Cash | Weak (one-time, capped) |
| RunPod | Referral → affiliate | Referral: 5% Serverless + 3% Pod spend for 6 months, in credits. Affiliate: 10% cash for 6 months via PartnerStack, only after 25 paying referrals [9]. Reseller/implementation tracks by application, terms not public [10] | Credits, then cash | Weak for brokerage |
| Massed Compute | Referral / affiliate | 3% in credits self-serve; "up to 10%" revenue share for approved affiliates [26] | Credits / cash | Weak–medium |
| Thunder Compute | Referral (beta) | 3% of card-paid GPU spend, lifetime, credits only, not convertible to cash [12] | Credits | No |
| Vast.ai | Referral | 3% of referred spend for life; up to 75% can be cashed out via a dedicated referral account [36] | Credits / cash | Weak |
| Latitude.sh | Referral | $200 in credits per paying referral [27] | Credits | No |
| Hivelocity | Referral agents | "Up to 20%" monthly per developer docs; GPU applicability not confirmed [30] | Cash | Unverified |
| HPC-AI (Singapore) | Sales partner | No fixed rate; usage-based or negotiated profit share; one customer mapped to one partner [23] | Cash | Unknown supplier – diligence first |

**No public referral terms found** (program exists but terms are private, or no program found): Crusoe [7][8], Lambda [13], CoreWeave [14], Hyperstack/NexGen [15], Scaleway [18], Hydra Host [24], DigitalOcean [25], Gcore [32], GMI Cloud [34], E2E Networks [35], Vultr [16], Leaseweb [29], Verda, Nscale [45], Genesis Cloud, Taiga Cloud [46], Fluidstack [39], Voltage Park, TensorWave, Together AI, Denvr, Yotta, Firmus [47].

#### Verification of your earlier notes

| Your note | Result |
|---|---|
| Ingenuity: 8% / 10% own data centres; 4–5% partner data centres | **Confirmed** [1][2]. Payout timing, clawbacks and caps are in the Referral Agreement, which is not public. |
| Nebius: referral for 64+ GPUs, more above 512 | **Confirmed** [3]. The percentage is not reliably public (5% for 12 months appeared on one version). |
| Cirrascale: recurring monthly commission | **Confirmed** [6]. Rate not public. |
| Crusoe: affiliate program | **Not confirmed.** Only a third-party directory mentions it [8]; `crusoe.ai/affiliates` returned "not found". Crusoe's partner page lists a "referral partnerships" track with no terms [7]. |
| RunPod: affiliate program | **Confirmed, but** cash needs 25 paying referrals, lasts 6 months per referral, and the opt-in is permanent [9]. |
| Thunder Compute: 3% in credits | **Confirmed** [12]. Credits cannot be turned into cash. |

#### What the terms look like in practice

- **Commission level.** 5–10% of customer spend is the realistic band for a real referral agreement. 1–3% is the self-serve band. Anything above 10% was reseller margin or unconfirmed for GPUs.
- **Duration.** Three patterns: "evergreen"/lifetime (Ingenuity, CloudSigma, Cirrascale's "recurring"); time-limited (Nebius 12 months, RunPod and Hyperbolic 6 months); one-time (OpenMetal).
- **Minimum deal size.** Nebius 64 GPUs; OVH €500 MRR with a 12-month commitment at the lowest level. Others state none.
- **Payout timing.** Rarely public. Published examples: quarterly, about 30 days after quarter end (Hyperbolic); within 30 days of customer payment (OpenMetal); monthly (Cirrascale). Expect to be paid only after the customer pays.
- **Deal registration.** Standard. Ingenuity and Civo require it; Civo protects a registered deal for 90 days, OpenMetal for 6 months, Hyperbolic requires signature within 180 days. A lead already known to the supplier earns nothing.
- **Restrictions to look for.** I did **not** find a published ban on charging the buyer a separate fee in any program page – those clauses live in the private agreements, so read each one. What I did find: RunPod's Terms of Service prohibit reselling credits and using "buying or purchasing agents" without written consent, and cap RunPod's liability at $100 [11]. OpenMetal excludes referrals of your own organisation and "unauthorized discount deals" [28].

**Illustration only (not a forecast):** at your earlier note of roughly $3.10 per GPU-hour for H100 (not re-verified by me), 64 GPUs running all month is about $145,000/month of customer spend. At 5% for 12 months that is about $7,200/month; at 8–10% it is $11,600–$14,500/month. One such deal matters; small on-demand referrals do not.

#### Which programs are realistically open to a new one-person US LLC?

| Tier | Suppliers | Why |
|---|---|---|
| **Apply now** | Ingenuity, Cirrascale, Nebius referral, CloudFerro referral, CloudSigma, Hydra Host, Hyperbolic | Open application, no joining fee or revenue commitment stated; referral track designed for introducers without their own services |
| **Apply, expect questions** | OVHcloud referral path, Civo, DigitalOcean Registered, Massed Compute affiliate, RunPod partner tracks, E2E Networks | Application reviewed; some expect regular referrals, certifications, or an existing audience |
| **Not yet** | CoreWeave, Lambda, Nscale, Fluidstack, Taiga Cloud, Together AI, GMI reseller, NexGen reseller | Technology-partner or wholesale orientation; reseller tracks need capital and a customer base |

Being a US LLC helps with US suppliers (contracting, W-8/W-9 paperwork – see finance files). Expect every supplier to ask who you are, what customers you already have, and for a deal to register. **A partner agreement with no registered deal is worth nothing; lead with a real buyer need.**

#### Ten questions to ask every supplier

1. Commission % and what revenue it is calculated on (list price, net of discounts, net of credits)?
2. How long is it paid (months, or life of customer)? On renewals and expansions too?
3. Minimum deal size or term?
4. When and how am I paid, in what currency, and after which event (invoice issued or customer payment)?
5. How do I register a deal, how long is it protected, and how do I know if the lead was already yours?
6. Clawbacks if the customer cancels, defaults or gets a refund?
7. May I also charge the buyer a disclosed fee? May I disclose my commission to the buyer?
8. Any exclusivity, non-compete or minimum-activity requirement?
9. What happens to my commissions if the agreement is terminated?
10. Who contracts with the customer, and what SLA does the customer get?

### Q4. Why would a supplier work with a broker?

What the evidence shows suppliers struggle with:

1. **Sales reach.** Neoclouds are engineering-heavy and sales-light. Nebius has said publicly that it wants distributors, telcos and resellers "across the board" and launched a formal partner program in 2026 [5]. Crusoe and CoreWeave were hiring people to build channel programs and incentive tiers [7][14]. A program that is still being built means the supplier wants channel revenue but has no process yet.
2. **Filling capacity that is idle or newly switched on.** Fluidstack's original business was finding "idle or newly deployed GPUs inside partner data centers" and selling them in contracts averaging about $340K [39]. NexGen's partner pack talks about monetising underused capacity [15]; RunPod and Hydra Host run supply-side partner tracks for data-centre operators with GPUs to fill [10][24].
3. **Mid-size committed deals.** Minimums and commitment terms in the programs (64 GPUs; 12-month commitments) show what suppliers will pay for: customers large enough to matter but too small for the supplier's own enterprise team to hunt.
4. **Regional and language reach.** A supplier in Finland or the US has no one selling in Serbian, Croatian or Montenegrin, or into Balkan universities and companies. This is a small but real edge.
5. **Qualification and screening.** Hyperbolic, OpenMetal and Civo only pay for *qualified* leads [22][28][19]. A broker who arrives with a completed intake form and KYC already done saves the supplier work.

What suppliers do **not** need from you: small on-demand users (self-serve covers them) and, when capacity is sold out, any leads at all.

**Recommendation:** position yourself to suppliers as "pre-qualified, KYC-screened, 16–256 GPU, 6–24 month buyers from regions you don't cover". Do not pitch volume you cannot show.

### Q7. Where else does capacity come from?

| Source | How it works | Who already does it | Realistic for you? |
|---|---|---|---|
| **Idle reserved capacity** (companies that over-bought) | Holder subleases unused reserved GPUs | SF Compute lets customers "sublease your reserved capacity when plans change" and sell idle compute through its scheduler [38]; Fluidstack began this way [39] | **Medium-hard.** Most cloud contracts forbid resale without consent (see RunPod's terms [11]). Only broker it with the original provider's written consent. Finding holders needs a network you do not yet have. |
| **Crypto miners converting to AI** | Miners with power and buildings host GPU clusters | IREN now presents itself purely as an AI cloud and data-centre business with 5 GW+ of secured power across North America, Europe (planned 300 MW in Badajoz, Spain) and Australia [40]; TeraWulf hosts for Fluidstack under long-dated agreements from 2026 [39] | **Low for the big names** – they sell to hyperscalers. Smaller converting miners are possible suppliers but are the highest verification risk (new to AI, unproven networking and support). |
| **Regional and sovereign data centres** | Telcos and local operators build "AI factories" | Orion Telekom opened a commercial sovereign AI factory in Belgrade in 2026 offering GPU-as-a-Service on NVIDIA DGX B200, and is adding a system at the State Data Centre expected in the first half of 2027 [41]; CloudFerro (Poland), OVHcloud and Scaleway (France) in the EU; Yotta and E2E in India [35][43]; a 1 GW campus in Topusko, Croatia was announced in April 2026 but is not operating [42] | **Best fit.** Language, proximity and data-residency demand. Capacity is small, so deals are small. |
| **Balkans / SE Europe today** | Local hosting firms and marketplace hosts | Price trackers list only a handful of offers in Serbia, Bulgaria, Slovenia, Croatia and Greece, mostly marketplace hosts and small providers; Serbia is described as nascent, with consumer-grade cards [48] | **Thin.** Do not promise Balkan-hosted H100/B200 clusters until you have confirmed a specific supplier. |
| **Universities and public HPC** | Allocated to projects by application | EuroHPC AI Factories; Serbia's National AI Platform in Kragujevac [41] | **Not brokerable.** Mention to eligible clients as a free option; never charge for access. (Rules not re-verified in this session.) |
| **Aggregators / marketplaces** | One account, many suppliers | Vast.ai (3% referral [36]); Spheron; Hydra Host's Brokkr [24] | Useful as a backup source and price check; they are also competitors. |

**Recommendation for Q7:** treat regional/sovereign suppliers as your differentiator and established neoclouds as your income. Leave idle-capacity brokerage and ex-miner sourcing until you have a verification routine and at least one closed deal.

## Questions for a lawyer / accountant

1. In each referral agreement: am I an independent contractor with no authority to bind the supplier? (Avoid "agent" language.)
2. Can I lawfully charge the buyer a disclosed fee while also receiving a supplier commission, under each supplier's agreement and under US state law on undisclosed commissions?
3. Do "evergreen" commissions survive termination of the agreement? What wording protects that?
4. If I introduce a holder of idle reserved capacity to a sub-user, what consent is needed from the original cloud, and what is my exposure if it is not obtained?
5. Paperwork suppliers will ask a foreign-owned US LLC for (W-9 vs W-8BEN-E) and how commissions are reported.

## Sources

All checked 2026-11-09. "Search summary" means the page was read through a search-engine result because the page itself could not be opened from the research session.

1. Ingenuity Cloud Services – THG ICS Partner Program, https://www.ingenuitycloudservices.com/partner-program/ (search summary; direct read did not show program text)
2. Ingenuity Cloud Services – Partner Program Brochure (PDF), https://www.ingenuitycloudservices.com/download/pdf/THG_Ingenuity_Cloud_Services_ICS_Partner_Program_Brochure.pdf (search summary; direct link returned 404)
3. Nebius – Referral program, https://nebius.com/referral (search summary; two versions indexed)
4. Nebius – Partner Program, https://nebius.com/nebius-partner-program
5. CRN Asia – "GPU Cloud Standout Nebius On TD Synnex Deal, Nvidia And New Partner Program In 2026", https://www.crnasia.com/news-network/2026/gpu-cloud-standout-nebius-on-td-synnex-deal-nvidia-and-new-partner-program-in-2026 (search summary)
6. Cirrascale – Referral Programs, https://referral.cirrascale.com (search summary; host not reachable from session)
7. Crusoe – Partner with Crusoe Cloud, https://crusoe.ai/partners
8. StartupHub.ai – Crusoe affiliate program listing, https://www.startuphub.ai/startups/crusoe/affiliate-program (third-party; search summary)
9. RunPod docs – Referrals, https://docs.runpod.io/accounts-billing/referrals
10. RunPod – Partners, https://www.runpod.io/partners
11. RunPod – Terms of Service, https://www.runpod.io/legal/terms-of-service
12. Thunder Compute docs – Referral program, https://www.thundercompute.com/docs/guides/referral-program
13. Lambda – Partners, https://lambda.com/partners
14. CoreWeave – Partner Network announcement, https://coreweave.com/news/coreweave-partner-network-accelerates-the-path-to-ai-innovation (search summary)
15. NexGen Cloud – Channel partnerships, https://www.nexgencloud.com/channel-partnerships
16. UpPromote – Vultr affiliate listing (third-party), https://uppromote.com/affiliate-directory/vultr/ (search summary)
17. OVHcloud – Referral Advisory Path, https://partner.ovhcloud.com/en/referral-advisory-path/
18. Scaleway – Partners program, https://www.scaleway.com/en/partners-program/ (search summary)
19. Civo – Partners, https://civo.com/partners ; ITPro 2021 report, https://www.itpro.com/business/business-strategy/367077/civo-unveils-new-partner-programme (search summary)
20. CloudFerro – Partner Programme, https://cloudferro.com/cloudferro-partner-programme/
21. CloudSigma – Referral Partner Program, https://www.cloudsigma.com/affiliate-program/
22. Hyperbolic – Partner Program (11 Aug 2025), https://www.hyperbolic.ai/blog/introducing-hyperbolic-partner-program
23. HPC-AI – Sales Partner Program, https://www.hpc-ai.com/blog/PartnerProgram
24. Hydra Host – Partner Program, https://hydrahost.com/partners/
25. DigitalOcean – Partner Pod, https://www.digitalocean.com/channel-partners
26. Massed Compute – Affiliate Program, https://massedcompute.com/affiliate-program/
27. Latitude.sh docs – Referral program, https://www.latitude.sh/docs/referral-program (search summary)
28. OpenMetal – Enterprise-to-Enterprise referral program, https://info.openmetal.io/enterprise-to-enterprise-e2e-referral-program
29. ITPro – Leaseweb partner program, https://www.itpro.com/business/business-strategy/leaseweb-launches-new-partner-program-amid-fresh-channel-investment (search summary)
30. Hivelocity – Partner Program, https://hivelocity.net/about/partners ; developer docs, https://developers.hivelocity.net/docs/resellers-and-solution-partners (search summary)
31. Atlantic.Net – Partner/referral FAQ, https://www.atlantic.net/partners/faq
32. Gcore – support article on referral program, https://gcore.com/support/articles/115005457805 (search summary; https://gcore.com/referral-program returned 404)
33. CUDO Compute – affiliate programme press release, https://pressat.co.uk/releases/cudo-compute-unveils-pioneering-affiliate-programme-amidst-rising-demand-for-high-performance-cloud-resources-80ec7cc732c4d33aceefb4e075be1b14 (search summary)
34. GMI Cloud – Partners, https://www.gmicloud.ai/partners
35. E2E Networks – Become a partner, https://e2enetworks.com/become-a-partner (search summary)
36. Vast.ai docs – Referral program, https://docs.vast.ai/guides/reference/referral-program
37. UpCloud – Affiliate program, https://upcloud.com/affiliate-program/ (search summary; direct read blocked)
38. SF Compute – home page, https://sfcompute.com
39. Sacra – Fluidstack analysis, https://sacra.com/chat/h/b3863997-808e-4513-bb34-0075ee0813a9/ (analyst summary, not company disclosure)
40. IREN – company site, https://iren.com/
41. Orion Telekom – sovereign AI factory announcement, https://oriontelekom.rs/orion-telekom-launches-a-sovereign-ai-factory/ (search summary; page returned 503) ; Biznis.rs, 23 Oct 2026, https://biznis.rs/biznis/orion-telekom-i-nvidia-grade-novu-ai-infrastrukturu-u-srbiji/
42. W.Media – Pantheon Atlas €50bn AI data center campus in Croatia, https://w.media/pantheon-atlas-plans-e50bn-ai-data-center-campus-in-croatia/ (search summary)
43. NVIDIA – Cloud Partners list, https://www.nvidia.com/en-us/data-center/gpu-cloud-computing/partners.md
44. SemiAnalysis ClusterMAX – Verda/DataCrunch review, https://clustermax.semianalysis.com/cloudreview/verdadatacrunch
45. Nscale – Singtel partnership, https://www.nscale.com/press-releases/singtel-and-nscale-unlock-gpu-capacity-globally-to-accelerate-ai-adoption (search summary)
46. RCR Wireless – Northern Data / Core42, https://www.rcrwireless.com/20250814/ai-infrastructure/core42-gpu (search summary)
47. TensorWave – Venture Connect Program, https://tensorwave.com/venture-connect-program (search summary); Yotta Rudra program, https://yotta.com/press-releases/yotta-launches-rudra-program-to-extend-yotta-shakti-cloud-credits-to-members-of-nvidia-inception-and-nvidia-connect-accelerating-ai-innovation/ (search summary). No partner-program pages found for Voltage Park, Together AI, Denvr, Genesis Cloud, Firmus.
48. GPUPerHour – Cloud GPU regions, https://gpuperhour.com/regions (search summary)
