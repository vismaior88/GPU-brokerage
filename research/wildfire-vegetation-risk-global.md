# Wildfire and vegetation risk: global market
_Last checked: 2026-11-18_

Builds on `satellite-imagery-ideas.md` (idea 3 downgraded to **Maybe**: no Balkan buyer, EFFIS is free, Overstory and LiveEO are well funded; see its "How it works" primer for free data, imagery prices and platforms) and `public-compute-for-startups.md` (free EuroHPC compute helps only with AI training bursts, and only through a Montenegrin d.o.o.). Not repeated here. Facts marked **(unverified)** could not be confirmed from a primary or reliable source. "Via search summary" in Sources means I read a search-engine summary, not the page itself.

## Summary

- **Direct answer: yes, it sells, but not by a newcomer building a product.** Utilities in the US, Australia and Southern Europe pay real money for satellite and AI vegetation risk work, driven by fire liability. The market is now **crowded and consolidating**. Schneider Electric agreed in mid-2026 to buy ~90% of AiDASH at a $350m valuation [7]. Overstory raised $43m in Nov 2025 and says it serves "6 of the 10 largest utilities" in the Americas [1][2]. LiveEO raised €28m in May 2026 [12]. Technosylva says it serves 25+ utilities [10].
- **The "small utilities are priced out" gap is mostly closed.** Small US municipal utilities already buy direct from the big vendors at modest prices. Rochelle, Illinois signed with AiDash at **$54,000/year for 5 years** (Nov 2025) [8]. Denton, Texas signed with AiDash at **up to $370,834 over 5 years** (Oct 2025) [9]. Eugene (EWEB) uses Overstory [6]. Overstory's customers include small co-ops such as Holy Cross Energy [5].
- **Best markets by money and urgency:**
  - **(1) US utilities under new state wildfire-plan laws.** Texas HB 145 made wildfire mitigation plans compulsory for co-ops in risk areas, with PUC rules in force from 4 Dec 2025 [26]. Idaho, Montana, Utah and Washington have similar plan-for-liability-relief laws [27][33].
  - **(2) Southern Europe, above all Greece.** Power lines were linked to the leading share of major 2025 fires, there were arrests and lawsuits in 2026, and HEDNO now invests ~€800m/year [38].
  - **(3) Australia**, where Powercor alone asked the regulator for a ~A$424m vegetation "step change" for 2026–31 [36].
- **Insurers: not a realistic entry for a newcomer.** Property wildfire scores need regulator acceptance. ZestyAI's Z-FIRE was cleared by the California Department of Insurance, and the FAIR Plan renewed with ZestyAI for four years [18]. ICEYE and Liberty launched building-level parametric wildfire cover in June 2026 [23].
- **Partner programmes exist, but only one is formal.**
  - **LiveEO** runs a public partner programme. It names "Consulting & Advisory Firms" and "Maintenance Service Providers" as partner types for its Treeline vegetation product, and "commission eligibility" comes after certification courses [13]. Rates are not published.
  - **Overstory** has technology integrations (Fulcrum, IQGeo) but no reseller programme that I could find [3].
  - **AiDash and Technosylva:** no public reseller programmes found.
- **Best entry route for this founder: (b), the referral/sales-partner route**, ideally with LiveEO. LiveEO has a formal programme, a Spanish reference (an i-DE/Iberdrola pilot [14]) and a German grid-wide rollout (E.DIS [14]). No Greek, Portuguese or Turkish utility customer of LiveEO was found. That is both the opening and the risk.
- **Weak points for this founder:**
  - He speaks none of Greek, Portuguese, Spanish or Turkish.
  - Utility sales cycles run 6–18 months **(unverified; typical of pilots seen here)**.
  - Big DSOs buy through tenders.
  - A commission may never arrive inside 6 months.
- **Verdict: still "Maybe", slightly upgraded from "Maybe (downgraded)".** It is better than Maybe only if a vendor gives written referral terms **and** at least two Southern European grid owners agree to a demo call. Run a 6-week, ~$0–100 test (below), alongside, not instead of, the EUDR test already recommended.

## Markets

| Region / buyer | Driver | Size / spend evidence | Named buyers of satellite/AI vegetation or wildfire products | How they buy | Fit for small newcomer |
|---|---|---|---|---|---|
| **US large investor-owned utilities** (California, Colorado, Hawaii, Pacific NW) | Liability: Eaton fire (SCE drawing on state fund; California added $18bn to the fund in Sept 2025) [30]; Xcel Marshall fire $640m settlement (Sept 2025) [31]; Hawaiian Electric ~$2bn share of the ~$4bn Maui deal [32] | PG&E 2026–28 plan approved Feb 2026, ~$18.9bn total cost over 3 years (secondary source) [29] | PG&E, SCE, SDG&E, PacifiCorp, Xcel (Technosylva) [10]; SCE (Neara) [20]; Xcel, APS, Portland General (Pano AI) [11] | Multi-year enterprise contracts, RFPs, regulator-scrutinised plans | **Very poor**: incumbents entrenched; requires a US presence and references |
| **US co-ops (~832 distribution co-ops) and public power (1,998 utilities)** [25] | New state laws: Texas HB 145 (co-ops must file a plan; PUC rule in force 4 Dec 2025; liability shield only with an approved plan) [26]; Idaho S1183 (2025), Montana HB 490 (2025), Washington and Oregon plan requirements [27][33][34]; Fix Our Forests Act passed the House [28] | DOE GRIP: Holy Cross + NRECA + 39 co-ops (the "WARN" consortium), ~$96.7m obligated, 2024–2029, includes "satellite-based vegetation management" [24]; LPEA $1.5m grant partly for satellite imaging [24] | Holy Cross, Sho-Me Power, Delaware Electric, Powder River (Overstory) [5]; United Power (AiDash) [b]; Rochelle IL $54k/yr, Denton TX ≤$370,834/5 yr (AiDash) [8][9]; EWEB (Overstory) [6] | Small RFQs, council or board votes, pilots, often grant-funded; free plan templates from APPA and Washington DNR [33] | **Poor for selling software** (vendors already sell direct at low prices). **Some room for plan-writing help**, but engineering firms (e.g. Guidehouse for WA DNR) do this [33] |
| **Canada** | Utility wildfire risk; BC wildfires | No vendor contract found at BC Hydro (only a conventional herbicide contract) [48] | Hydro Ottawa (Overstory) [48]; Pano AI deployed in Canada [11] | Tenders | Poor |
| **Australia** | Bushfire regulation: Energy Safe Victoria fined AusNet and United Energy for clearance failures (Jan 2025) [36] | Powercor proposed ~A$424m vegetation step change 2026–31 (proposal, not decision) [36]; AusNet ~A$331m on maintenance + vegetation in 12 months to Nov 2025 [36] | Powercor uses helicopter LiDAR on 77,000+ km [36]; AiDash has an ANZ director and unnamed pilots [37]; Neara is Sydney-based [20] | Regulated capex/opex, tenders | Poor: LiDAR-heavy, local vendors, far away |
| **Greece** | Power lines linked to 15 of 41 investigated major fires in 2025; HEDNO disputes the share (<1% historically); a mayor plans a negligence suit; 3 arrests over a July 2026 fire started on a **private wind-farm network** [38] | HEDNO investment ~€800m/year (vs €150m in 2019), ~250,000 km of network; €4.79bn plan 2026–30 [38]; Greece's €20m OroraTech satellite fire-detection system (state, not utility) [16]; EU plans €350m more for Greek fire programmes (unclear link) [16] | No HEDNO satellite vegetation vendor found **(unverified; Greek-language tenders not searched)** | State-linked DSO tenders (ESIDIS); private renewable operators buy directly | **Best of the weak options**: urgent, under-served by satellite vendors, close to Montenegro. But he has no Greek, and HEDNO buys by tender |
| **Portugal** | Decree-Law 82/2021: line operators must keep fuel strips (10 m each side for HV/VHV, 7 m for MV); new ICNF rules (Despacho 675/2026) [40] | E-REDES: 2-year fuel-strip contract, ~€19m/year; 179,000 km network, 28,000 km in forest [39] | E-REDES says it already uses drones and satellite images (vendor not named) [39]; EDP was reportedly Overstory's first utility client (2020) **(unverified)** [d] | Public tenders | Medium-poor: law creates steady demand, but the buyer already has tools |
| **Spain** | Fire seasons; EU 2025 record burn [44] | Endesa: €105m summer forest protection + maintenance [41] | i-DE/Iberdrola: LiveEO Treeline pilot (Vizcaya, 2024) and ICEYE radar pilot (June 2026) [14][15]; Red Eléctrica (Overstory) [4] | Innovation pilots, then tenders | Poor: Spanish majors already test the leaders |
| **Italy, France** | EU strategy (March 2026) names power lines among human ignition sources; no binding EU vegetation rule found [44] | — | Terna is pilot user of ESA-backed RELECT (radar damage) [43]; Enedis works with Alteia since 2018 [42] | Tenders, ESA-funded pilots | Poor |
| **Turkey** | İzmir governor blamed power lines for 2025 fires; distributor GDZ denied; 15 m clearance duty in law [45] | Not found | None found | Private regional distributors | Unclear: high political/legal noise; language barrier |
| **Chile, Brazil, South Africa** | Chile's Feb 2024 Valparaíso fires (100+ deaths; cause not linked to lines in sources found) [50]; Brazil storm/tree outages; Eskom veld-fire risk | Not found | Brazil: Hitachi Vegetation Manager launched 2023, local AI start-up Fu2re, AXIA LiDAR+AI [46]; Eskom used satellite fire alerts since 2005 [47] | Tenders | Poor: local players, Portuguese/Spanish needed |
| **Insurers / reinsurers / cat-model vendors** | California crisis: FAIR Plan ~697k policies (June 2026), +157% since Sept 2022 [49] | — | California FAIR Plan, Colorado FAIR Plan, TruStage (ZestyAI) [18]; Green Shield Risk (Technosylva) [10]; Liberty (ICEYE) [23] | Regulator-approved models; multi-year data licences | **Very poor**: needs a filed, validated model |
| **Others** (rail, pipelines, telecom, forestry, governments) | Same liability logic | — | Deutsche Bahn, BPA (LiveEO) [12]; Greek state (OroraTech) [16] | Tenders | Poor-medium; same vendors |

**Notes.**

- **US: the money is real, but the middle is crowded.**
  - The new state laws (Texas, Idaho, Montana, Washington, Oregon) all link a filed or approved plan to liability protection [26][27]. That makes "documented vegetation work" valuable even for tiny utilities.
  - The vendors have already gone downmarket. AiDash won a small-city RFQ at $54k/year [8]. Overstory sells pilots to co-ops. AiDash sells through Business Wire-style launches and has partnered with Technosylva and BurnBot [10].
  - A Montenegro-based newcomer adds little that these sales teams don't already offer, and US buyers expect US insurance, references and site visits **(unverified)**.
  - Industry cost benchmarks: vegetation work itself costs ~$6k–11k per distribution mile per cycle (DOE table) [35]. Helicopter LiDAR costs ~$400–700/mile (LiveEO, vendor claim) [c]. Satellite analytics are sold as the cheaper layer.
- **Greece is the stand-out European driver.** Every 2025–2026 fire season has put HEDNO's lines in the news [38].
  - A new buyer type appeared in 2026: **owners of private medium-voltage networks** (wind/solar farms). The July 2026 fire was traced to a wind-farm network with poor clearing around poles, and three people were arrested [38].
  - These owners have personal criminal exposure and probably no vegetation analytics. That is a hypothesis, not a verified gap.
- **Portugal and Spain** already pay for vegetation work at scale (E-REDES ~€19m/year on fuel strips alone [39]; Endesa €105m [41]). Their majors already run pilots with LiveEO, ICEYE and Overstory [4][14][15].
- **Insurers.** A newcomer cannot sell scores. The only plausible insurer product is one-off **post-fire or pre-bind reports** for small commercial brokers. ICEYE already sells building damage assessment [23].

## Competitors

| Company | Offer | Funding / revenue | Customers (named) | Partner / reseller programme? | Source |
|---|---|---|---|---|---|
| **Overstory** (NL/US) | Satellite + AI vegetation, outage and wildfire risk; tree-level models (Apr 2026) | $43m Series B (Nov 2025, Blume Equity, EIP); ~$68m total **(unverified)** | 6 of 10 largest Americas utilities (claim); Holy Cross, Sho-Me, Delaware Electric, EWEB, Hydro Ottawa, Red Eléctrica | Integrations only (Fulcrum, Sept 2026; IQGeo). No reseller programme found | [1][2][3][4][5][6][48] |
| **AiDASH** (US/India/UK) | Satellite vegetation management, wildfire, storm; grid inspection | ~$83–101m raised; Schneider agreed to buy ~90% at $350m (mid-2026; closing not confirmed) | National Grid (UK), United Power, Rochelle IL, Denton TX | None public; partnerships with Technosylva and BurnBot | [7][8][9][10][a] |
| **LiveEO** (DE) | Treeline (vegetation for grids/rail), SurfaceScout (pipelines), TradeAware (EUDR); own satellites planned | €28m first close (May 2026) | E.DIS (grid-wide), i-DE/Iberdrola pilot, Deutsche Bahn, BPA | **Yes**: partner categories include consulting and maintenance firms; commission after certification; co-sell. Rates not public | [12][13][14] |
| **Technosylva** (US/ES) | Wildfire spread simulation, risk planning | Not found | PG&E, SCE, SDG&E, PacifiCorp, Xcel; 25+ utilities; Green Shield (insurer) | Tech partnerships (AiDASH, Pano AI); no reseller programme found | [10] |
| **Pano AI** (US) | Camera + AI fire detection | $44m Series B (Jun 2025); $89m total | 15+ US utilities incl. Xcel, APS, PGE; 250+ customers | Not found | [11] |
| **Neara** (AU) | 3D network digital twin, LiDAR/satellite risk | $24m Series B (date not confirmed) | SCE; Hawaii work (claim) | Not found | [20] |
| **OroraTech** (DE) | Thermal satellites, fire detection | ~€25m Series B (Oct 2024); extension to €37m **(unverified)** | Greek state (€20m, via ESA tender); 4 satellites launched May 2026 | Not checked | [16] |
| **Dryad Networks** (DE) | Ground sensors for ultra-early detection | €6.3m (Oct 2024); Series B not confirmed | Not checked | Not checked | [17] |
| **ZestyAI** (US) | Property wildfire scores (Z-FIRE) | $15m credit line (2025) | California FAIR Plan, Colorado FAIR Plan, TruStage | Not relevant | [18] |
| **Kettle** (US) | Wildfire reinsurance MGA | $25m Series A (2021); nothing newer found | — | — | [19] |
| **Sharper Shape** (FI/US) | Drone/LiDAR inspection, LiDAR Insights (Aug 2025) | Not found | Not named | Not found | [21] |
| **Rezatec** (UK) | Dams, pipelines, forests (moved away from utilities vegetation) | Lender exited Dec 2024, new owner **(via search summary)** | — | Has a partners page | [22] |
| **ICEYE** (FI) | Radar; wildfire building damage; parametric cover with Liberty | Not checked | Iberdrola pilot (2026), Liberty | Not checked | [15][23] |
| **Others** | Alteia (Enedis), GridEyeS (Lede, Norway), EOinTime (E.ON), Hitachi Vegetation Manager (Brazil), Spottitt (UK) | — | — | — | [42][43][46] |

**Consolidation and failures.**
- The big event is the **Schneider–AiDASH** deal [7]. Its closing was not confirmed when checked.
- Rezatec changed ownership after its lender left [22].
- Kettle and Dryad show no new rounds since 2021 and 2024 respectively, which may mean stagnation **(unverified)**.
- No outright shutdown of a vegetation vendor was found.

**Contract sizes.**
- Small municipal utilities: **~$54k–74k/year** (Rochelle; Denton ≤ $370,834 over 5 years) [8][9].
- Large utilities: undisclosed; multi-year.
- No published per-mile satellite price was found.

## Gaps and entry routes

**Where a small player could still fit (sceptical view).**

1. **Small private grid owners in Southern Europe** (wind/solar farm medium-voltage networks, industrial sites, small island grids). Liability is personal, as the July 2026 Greek arrests show [38]. The big vendors sell to DSOs, not to a 30 km wind-farm line **(unverified that they don't)**. This is the most interesting and least proven gap.
2. **Greek, Portuguese and Turkish DSOs as a local door-opener** for a vendor with no presence there. LiveEO's partner categories fit this exactly [13].
3. **Post-fire burned-area and asset-exposure reports** using free Sentinel-2 and EFFIS data (see primer). These are cheap to make. Buyers are scarce, and ICEYE and Copernicus EMS are free or established for big events [23].
4. **US co-op plan-writing help.** Demand exists (Texas rule from Dec 2025 [26]), but free templates exist (APPA, Washington DNR [33]). Buyers want engineers who know US codes. **Not a fit.**
5. **Data labelling / ground-truth field checks** for vendors in the Balkans or Greece: possible small gigs. No evidence of demand found.

**The three routes compared.**

| | (a) Own product with technical co-founder | (b) Sales/referral partner of a vendor | (c) Service: vegetation-risk / post-fire reports |
|---|---|---|---|
| What it is | Build a vegetation-risk SaaS for small grid owners | Find and qualify Southern European grid owners for LiveEO (or Overstory/AiDASH if they agree); earn commission | Sell one-off reports (corridor vegetation within X m of lines, burned area, exposure) from free Sentinel data + QGIS, plus commercial imagery when paid |
| Cash cost within 6 months | $2k is not enough. Very-high-resolution imagery is needed to see trees near distribution lines (30–50 cm; archive ~$10–22.50/km², minimums apply, see primer). E&O insurance and pilots are on top | ~$0–300 (email, a LinkedIn trial, video calls); travel to Athens optional | ~$0–500 (QGIS free; CDSE free credits; one paid imagery order per paid job) |
| Time to first revenue | 12–24 months **(estimate)** | 6–18 months: commission arrives only after the utility signs and pays **(estimate; utility cycles)** | 1–3 months for a first small job, if a buyer exists **(estimate)** |
| Main risks | No co-founder; competing with $40m+ funded firms; needs EuroHPC/AI only for model training | Vendor declines or has no Southern Europe interest; commission terms unknown; no language skills; HEDNO tenders favour local integrators | 10 m Sentinel pixels cannot show single trees or clearance distances; liability if a report misses a hazard; low prices; looks amateur to utilities |
| Fit for non-technical founder | Poor | **Best** | Medium (needs a part-time GIS contractor for anything serious) |

**Cross-cutting issues.**
- **References:** utilities want named references. Route (b) borrows the vendor's.
- **Insurance:** E&O/professional liability is expected for (a) and (c). For (b) the vendor carries product liability, but the agent agreement may still require cover **(unverified)**.
- **Procurement:** HEDNO and E-REDES require vendor registration and tender documents in the local language. A vendor partner usually bids, not the agent.
- **Sanctions screening** applies to each prospect. Chinese-owned grid assets are acceptable under the founder's policy for this non-GPU business, but **check vendor policy**: LiveEO now also works in defence [12] and may restrict some customers.

## Recommended next step

**6-week test: "Southern European grid-owner door-opener" (cost ~$0–100, ~10 h/week, no sign-ups or payments until terms are seen).** Run it in parallel with the EUDR test, which remains the higher priority.

- **Weeks 1–2: supply side.**
  - Write a one-page proposal: "I introduce and qualify grid owners in Greece, Cyprus, Portugal and Turkey that you don't cover; you close."
  - Send it to the partnership contacts of LiveEO (public programme [13]), Overstory and AiDASH/Schneider.
  - Ask three questions: Do you want these countries? What are the referral or commission terms? Do you need a local entity or insurance?
  - **Go signal:** at least one vendor sends written referral terms.
- **Weeks 2–4: demand side.**
  - List 30 targets:
    - HEDNO regional heads of network maintenance
    - Cyprus's EAC
    - 10 Greek wind/solar operators with their own MV lines (from the regulator's licence registers)
    - E-REDES innovation staff
    - 5 Turkish distributors (GDZ, Toroslar, etc.)
    - island and industrial grid owners
  - Find contacts manually on LinkedIn and company sites.
  - Send a short English message, plus Greek via a paid translator only after a vendor says yes.
  - The offer: "free 30-minute look at vegetation risk on one feeder, using [vendor] data".
- **Weeks 3–5: free sample.**
  - With a vendor's demo, or with free Sentinel-2 data and a contractor at ≤$100, produce one map: a 10 km stretch of line near a 2025 Greek fire, with fuel load and burn scar.
  - Label clearly what 10 m data can and cannot show.
- **Week 6: decide.**
  - **Upgrade to "Do":** written partner terms **and** at least 2 qualified meetings (a utility or grid owner agrees to a vendor demo).
  - **Stay "Maybe":** terms but no meetings, or meetings but no vendor.
  - **Drop:** neither.

Do not build software, buy imagery or form a Greek entity during the test.

## Questions for a lawyer / accountant

1. Can the **US LLC** sign a commission or referral agreement with a German (LiveEO) or Dutch (Overstory) company and be paid for introductions in Greece or Portugal? Does working from Montenegro create a permanent establishment or tax presence there, or in the client's country?
2. Would the **EU Commercial Agents Directive (86/653/EEC)** apply? It covers goods, but some states extend it. If it applies, are there termination indemnities and minimum notice rights? Which governing law should the agreement use?
3. Do Greek or Portuguese **public procurement rules** restrict paid intermediaries or success fees on tenders (HEDNO, E-REDES)? What disclosure is needed, and what are the anti-bribery (FCPA, Greek law) red lines?
4. For route (c) reports: what **disclaimer and liability cap** is enforceable, and is **E&O insurance** available to a US LLC owned by a non-resident living in Montenegro? Roughly what does it cost?
5. Does reselling or sharing vendor outputs or commercial imagery breach **imagery licences** (Airbus/Maxar end-user terms)?
6. Given the 2026 Greek arrests, could advice on vegetation clearance expose the founder to **criminal or civil liability** if a fire later occurs on that line?
7. Accountant: US tax treatment of commission income for a single-member LLC with a non-resident owner (effectively connected income? Form 5472/1120 pro forma). Montenegrin personal tax on the same income.
8. **Sanctions and export control:** any restriction on supplying satellite-derived analytics of critical infrastructure (e.g. Turkish or Cypriot grids) to customers, and on vendors with defence lines?

## Sources

1. ESG Today, "Overstory Raises $43 Million to Help Utilities Avoid Wildfires with AI" — https://www.esgtoday.com/overstory-raises-43-million-to-help-utilities-avoid-wildfires-with-ai/ — checked 2026-11-18 (via search summary)
2. Overstory, Series B announcement (Nov 2025) — https://www.overstory.com/blog/series-b-announcement ; Overstory explorer/pilot page (no pricing shown) — https://www.overstory.com/explorer-pilot — checked 2026-11-18 (pilot page read directly; blog via search summary)
3. TechIntelPro, "Overstory and Fulcrum partner to deliver closed-loop risk reduction" (Sept 2026) — https://techintelpro.com/news/ai/enterprise-ai/overstory-and-fulcrum-partner-to-deliver-closed-loop-risk-reduction ; Cambridge Network, IQGeo and Overstory — https://cambridgenetwork.co.uk/news/iqgeo-and-overstory-provide-state-art-vegetation-management-new-electric-utility-customer — checked 2026-11-18 (via search summary)
4. CaseStudies.com, Overstory and Red Eléctrica — https://www.casestudies.com/company/overstory/case-study/how-overstory-helped-ree-identify-37-species-of-trees-and-other-vegetation-across-13-climate-zones-from-satellite-data — checked 2026-11-18 (via search summary)
5. Holy Cross Energy, Overstory case study (2023) — https://www.holycross.com/wp-content/uploads/2023/04/HCE_OverstoryCaseStudy_2023.pdf ; CB Insights, Overstory customers — https://www.cbinsights.com/company/20treeai/customers — checked 2026-11-18 (via search summary)
6. EWEB, "EWEB invests in satellite-based forestry analytics" (30 May 2024) — https://www.eweb.org/your-public-utility/news/eweb-invests-in-satellite-based-forestry-analytics-for-vegetation-management — checked 2026-11-18 (read directly)
7. ESG Today, "Schneider Electric Acquires … AiDASH for $350 Million" — https://www.esgtoday.com/?p=25069 ; Wilson Sonsini client note — https://www.wsgr.com/en/insights/wilson-sonsini-advises-aidash-on-dollar350-million-acquisition-by-schneider-electric.html — checked 2026-11-18 (via search summary; closing not confirmed)
8. SuperHits 93.5, "Rochelle Approves AIDash Proposal for Vegetation Management Services" (18 Nov 2025) — https://superhits935.com/rochelle-approves-aidash-proposal-for-vegetation-management-services — checked 2026-11-18 (read directly; council minutes not checked)
9. City of Denton, City Council 21 Oct 2025, item ID 25-1880 (AiDash, RFQ 8819, NTE $370,834) — https://denton-tx.granicusideas.com/meetings/4249-city-council-on-2025-10-21-3-00-pm/agenda_items/68f026da44253817560090ab-m-id-25-1880-consider-adoption-of-an-ordinance-of — checked 2026-11-18 (read directly)
10. Utility Dive, Technosylva and AiDASH partnership (21 Aug 2025) — https://www.utilitydive.com/press-release/20250821-technosylva-and-aidash-partner-to-integrate-vegetation-management-and-wildf ; Water Online, Technosylva–Pano AI (3 Feb 2026) — https://www.wateronline.com/doc/technosylva-and-pano-ai-announce-partnership-to-deliver-unified-predictive-real-time-wildfire-intelligence-0001 ; Renewable Energy World on Technosylva customers — https://www.renewableenergyworld.com/?p=80798112690 ; Silicon UK, Green Shield Risk Solutions–Technosylva — https://silicon.co.uk/press-release/green-shield-risk-solutions-partners-with-technosylva-to-revolutionize-wildfire-risk-analysis-for-the-insurance-industry — checked 2026-11-18 (via search summary)
11. Insurance Journal, "Pano AI … Raises $44M Series B" (20 Jun 2025) — https://www.insurancejournal.com/news/west/2025/06/20/828412.htm ; Gunderson Dettmer client note — https://www.gunder.com/en/news-insights/client-news/wildfire-management-pano-ai-announces-dollar44m-series-b — checked 2026-11-18 (via search summary)
12. SpaceWatch.Global, "LiveEO Raises €28M" (May 2026) — https://spacewatch.global/2026/05/liveeo-raises-e28m-to-scale-geospatial-intelligence-across-civil-infrastructure-and-defense/ ; TAM Radar (customers DB, BPA) — https://www.tamradar.com/funding-rounds/liveeo-28m-satellite-intelligence — checked 2026-11-18 (via search summary)
13. LiveEO, "Explore Our Partner Ecosystem" — https://www.live-eo.com/partners (read directly) ; LiveEO, "LiveEO Invites Industry to Join New Partner Program" (Mar 2022) — https://www.live-eo.com/company/press/liveeo-invites-industry-to-join-new-partner-program ; LiveEO job ad, Senior Partner & Business Development Manager — https://www.climatetechlist.com/job/liveeo-senior-partner-business-development-manager-f-m-x-0gGXXGBTLnI4tE — checked 2026-11-18 (last two via search summary)
14. LiveEO, i-DE (Iberdrola) tests Treeline — https://www.live-eo.com/company/press/i-de-iberdrola-spains-distribution-network-company-tests-liveeos-treeline-for-enhanced-vegetation-control ; LiveEO, grid-wide monitoring for E.DIS — https://www.live-eo.com/company/press/liveeo-launches-grid-wide-vegetation-monitoring-for-e-dis — checked 2026-11-18 (via search summary)
15. Iberdrola, investing in ICEYE space technology (June 2026) — https://www.iberdrola.com/press-room/news/detail/iberdrola-investing-space-technology-finnish-company-iceye-strengthen-network-against-extreme-weather-events — checked 2026-11-18 (via search summary)
16. OroraTech, "Greece launches world's first national wildfire satellite system" (May 2026) — https://ororatech.com/resources/news-blog/greece-launches-world-s-first-national-wildfire-satellite-system ; TNW, OroraTech Series B (Oct 2024) — https://thenextweb.com/news/german-startup-ororatech-raises-25-million-wildfire-early-warning-system ; The Recursive, €20m Greece pact — https://therecursive.com/greece-and-ororatech-forge-e20m-pact-to-pioneer-satellite-based-wildfire-system ; Fortune/AP (26 Jun 2026) — https://fortune.com/2026/06/26/greece-wildfire-satellite-ai-eu-funding-ororatech-2026/ — checked 2026-11-18 (via search summary)
17. Silicon Republic, "Dryad Networks raises €6.3m" (Oct 2024) — https://siliconrepublic.com/start-ups/dryad-networks-wildfire-prevention-drones-ai-berlin — checked 2026-11-18 (via search summary)
18. Insurance Journal, "California FAIR Plan Extends ZestyAI Partnership" (17 Jun 2025) — https://www.insurancejournal.com/news/west/2025/06/17/827986.htm ; ZestyAI, CIBC credit facility — https://zesty.ai/news/credit-facility-cibc ; Reinsurance News, Z-FIRE approval — https://www.reinsurancene.ws/zestyais-z-fire-model-gains-approval-for-california-wildfire-risk-assessment/ — checked 2026-11-18 (via search summary)
19. TechCrunch, "Kettle books $25M" (19 Nov 2021) — https://techcrunch.com/2021/11/19/kettle-books-25m-for-its-reinsurance-platform-against-fire-and-other-catastrophes — checked 2026-11-18 (via search summary)
20. Business Wire, "Neara Partners with Southern California Edison" (27 Sept 2023) — https://www.businesswire.com/news/home/20230927480271/en ; ESG Today, Neara $24m — https://www.esgtoday.com/infrastructure-tech-startup-neara-raises-24-million-to-help-utilities-deploy-renewable-energy-reduce-climate-risk/ — checked 2026-11-18 (via search summary)
21. Geo Week News, Sharper Shape LiDAR Insights (Aug 2025) — https://www.geoweeknews.com/sharper-shape-introduces-lidar-insights-solution — checked 2026-11-18 (via search summary)
22. CB Insights, Rezatec — https://www.cbinsights.com/company/rezatec ; Rezatec partners — https://rezatec.com/about/partners — checked 2026-11-18 (via search summary)
23. ICEYE, "Liberty and ICEYE partner to deliver market-first Parametric Wildfire Insurance Cover" (15 Jun 2026) — https://www.iceye.com/newsroom/press-releases/liberty-and-iceye-partner-to-deliver-market-first-parametric-wildfire-insurance-cover — checked 2026-11-18 (via search summary)
24. NRECA, "NRECA, Electric Co-op Consortium Selected for Wildfire Mitigation Infrastructure Funding" — https://www.electric.coop/nreca-electric-co-op-consortium-selected-for-wildfire-mitigation-infrastructure-funding ; HigherGov, DE-GD0000885 — https://www.highergov.com/grant/DEGD0000885 ; LPEA $1.5m grant — https://lpea.coop/safety/we-have-been-awarded-15-million-federal-grant-bolster-wildfire-mitigation-and-grid — checked 2026-11-18 (via search summary)
25. NRECA, Electric co-op fact sheet — https://www.electric.coop/electric-cooperative-fact-sheet ; APPA, 2026 Public Power Statistical Report — https://www.publicpower.org/system/files/documents/2026_Public-Power-Statistical-Report.pdf — checked 2026-11-18 (via search summary)
26. Texas Legislature, HB 145 (89R) enrolled text — https://capitol.texas.gov/tlodocs/89R/billtext/html/HB00145F.htm ; Lloyd Gosselink, implementation of 89th-session bills (PUC rule 16 TAC §25.60, effective 4 Dec 2025) — https://www.lglawfirm.com/now-what-implementation-of-electric-and-utility-bills-from-the-89th-legislative-session/ — checked 2026-11-18 (via search summary)
27. CSG West, "Wildfire and Utilities Legislation" (Feb 2026) — https://csgwest.org/wp-content/uploads/2026/02/Wildfire-and-Utilities-Legislation.pdf ; S&P Global, new wildfire liability laws in western US (Aug 2025) — https://www.spglobal.com/market-intelligence/en/news-insights/research/2025/08/new-wildfire-liability-mitigation-laws-in-effect-across-western-us ; Stateline (22 Apr 2025) — https://stateline.org/2025/04/22/as-wildfires-intensify-utilities-want-liability-protections-but-then-who-pays/ — checked 2026-11-18 (via search summary; bill texts not read; Utah SB 224 date unverified)
28. NRECA, "House-Passed Bill Would Help Co-ops Reduce Wildfire Risks" — https://www.electric.coop/house-passed-bill-would-help-co-ops-reduce-wildfire-risks — checked 2026-11-18 (via search summary)
29. Energy Safety, approval of PG&E 2026–2028 Wildfire Mitigation Base Plan (5 Feb 2026) — https://energysafety.ca.gov/news/2026/02/05/energy-safety-issues-approval-of-pacific-gas-and-electrics-2026-2028-wildfire-mitigation-base-plan/ ; RCRC, PG&E plan cost — https://www.rcrcnet.org/general/pge-releases-2026-2028-wildfire-mitigation-plan/ — checked 2026-11-18 (via search summary)
30. E&E News, "Southern California Edison to tap state wildfire fund for Eaton Fire costs" — https://www.eenews.net/articles/southern-california-edison-to-tap-state-wildfire-fund-for-eaton-fire-costs/ ; Utility Dive, SCE wildfire earnings — https://www.utilitydive.com/news/southern-california-edison-wildfire-earnings/804704/ — checked 2026-11-18 (via search summary)
31. CPR News, Xcel Marshall fire settlement (24 Sept 2025) — https://www.cpr.org/2025/09/24/xcel-energy-marshall-fire-trial-begins/ — checked 2026-11-18 (via search summary)
32. Insurance Journal / Bloomberg, "Hawaiian Electric Finalizes $2 Billion Maui Fire Settlement" (Nov 2024) — https://amp.insurancejournal.com/news/west/2024/11/06/800201.htm — checked 2026-11-18 (via search summary)
33. APPA, Wildfire Mitigation Strategies and Resources for Public Power Utilities (Sept 2025) — https://www.publicpower.org/system/files/documents/Wildfire-Mitigation-Strategies-and-Resources-for-Public-Power-Utilities-September2025.pdf ; Washington DNR, WMP template report (Guidehouse) — https://dnr.wa.gov/sites/default/files/2025-11/rp_electric_utility_wmp_template_development_deployment_report.pdf ; WA UWFPAC minutes Nov 2024 (42 of 62 plans) — https://dnr.wa.gov/publications/rp_uwfpac_minutes_112024.pdf — checked 2026-11-18 (via search summary)
34. Oregon PUC, Wildfire Mitigation Plans 2024 — https://www.oregon.gov/puc/safety/Documents/Wildfire-Mitigation-Plans-2024.pdf — checked 2026-11-18 (via search summary)
35. US DOE, Vegetation Management (Nov 2024) — https://www.energy.gov/sites/default/files/2024-11/111524_Vegetation_Management.pdf — checked 2026-11-18 (via search summary)
36. Powercor, Vegetation management step change, AER 2026–31 proposal (Jan 2025) — https://aer.gov.au/system/files/2025-02/PAL%20ATT%209.02%20%E2%80%93%20Vegetation%20management%20step%20change%20%E2%80%93%20Jan2025.pdf ; Energy Safe Victoria, fines — https://www.energysafe.vic.gov.au/media-centre/news/electricity-companies-fail-keep-trees-away-powerlines-hazardous-bushfire-risk-areas ; Utility Magazine, AusNet $331m — https://utilitymagazine.com.au/ausnet-readies-for-challenging-summer-with-331m-investment/ ; Powercor helicopter LiDAR — https://www.powercor.com.au/media-and-resources/media-centre/powercor-helicopters-scanning-powerlines-over-bendigo-and-central-victoria/ — checked 2026-11-18 (via search summary)
37. Business Wire, AiDash expands in Australia and New Zealand (Sept 2024) — https://www.businesswire.com/news/home/20240904664396/en — checked 2026-11-18 (via search summary)
38. Cyprus Mail/Reuters, "Devastating Greek wildfires stoke fear of faulty power lines" (18 Aug 2026) — https://cyprus-mail.com/2026/08/18/devastating-greek-wildfires-stoke-fear-of-faulty-power-lines (read directly) ; Cyprus Mail, "Greece faces costly grid upgrades as power lines spark wildfires" (25 Sept 2025) — https://cyprus-mail.com/2025/09/25/greece-faces-costly-grid-upgrades-as-power-lines-spark-wildfires ; in.gr, €4.79bn DEDDIE plan (27 Aug 2025) — https://www.in.gr/2025/08/27/english-edition/greece-plans-major-grid-upgrades-protect-forests/ ; dnews.gr, grid under scrutiny — https://www.dnews.gr/eidhseis/news-in-english/604952/greece-s-power-grid-comes-under-scrutiny-as-wildfires-raise-alarm — checked 2026-11-18 (last three via search summary)
39. E-REDES, new ongoing vegetation management contract (9 Apr 2024) — https://e-redes.pt/en/news/2024/04/09/e-redes-launches-new-ongoing-vegetation-management-contract ; E-REDES, "Maintaining energy, preserving the forest" — https://e-redes.pt/en/stories/gestao-da-vegetacao ; Agroportal, E-REDES €14.5m with drones and satellite — https://bo.agroportal.pt/e-redes-investe-145-milhoes-de-euros-na-gestao-da-vegetacao — checked 2026-11-18 (via search summary)
40. Abreu Advogados, Fiscalização da gestão de combustível 2024 — https://abreuadvogados.com/wp-content/uploads/2024/02/Fiscalizacao-da-Gestao-de-Combustivel-2024-1.pdf ; Diário da República, Despacho 675/2026 — https://diariodarepublica.pt/dr/detalhe/despacho/675-2026-1016754080 — checked 2026-11-18 (via search summary; official consolidated text not read)
41. Endesa, €105m forest management, maintenance and grid inspection — https://www.endesa.com/en/press/press-room/news/energy-efficiency/Environmente/105-million-euros-forest-management-maintenance-grid-inspection-summer — checked 2026-11-18 (via search summary)
42. Alteia, "Enedis chooses Alteia for its smart vegetation management program" — https://alteia.com/resources/blog/enedis-chooses-alteia-for-its-smart-vegetation-management-program/ — checked 2026-11-18 (via search summary)
43. ESA Business Applications, RELECT (Terna) — https://business.esa.int/projects/relect ; GridEyeS — https://business.esa.int/projects/grideyes ; Enlit, Lede to use GridEyes — https://www.enlit.world/library/norwegian-dso-lede-to-use-grideyes-for-ai-based-vegetation-management — checked 2026-11-18 (via search summary)
44. European Commission, new approach to rising wildfire threat (25 Mar 2026) — https://commission.europa.eu/news-and-media/news/modernising-our-approach-tackling-rising-wildfire-threat-2026-03-25_it ; Lovguiden summary — https://lovguiden.dk/en/det-offentlige/europa-kommissionen-press-corner/2026-03-25-eus-integrerede-strategi-mod-stigende-skovbrandsrisiko-i-europa — checked 2026-11-18 (via search summary)
45. Turkish Minute, "Power companies cutting corners on safety … fuel Turkey's wildfires" (4 Jul 2025) — https://turkishminute.com/2025/07/04/power-companies-cutting-corners-on-safety-with-little-govt-oversight-fuel-turkeys-wildfires/ ; Bianet, Diyarbakır–Mardin fire — https://bianet.org/haber/electricity-distribution-company-under-scrutiny-after-deadly-diyarbakir-mardin-fire-296763 — checked 2026-11-18 (via search summary)
46. Cenário Energia, Brazilian AI maps tree-fall risk (Feb 2026) — https://cenarioenergia.com.br/2026/02/10/ia-brasileira-mapeia-risco-de-queda-de-arvores-na-rede-para-reduzir-apagoes-durante-temporais/ ; AXIA Energia AI + LiDAR (Jan 2026) — https://cenarioenergia.com.br/2026/01/16/axia-energia-aposta-em-inteligencia-artificial-e-lidar-para-revolucionar-o-monitoramento-de-vegetacao-na-transmissao/ — checked 2026-11-18 (via search summary)
47. Eskom, Technical Note: Fire Management (Oct 2005) — https://www.eskom.co.za/eia/tx/wp-content/uploads/migrated/RoodepoortStrenght/Draft-Basic-Assessment-Report-1600/Technical_Note-Fire_Management-Oct05.pdf — checked 2026-11-18 (via search summary; old)
48. T&D World, Hydro Ottawa and remote sensing — https://www.tdworld.com/vegetation-management/article/55373019/the-trees-are-winning-hydro-ottawa-is-using-remote-sensing-to-fight-back ; BC Hydro herbicide and vegetation control solicitation — https://www.cleat.ai/government/contracts/herbicide-and-vegetation-control-related-services-for-bc-hydro-facilities-40uv — checked 2026-11-18 (via search summary)
49. California Department of Insurance, 2026 press release on the FAIR Plan — https://www.insurance.ca.gov/0400-news/0100-press-releases/2026/release005-2026.cfm ; CDI, Make It FAIR Act announcement (2 Feb 2026) — https://www.insurance.ca.gov/0400-news/0102-alerts/2026/upload/020226-Commissioner-Lara-and-Assemblymember-Calderon-announce-legislation-transforming-the-California-FAIR-Plan.pdf — checked 2026-11-18 (via search summary; the policy count came from a broker site citing CDI data)
50. NASA Earth Observatory, "Inferno Scars Valparaíso" (Feb 2024) — https://earthobservatory.nasa.gov/images/152417/inferno-scars-valparaiso — checked 2026-11-18 (via search summary)

Supplementary references cited by letter:
a. CB Insights, AiDash — https://www.cbinsights.com/company/aidash ; Silicon UK, AiDash and National Grid — https://www.silicon.co.uk/press-release/aidash-launches-first-of-its-kind-full-stack-platform-for-grid-inspection-and-monitoring — checked 2026-11-18 (via search summary)
b. AiDash/T&D World, United Power (May 2023) — https://www.aidash.com/wp-content/uploads/2023/06/2305TDW_AiDash.pdf — checked 2026-11-18 (via search summary)
c. LiveEO on Medium, "LiDAR or Satellite?" — https://medium.com/liveeo/what-technology-for-utility-vegetation-management-lidar-or-satellite-37d0311ea167 — checked 2026-11-18 (via search summary; vendor claim)
d. AI World EU, Overstory Series B story (EDP as first client, citing Inc.) — https://aiworld.eu/story/43-million-series-b-boosts-overstorys-ai-platform-for-preventing-wildfires-and-strengthening-grid-reliability — checked 2026-11-18 (via search summary)
