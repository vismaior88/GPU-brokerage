# Demand side: who buys, where to find them, how long deals take (Q10, Q11, Q13)
_Last checked: 2026-11-09_

## Summary

- **Realistic first buyers are small and mid-size**: funded AI startups (seed to Series B), university / research groups with a deadline, and SMEs or agencies that need EU-hosted compute. They want 8–64 GPUs for weeks to months. Large enterprises and frontier labs go direct or use established desks; do not plan around them.
- **Why they use an intermediary**: they cannot get allocation or a reply from big providers, they cannot or will not sign 1–3 year commitments, they do not have time to compare 100+ providers, or they need a specific location (EU / data residency) [1][2][3][4]. Price alone is a weak reason: a broker rarely beats a public marketplace on price.
- **Your biggest competitor for small startups is "free"**: hyperscaler credits (Google reportedly up to $350k, AWS up to $100–200k — third-party figures, unverified) [16] and free public compute (EuroHPC AI Factories, Serbia's National AI Platform) [5][6][9]. You cannot broker public compute, but pointing a client to it honestly builds trust and costs you nothing.
- **Public compute has real gaps you can sell into**: allocations are short (1–3 months for Playground / Fast Lane), tied to one project, aimed at training rather than production inference, and can run at "academic tempo" [5][8]. Startups that outgrow it or need production inference are your buyers.
- **Local angle is real but small**: Serbia has an active AI scene (over half of 170 surveyed startups use AI/ML [11]; Startit runs 100+ free AI events a year [14]); Croatia's CroAI has roughly 400 members [13]; Montenegro's market is tiny. Treat SE Europe as your **network and credibility base**, not as your whole market. Paying demand is mostly in the wider EU/UK.
- **Free channels come first**: LinkedIn (free), Startit AI Hub meetups and AI Tinkerers Belgrade (free), founder communities, and direct outreach. The one near-term paid event worth considering is **DSC Europe, Belgrade, 23–27 Nov 2026** (from €350 + VAT) [10]. Slush 2026 is reportedly sold out [17]; skip the large expensive conferences.
- **Deal cycle (estimate, not published data)**: small on-demand / short reservations 1–3 weeks; 8–64 GPU reservations of 1–6 months roughly 3–8 weeks; larger or longer contracts 2–4 months. Add your own KYC time and the supplier's payout delay. Plan on **no commission income for the first 3–4 months**.
- **Why deals fail**: capacity gets sold while the buyer decides, buyer goes direct or uses credits, prepayment / credit terms, buyer is not actually funded, technical mismatch (networking, storage), and KYC failures (which are a correct outcome, not a loss).
- **Recommendation**: weeks 1–4, run 15–20 free "what do you actually pay / struggle with" conversations in the Belgrade / Zagreb / Ljubljana AI community before selling anything. Use the intake form in `/buyers/intake-form.md` from day one.

## Details

### Q10. Who buys GPU capacity through brokers, and why

Published evidence on broker customers is thin and mostly comes from vendors, so treat the profiles below as directional. Compute Exchange says its requests range "from hundreds to tens of thousands of GPUs" from AI startups, cloud providers, enterprises and infrastructure operators [1]. Newcomer reports Ornn routes capacity to startups willing to pay for short-term contracts, because startups compete with giants for compute [2]. SF Compute's early buyers were researchers needing a large burst for a short window [3]. Shadeform describes reservations for "weeks or months" and notes short-term capacity is booked out quickly [4].

| Buyer profile | Typical need | Why an intermediary | Buying process | Fit for you |
|---|---|---|---|---|
| **Funded AI startup (seed–Series B)** | 8–64 GPUs, 1–6 months, fine-tuning / training runs, then inference | No time to compare providers; ignored by big providers; cannot sign multi-year terms | CTO or ML lead decides, founder/CFO approves. Fast (days–weeks) once credits run out | **Best fit** |
| **Startup leaving free credits or public compute** | Move from credits / AI Factory allocation to paid production capacity | First time buying; does not know market prices or contract terms | Same as above; trigger is a credit expiry date | **Best fit** — ask "when do your credits end?" |
| **University / research group** | Burst before a paper or grant deadline; 1–8 weeks | Public allocation too slow or too small for the deadline | PI decides, but university procurement and grant rules slow payment | Medium: small tickets, slow payment |
| **SME / enterprise team needing EU-hosted** | Dedicated nodes in an EU country, GDPR / sector rules | Needs someone to check location and contract claims | IT + legal + procurement; 2–4 months | Medium–good, slower |
| **AI agency / systems integrator** | Capacity for a client project | Wants one contact who sources; may repeat | Project-driven; repeat potential | Good — repeat business |
| **Inference-heavy product company** | Steady 24/7 capacity, cost-sensitive | Wants better reserved price | Benchmarks several providers itself | Hard: they are price experts |
| **Large enterprise / frontier lab / other clouds** | 500+ GPUs, multi-year | Uses large desks, auctions, direct deals | RFP, legal, months | **Not for you now** |

What European startups say they need (Interface policy brief, July 2026, ten interviews in Poland — small sample): cost is a key constraint (7 of 10), data residency raised by all 10, bureaucracy is a barrier (5 of 10), half prefer managed environments over raw machines, and local human support is seen as an advantage over big clouds [8]. This supports a positioning around **EU location, a human who answers, and fast quotes**, rather than "cheapest price".

**Honest weaknesses**
- A buyer with a credit card and 1–8 GPUs can self-serve on a marketplace in minutes. You add nothing there. Your value starts where a human negotiation is needed: reservations, specific regions, clusters with fast networking, contract terms.
- Supply is tight. One analysis argues that as large players sign multi-year deals with neoclouds, there is less idle inventory for intermediaries to place (unverified commentary) [15]. In a tight market the buyer needs you more, but you may have nothing to offer.
- Many small startups are not real buyers yet: they have credits, or no funding. Qualify early (budget, funding, start date).

**Recommendation (Q10):** target funded startups and agencies in Europe needing 8–64 GPUs for 1–12 months, with EU hosting as the lead message. Second target: research groups and startups that have outgrown public compute.

### Q11. Where to find buyers

#### Free channels (start here)

| Channel | Cost | How to use it |
|---|---|---|
| **LinkedIn** (personal profile) | Free | Clear headline ("independent GPU capacity broker, EU focus"). Search ML leads / CTOs at funded AI startups. Post one useful item a week (price movements, what a reservation contract contains). Sales Navigator is paid — skip at first. |
| **Startit AI Hub meetups**, Belgrade and Novi Sad | Free with registration [14] | 100+ free AI events in 2026. Attend, ask people how they get compute. |
| **AI Tinkerers Belgrade** | Free (check page) [14] | Demo-first builder meetups. Builders, not buyers — but they know who is scaling. |
| **ICT Hub / Hub201 AI Salon**, Belgrade | Free / RSVP [14] | Founder and investor crowd. |
| **CroAI** (Croatian AI Association) | Membership fee unknown (unverified) | About 400 members per one source [13]. Follow events; ask for intros. |
| **Digital Serbia Initiative** | Free to follow | Publishes the Startup Scanner (170 startups surveyed in 2026) [11] and feeds the official AI ecosystem map [12] — a ready prospect list. |
| **Science and Technology Parks** (Belgrade, Novi Sad, Niš, Čačak; Tehnopolis and STP Montenegro) | Free | Startups in Serbian parks are eligible for the free National AI Platform [6]; park managers know who has outgrown it. |
| **SAIFA (Serbian AI Factory Antenna)** and national HPC competence centres (NCC Serbia at IPB; NCC Montenegro at UDG) | Free | Not buyers. Referral sources: they meet companies whose needs do not fit public compute. Launched May 2026, coordinated by ETF Belgrade [7]. |
| **VCs and accelerators** (Katapult, regional funds — names unverified by me) | Free | One portfolio intro beats 100 cold emails. Offer a free "compute options" note for their portfolio. |
| **Online communities** (Hugging Face forums, r/LocalLLaMA, MLOps Community Slack, Hacker News) | Free | Answer questions; do not spam. Slow, but builds a name. |
| **Regional media** (Netokracija, Startit, The Recursive) | Free | Pitch one guest article on "how to buy GPU capacity as a startup in the region". |

#### Events, Nov 2026 – May 2027

Dates and prices were found via web search on 2026-11-09. **Check the official site before booking anything.**

| Event | Date | Place | Cost | Verdict |
|---|---|---|---|---|
| **DSC Europe 2026** | 23–27 Nov 2026 | Belgrade Fair, Hall 3 | AI Builders Pass (1 day, 27 Nov) €350; Full €750; VIP €1,500; all + VAT [10] | **Best near-term option.** Regional AI crowd, drive/fly from Montenegro. If budget is tight, buy the one-day pass or just hold meetings around the venue. |
| Web Summit 2026 | 9–12 Nov 2026 | Lisbon | — | Happening now; too late. |
| Slush 2026 | 18–19 Nov 2026 | Helsinki | Startup pass €395; reportedly sold out [17] | Skip. |
| KubeCon + CloudNativeCon Europe 2027 | 15–18 Mar 2027 | Barcelona | Price not checked (typically high) [18] | Skip unless a supplier invites you. Has AI / sovereign cloud side-days. |
| Tech Show London / Data Centre World | 10–11 Mar 2027 | ExCeL London | Free for "buyers"; **service providers pay £199 + VAT until 31 Dec 2026**, rising later [19] | Supply side mostly. Useful for meeting data centres; travel is the real cost. A broker likely counts as a service provider. |
| Founder Institute Montenegro | 8 Mar – 25 May 2027 | Montenegro | Fee not checked [20] | A programme, not an event. Local founder network. |
| Wolves Summit | 7–8 Apr 2027 (unverified) | Warsaw (unverified) | Not checked | Optional. |
| Podim 2027 | 17–19 May 2027 (unverified, third-party listing) | Maribor, Slovenia | Not checked | Good regional startup/investor event; reachable by car. |
| EuroHPC Summit 2027 | Not announced (2026 edition was postponed) [21] | — | — | Watch only. |
| ISC High Performance 2027 | 7–11 Jun 2027 (just outside 6 months) | Hamburg | Not published [22] | HPC supplier event. Later. |
| VivaTech / GTC Paris 2027 | 16–19 Jun 2027 (unverified) | Paris | Not checked | Later. |
| Startit AI Week | Was 25–31 May in 2026; 2027 date not announced [14] | Belgrade | Mostly free | Watch for the 2027 date. |

Not found / not announced for 2027: Infobip Shift (Zadar, was 13–15 Sept 2026), AI2Future (Zagreb, usually October), Kiss the Future AI Summit (Sarajevo), Adriatics Tech Summit (Sarajevo, was Mar–Apr 2026), Spark.me (Montenegro), AI Tech Summit SEE (Belgrade, was 3–4 Sept 2026). All **(unverified for 2027)**.

**Budget reality:** with under $2,000 for six months, one regional event (DSC Europe one-day pass plus bus/car and a night in Belgrade ≈ €500–600) is the most you should spend. Everything else should be free meetups and outreach. Do not buy a booth anywhere.

#### Free public compute: mention it, never broker it

| Programme | What it is | Who can use it | Why it cannot be brokered |
|---|---|---|---|
| **EuroHPC AI Factories** | Free GPU time on EU supercomputers. Playground (entry level, access targeted in ~2 working days), Fast Lane (up to 50,000 GPU hours, 1–3 months), Large Scale (50,000+ GPU hours, 3–12 months, peer reviewed) [5][9] | Free for AI startups and SMEs for innovation; eligible countries reportedly include EU members and EuroHPC Participating States [9]. Serbia and Montenegro are Participating States [23]. **Confirm eligibility in each call's Terms of Reference.** | Allocation is awarded to a named applicant for a named project, with reporting duties [9]. I did not find the exact non-transfer wording (unverified) — treat it as not transferable. |
| **Serbia's National AI Platform** (State Data Centre, Kragujevac) | First system: 4× NVIDIA DGX A100 (32 GPUs). A second, faster system was launched 30 Apr 2026 (government says ~7× faster). A larger third phase was planned for 2026; status not confirmed [6][24] | Universities, institutes, and domestic startups in science and technology parks; "completely free of charge" per the government [6]. 38 startups were users as of May 2025 (government presentation) [25] | State resource allocated to eligible users. |
| **SAIFA** (Serbian AI Factory Antenna) | Support and onboarding link to AI Factories (partners: Pharos in Greece, IT4LIA in Italy) [7] | Serbian startups, SMEs, researchers | It is a support service, not capacity. |

How to use this: when a small startup asks for 4–8 GPUs for an experiment, tell them to try Playground / the National Platform first. Some AI Factory systems were marked unavailable for new allocations in October 2026 [9] — that is exactly when a startup needs a paid fallback, and they will remember who gave honest advice.

**Recommendation (Q11):** 80% of effort on free channels: LinkedIn + Belgrade/Novi Sad meetups + park/VC/NCC referral sources. One paid event at most (DSC Europe). Build a prospect list from the Serbian AI ecosystem map and CroAI members.

### Q13. Deal cycle and why deals fail

I found **no published sales-cycle figures** for brokered GPU deals. The table is my estimate from how the market works (reservation flows described by marketplaces [4], providers pushing commitments and prepayment [15], enterprise procurement norms). Treat as planning assumptions and replace with your own data.

| Deal type | Estimated time, first contact → signed | Then → your commission paid |
|---|---|---|
| On-demand / self-serve via referral link | Days | Per programme terms; often 30–90 days after the customer pays (see supplier research) |
| 8–64 GPUs, 1–6 months, startup | 3–8 weeks | + 1–3 months |
| EU-residency deal with legal review, SME/enterprise | 2–4 months | + 1–3 months |
| University / grant-funded | 1–3 months (procurement) | + 1–3 months |
| 100+ GPUs, 12+ months | 3–6 months | + 1–3 months |

Steps that take time: intake (1–2 days), your KYC and screening (1–5 days), supplier quotes (2–7 days), test access / benchmark (3–10 days), contract and supplier's own onboarding/KYC (1–3 weeks), payment or prepayment.

**Why deals fail**

| Reason | What to do |
|---|---|
| Capacity sold while buyer decides (tight market) | Give quotes an expiry date; get 2–3 options; tell the buyer plainly that quotes are not holds. |
| Buyer goes direct after you introduce the supplier | Register the deal with the supplier in writing before naming them; see legal research on non-circumvention. |
| Buyer uses free credits or public compute instead | Qualify early. Stay in touch for when credits end. |
| Buyer not funded / fails supplier credit check / will not prepay | Ask about budget and payment terms in the intake form. |
| Price expectations from marketplace spot prices | Explain the difference between spot, on-demand and reserved with SLAs; show index prices. |
| Technical mismatch (no InfiniBand, wrong storage, region) | Collect details in intake; do not quote without them. |
| Supplier slow or does not deliver as described | Work only with suppliers you have verified; ask for test access. |
| Buyer fails KYC, refuses to name end user, or red flags appear | **Decline.** This is the system working. See `/compliance/`. |
| Slow buyer procurement / legal | Expect it; keep several deals in parallel. |
| You are too slow | Reply within 24 hours; first indicative range within 48 hours. |

**Recommendation (Q13):** assume first commission cash arrives month 4–6 at the earliest. Keep at least 10 qualified conversations open to close 1–2 deals. Record the actual days per stage in `pipeline.csv` so estimates become data.

## Questions for a lawyer / accountant

- If I advise a client to apply for EuroHPC or national public compute and later sell them paid capacity, is there any conflict or disclosure I should make in my buyer agreement?
- Does cold B2B email to EU contacts from a US LLC run by a Montenegro resident need specific GDPR / ePrivacy steps (legitimate-interest note, opt-out, country differences, e.g. Germany is stricter)?
- Can a referral agreement stop me from telling a buyer about a competing free or cheaper option?

## Sources

All checked 2026-11-09.

1. SiliconANGLE, "Compute Exchange opens secondary market for used Nvidia H100/A100 GPUs" (17 Jul 2026) — https://siliconangle.com/2026/07/17/compute-exchange-opens-secondary-market-used-nvidia-h100-a100-gpus/
2. Newcomer, "Compute crunch: startups aim to financialize" — https://www.newcomer.co/p/compute-crunch-startups-aim-to-financialize
3. Latent Space, SF Compute profile / "Commoditizing GPUs" — https://latent.space/reading/sf-compute-commoditizing-gpus/
4. Shadeform, "How to rent GPU instances and clusters" — https://shadeform.ai/blog/how-to-rent-gpu-instances-and-clusters-on-shadeform ; Cerebral Valley interview — https://cerebralvalley.beehiiv.com/p/gpu-clouds-everywhere-are-sold-out-shadeform-is-building-the-solution
5. EuroHPC JU, AI Factories access calls — https://www.eurohpc-ju.europa.eu/ai-factories/ai-factories-access-calls_en
6. Serbia Office for IT and eGovernment, National Platform for AI — https://www.ite.gov.rs/tekst/en/35/government-data-centredr-location-in-kragujevac.php
7. ETF Belgrade, "Project SAIFA launched" (May 2026) — https://www.etf.bg.ac.rs/en/news/2026/05/project-saifa-serbian-artificial-intelligence-factory-antenna-launched ; antenna country list via Web Summit/EuroHPC press release — https://websummit.com/wp-media/2025/11/WS_Press_Release_-_EuroHPC_JU_Expands_AI_Factory_Network_to_Boost_Innovation_for_European_Startups_and_SMEs.docx.docx.pdf
8. Interface, "Public compute for applied AI startups" policy brief (1 Jul 2026) — https://www.interface-eu.org/publications/public-compute-applied-ai-startups
9. EU AI Continent (euacc.ai), AI Factories programme page (third-party summary of EuroHPC terms) — https://www.euacc.ai/programmes/ai-factories
10. DSC Europe 2026 — https://www.datasciconference.com ; Belgrade Fair listing — https://sajam.rs/en/?p=55295
11. Startup Genome, "Serbia's startup ecosystem is ready to scale together" (GSER 2026, cites DSI Startup Scanner) — https://startupgenome.com/report/the-global-startup-ecosystem-report-2026/serbia-s-startup-ecosystem-is-ready-to-scale-together
12. UNDP Serbia, interactive map of the AI ecosystem — https://www.undp.org/serbia/news/interactive-map-ai-ecosystem-showcasing-serbias-potential-artificial-intelligence
13. Science|Business, "Ecosystem: Croatia looks forward to ubiquitous AI" — https://sciencebusiness.net/widening/news/AI/ecosystem-croatia-looks-forward-ubiquitous-artificial-intelligence ; CroAI member count from Czech embassy page — https://mzv.gov.cz/zagreb/cz/obchod_a_ekonomika/chorvatsko_planuje_investovat_temer.html
14. Startit AI Hub meetups — https://startit.rs/ai-hub-meetups/ ; Startit AI Week — https://startit.rs/ai-week ; AI Tinkerers Belgrade — https://belgrade.aitinkerers.org/ ; AI Salon Belgrade — https://luma.com/AI-Salon-Belgrade-March-2026
15. Spheron blog (vendor commentary on neocloud utilisation and commitments) — https://spheron.network/blog/nvidia-neocloud-backstop-financing-circular-gpu-2026/ ; Sacra note on reservations — https://sacra.com/chat/h/b185f43c-023d-440a-8857-025e4a3739da/
16. Causo, "Startup cloud credits compared 2026" (third-party aggregator) — https://hub.causo.ai/startup-cloud-credits-compared-2026
17. Slush — https://www.slush.org/ ; sold-out status via https://www.opencurious.com/tech-events/slush-2026
18. KubeCon + CloudNativeCon Europe 2027 — https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/attend/faq/
19. Tech Show London (incl. Data Centre World) — https://techshowlondon.co.uk ; visitor FAQs — https://www.techshowlondon.co.uk/visitor-faqs
20. Founder Institute Montenegro — https://fi.co/apply/15422 ; Montenegro ecosystem: https://tehnopolis.me/en/grand-finale-of-montenegro-pitching-competition-2026-held/
21. EuroHPC Summit 2026 (postponed) — https://www.eurohpc-ju.europa.eu/media-events/events/eurohpc-summit-2026-2026-03-10_en
22. ISC High Performance — https://www.isc-hpc.com/
23. EuroHPC JU, "Switzerland officially rejoins" (lists non-EU Participating States incl. Montenegro, Serbia) — https://eurohpc-ju.europa.eu/switzerland-officially-rejoins-eurohpc-joint-undertaking-2025-11-11_en
24. Tanjug, supercomputer launch in Kragujevac (30 Apr 2026) — https://www.tanjug.rs/english/politics/248766/titolo-supercomputer-launch-in-kragujevac-confirms-new-era-in-us-serbia-relations/vest
25. Government presentation at EuroCC4SEE workshop (May 2025) — https://www.hpc.ipb.ac.rs/news/day-two-of-the-eurocc4see-workshop-in-belgrade/EuroCC4SEE-BStesevic-20250521.pdf
