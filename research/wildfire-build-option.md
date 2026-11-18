# Building a wildfire and vegetation-risk product for Greece, Cyprus, Portugal and Turkey
_Last checked: 2026-11-18_

Re-examines the BUILD route that `wildfire-vegetation-risk-global.md` rejected in favour of referral. Builds on `satellite-imagery-ideas.md` (free data, imagery primer) and `public-compute-for-startups.md` (EuroHPC needs a Montenegrin d.o.o. and an AI training task). Facts marked **(unverified)** could not be confirmed from a primary or reliable source. "Via search summary" in Sources means I read a search-engine summary, not the page itself.

## Summary

- **Direct answer: do not build a satellite/AI software product for grid owners. But a narrow, service-first build is worth testing, and it is a better bet than referral alone.** The earlier "refer, don't build" verdict was right for the big utilities (HEDNO, IPTO, E-REDES, EAC, the Turkish distributors). It was too quick to dismiss a small niche that changed sharply in 2026.
- **What changed in 2026 (the case for building):**
  - A private wind-farm line caused the 31 July 2026 Attica/Boeotia fire. Three people were arrested, including the wind-farm owner, and prosecutors ordered a **nationwide investigation of every wind farm in Greece** [1][2].
  - Greek preliminary data blame grid-linked fires for ~75% of the area burned in 2026 [3].
  - The Greek Fire Service issued **Circular 60013/Φ.701.45.4/2026** on fire protection for ground-mounted PV parks (October 2026). It requires a **Fire Risk Assessment Study**, an emergency plan and measures for the park "and its surrounding area" [4]. The full text is paywalled; widths and deadlines are **(unverified)**.
  - These owners have personal criminal exposure, small assets (one wind farm's line was 4 km overhead [1]), and no in-house GIS team **(unverified)**. The big vendors sell grid-wide subscriptions to utilities, not €1,000 reports to a 20 MW park owner.
- **Best first segment and country:** **Greece, private renewable owners** (wind farms with their own medium-voltage lines, then ground-mounted PV parks), sold through or with a **Greek licensed engineer or O&M contractor**. **Cyprus** is the second test market because business there runs in English.
- **Do not start with:** HEDNO, IPTO, E-REDES, EAC or Turkish distributors. They buy by tender and already run their own drone, LiDAR or satellite programmes [5][6][7][8]. In Turkey, AiDASH has a partnership with Sabancı (co-owner of Enerjisa) [9], and the regulator rewards local software [10].
- **The MVP is a "pre-fire-season vegetation and fire-exposure pack" per site, not software.** It contains a map and a ranked list of spans or fence sections, made by hand from free layers, client-supplied line routes and, where needed, one paid very-high-resolution (VHR) image or a drone flight. A contractor can make one in about 2–4 days once the method exists **(estimate)**.
- **Resolution is the hard limit.** Sentinel-2 (10 m) cannot see single trees near a line. Span-level work needs ~30–50 cm imagery. Pléiades Neo 30 cm archive costs **~$22.50/km²**, with a **25 km² minimum**, so ~$560 per site from archive. New tasking costs **~$42.50–63.75/km²** with a **100 km² minimum** (~$4,250+) [11][12]. For one small site, a drone flight may beat satellite.
- **Cost:** ~$0–300 for the 6-week test. ~$2,000–5,000 to reach 3 paid pilots (contractor time, imagery, translation). That is above the $2,000 budget unless the first pilots are paid upfront or a technical partner takes equity.
- **Conditions for "build":** (1) a Greek engineering or O&M partner who signs or co-delivers; (2) at least 3 owners who pay ≥€500 per site upfront before any software is written; (3) written "screening, not certification" terms with a liability cap, and an insurer willing to cover it.
- **Recommendation: hybrid.** Run the 6-week build test below, aimed at Greek private renewable networks. Refer any utility-scale lead to LiveEO or Overstory. Build software only after month 6, and only if paid repeat demand exists.

## Buyers by country

| Country | Buyer | Legal / liability driver | Current vendor (known) | Budget evidence | Fit for this founder |
|---|---|---|---|---|---|
| Greece | **Private wind-farm owners with their own MV lines** | 31 Jul 2026 fire from a private wind-farm line; 3 arrests; operations suspended; nationwide prosecutor-ordered probe of all wind farms [1][2] | None found | None published. Greece has ~6.0 GW of wind (June 2026) [13]; number of private overhead lines not found | **Best**: urgent, personal criminal exposure, small assets, direct buying (no tenders) |
| Greece | **Ground-mounted PV parks** (PPC Renewables, Metlen, HELLENiQ, Principia and many small owners) | Circular 60013/2026: Fire Risk Assessment Study, emergency plan, measures around the park [4]; 2024 ministerial decision on perimeter planting zones (≥10 m for large parks) [14] | Local fire-safety engineers are the likely suppliers **(unverified)** | ~13 GW of PV reported by May 2026 (figures conflict) [13]; price per study unknown | **Good** as a data layer for the engineers who write the studies; poor as a standalone if the study must be signed by a Greek-licensed engineer **(unverified)** |
| Greece | HEDNO / DEDDIE (distribution) | Grid-linked fires; HEDNO staff arrested after the Crete fire; lawsuits over grid fires rose from 369 to 681 in 2024 [3] | Drone pilot (ALTITUDE) and a LiDAR-based 3D network model [5]; ~€3bn works tender in 37 lots including tree cutting **(date unclear)** [15] | ~€800m/yr investment (earlier file) | Poor: tenders in Greek; refer to vendor |
| Greece | IPTO / ADMIE (transmission) | July 2026 memorandum with the civil-protection ministry: firebreaks along HV lines, Fire Service gives yearly priority map; ADMIE pays [16]; drone surveillance pilot [17] | In-house, drones | Not disclosed | Poor |
| Cyprus | EAC (distribution); TSO Cyprus; PV parks | Power-line short circuits caused 7% of forest fires 2015–2024 (10% in 2024); at least 5 network fires in 2026 [18]; 2025 Limassol fire destroyed ~500 pylons [19] | EAC patrols lines in state forests Feb–June, trims with the forestry department [19][18] | 267 km of overhead lines inside state forests, 3,433 km near forests [19] | **Medium**: English works; EAC is small and in-house; private PV parks are the real target **(demand unverified)** |
| Portugal | E-REDES, REN, private renewables | Decree-Law 82/2021: line operators keep fuel strips (earlier file: 10 m HV, 7 m MV); ICNF technical rules updated 2026 [20] | E-REDES runs "Earth Observation for Vegetation Management" and its own AI tool, Analytics4Vegetation [6]; satellite audits of clearing work; ~€14.5m on inspection and fuel strips [21] | 179,000 km network, 28,000 km in forest [6] | Poor for utilities (already served); private PV unclear; Portuguese needed |
| Turkey | 21 private distributors (Enerjisa, CK Enerji, Aydem/GDZ, Toroslar…), TEİAŞ | EPDK 2026–2030 tariff period: forest pruning made mandatory planned maintenance, **annual** maintenance in forest areas, fines for neglect; maintenance budget ~2.1× in real terms [10]. Power lines started 4% of fires but caused 20% of burned forest (OGM data, via press) [22]. Ombudsman told GDZ to compensate victims and inspect more often [22] | Enerjisa expands its own drone fleet [23]; AiDASH–Sabancı partnership covering EMEA, citing Enerjisa (2024) [9] | Not disclosed | Poor-medium: real money and a new rule, but language, local-software incentive [10] and large incumbent partners |

**Notes.**
- **Greek private networks are the only segment where all of these hold at once:** a fresh legal shock, a named person who can go to jail, no tender rules, and no known vendor. The wind-farm line that burned was 42 km long, but only **4 km were overhead** [1]. That is too small for an enterprise satellite subscription. It is the right size for a one-off pack.
- **The PV circular is a new compulsory document, but probably an engineer's job.** If the Fire Risk Assessment Study must be signed by a Greek-licensed engineer (likely, **unverified**), the founder cannot sell the study itself. He can sell the **map and evidence annex** that goes into it, to the engineers, or partner with one engineering firm.
- **No sign that LiveEO, Overstory or AiDASH serve Greek private renewables** (searched English and Greek; **absence of evidence, not proof**). AiDASH's Sabancı tie means Turkey is not open ground [9].
- **Insurers.** Insurers ask solar sites for vegetation plans (cut height, monitoring frequency) [24]. Some have added wildfire exclusions [24]. No Southern European insurer rule requiring third-party reports was found **(unverified)**. Treat insurer reports as an add-on, not the first market.

## What the product would be

**MVP: "Fire-season vegetation and exposure pack" for one private line or one park.**

1. **Inputs from the client:** line route (KML/DWG), pole positions, fence outline, last clearing dates. Do not rely on OpenStreetMap: it shows only **~94 km of 10–25 kV lines in all of Greece** (13,195 km of lines in total). Private MV lines are essentially missing. Portugal (61,533 km) and Turkey (70,221 km) are better mapped, but MV coverage is patchy [25].
2. **Free context layers:**
   - Sentinel-2 vegetation dryness and greenness (10 m, every ~5 days)
   - ESA WorldCover land cover (10 m)
   - Meta/WRI 1 m global canopy height map (free for commercial use; reported mean error ~2.8 m; imagery mostly 2009–2020, so it is stale) [26]
   - EFFIS fire danger and past burned areas
   - Greece's National Forest Fire Risk Map (approved Dec 2025; puts each municipality in a low, medium or high class) [27]
   - slope and aspect from a free elevation model
3. **Span-level evidence:** one recent VHR image (30–50 cm) or a drone orthophoto of the corridor. The analyst marks trees and shrubs within the legal strip, pole bases that are not clear, and dry fuel next to the fence.
4. **Output:** a PDF and a web map. Each span or fence section is ranked red, amber or green, with photos or image chips, the legal reference and a recommended action. It ends with a clear "screening, not certification" statement.

**Open tools that cut build effort:** QGIS (free), DeepForest (open-source tree-crown detection), Segment Anything-based geo tools, the Meta/WRI canopy model, which can be locally tuned with 10–15 field points [26], Copernicus Data Space (free data plus 10,000 openEO credits a month; commercial-use terms **unverified**). **No model training is needed for the MVP.** EuroHPC Fast Lane is irrelevant until a later stage, and it would need a Montenegrin d.o.o.

**Resolution and imagery cost.**

| Source | Pixel | Sees single trees near a line? | Price (list, reseller) | Minimum |
|---|---|---|---|---|
| Sentinel-2 | 10 m | No: shows dryness and fuel type only | Free | — |
| PlanetScope | ~3 m | Groups of trees, not clearance | Subscription; small tiers ~$2,700–5,100/yr **(unverified)** | Area plans |
| Planet SkySat archive | 50 cm | Mostly yes | ~$15–35/km² **(vendor blog, unverified)** | 25–100 km² depending on reseller [28] |
| Pléiades (1A/1B) archive | 50 cm | Mostly yes | ~$10/km² (earlier file) | 5–25 km² by reseller |
| Pléiades Neo archive | 30 cm | Yes | **$22.50/km²** (LandInfo, Jan 2026) [11] | **25 km²**, at least 5 km wide [12] |
| Pléiades Neo new tasking | 30 cm | Yes, current season | ~$42.50–63.75/km² [11] | **100 km²** [11][29] |
| Drone RGB / LiDAR | 1–5 cm | Yes, with heights (LiDAR) | Local quote needed **(unverified)** | Per day; Greek providers exist [30] |

**Corridor maths.**
- 1,000 km of line × 100 m corridor = 100 km². Pléiades Neo archive costs ~$2,250 at that size; fresh tasking costs ~$4,250–6,400.
- A 4 km private overhead line × 100 m = 0.4 km². But the 25 km² minimum turns that into **~$560 per site** from archive, and the archive may be one to three years old.
- Fresh tasking for one small site (100 km² minimum) costs **~$4,250+**, which kills the economics.
- So, for single sites, use **archive VHR for screening and a local drone flight for "this season"** proof. Group several sites in one region to share a tasking order.

**Accuracy the buyer will expect.**
- Utilities expect validated tree-height and clearance error (LiDAR is the benchmark).
- A private owner facing a prosecutor needs something different: dated, traceable evidence that the strip was checked and cleared.
- The MVP should promise **"find and rank likely problems, then field-verify,"** not "measure clearance to ±1 m."
- Validate on the first 3 pilots by ground checks (photos at 20–30 random spans) and report hit rate honestly.
- Do not use Google Earth/Maps imagery in paid reports: licence terms generally forbid it **(unverified for this use)**.

**Narrower angles, ranked:**
1. Wind-farm and private MV line pre-season packs (best fit).
2. Map and evidence annex for PV Fire Risk Assessment Studies, sold to engineers (good if the circular applies to existing parks; **unverified**).
3. Post-fire evidence packs: burned area, timeline, pre-fire vegetation state, for owners, lawyers and loss adjusters. Low volume, but high value per case **(unverified)**, and legally sensitive.
4. Insurer pre-bind reports for renewable assets (later).

## Team, cost and funding

**Who is needed.**
- **Technical partner (contractor first, co-founder later).**
  - QGIS and Python (rasterio/geopandas)
  - Sentinel-2 processing; ordering and orthorectifying VHR imagery
  - DeepForest or canopy-height tools
  - basic understanding of MV line clearances
  - ideally ground-truth fieldwork
  - Sources from the earlier file: BioSense (Novi Sad), University of Belgrade geodesy, Geosemantica (Tivat), GILab (Belgrade).
- **Greek partner:**
  - a licensed engineer or O&M firm that serves wind and PV parks (for example a drone-inspection company such as I.D.S., Athens [30]);
  - brings Greek-language delivery, site access and the legal signature;
  - pay them by revenue share.

**Costs (estimates unless cited).**
- Contractor rates: Upwork GIS developers median $20–30/h; a Greek remote-sensing/ML freelancer listed at $20/h; client posts $15–60/h [31]. The MVP method and first template take ~40–60 h ≈ **$800–1,800**. Each further pack takes ~16–24 h ≈ $400–700.
- Imagery: $0 (free layers only) to ~$560 per site (Neo archive), or a drone day (quote needed).
- Tools: QGIS, CDSE and Sentinel are free. Avoid Google Earth Engine commercial plans ($500/month).
- Greek translation of a one-page offer and sample: ~$50–150 **(unverified)**.
- Professional indemnity: UK low-risk policies start ~£250/yr. Engineering-type risk runs into "thousands" [32]. Wildfire exclusions are possible **(unverified)**.
- **Total to first 3 paid pilots: ~$2,000–5,000.** Feasible only with upfront payment from pilots, or a partner on equity.

**Can the US LLC sell?** For private Greek or Cypriot companies, probably yes: a B2B service invoice, with the EU reverse-charge VAT treatment usual for B2B services (**accountant to confirm**). Public utilities (HEDNO, EAC, E-REDES, Turkish DSOs) need tender registration, local-language documents and often a local entity or bidding partner. Leave those to a vendor or partner. A Montenegrin d.o.o. is needed for EU and Montenegrin grants and for EuroHPC [see `public-compute-for-startups.md`].

**Funding that could pay for the build.**

| Source | Open to founder? | Amount / dates | Fit |
|---|---|---|---|
| Montenegro Innovation Fund (early-stage start-ups) | Yes, via d.o.o. or team | Up to €30,000 (90%) + €5,000 mentoring (2024 round); calls of €350,000 total in 2023 (closed 20 Oct) and 2024; **no 2026 call found** [33] | Best cash source once there is a paying pilot |
| EIC Accelerator | Yes (ME associated), via d.o.o. | Short proposals any time; 2026 full-proposal cut-offs (Jan–Nov 2026) passed; 2027 dates conflict (3 Feb or 20 Jan 2027) **(unverified)** [34] | Too early; needs traction and a team |
| Horizon Europe (Cluster 5/6/3) | Yes, as a small consortium partner | No 2026–27 topic on wildfire risk to energy networks found; CL5-2026-11 energy call closes 1 Dec 2026 (PV, AI-ready energy datasets) [35] | Low; only as a subcontractor to a consortium **(unverified)** |
| ESA business applications / CASSINI | ESA: no Montenegro/Serbia agreement found; CASSINI excludes ME for EO-led entries (earlier file) | — | No |
| EDP / Free Electrons | Global, but wants funded start-ups with pilots | 2026 call closed 31 Jan 2026; 2027 call **(unverified)** [36] | Later |
| Enerjisa İVME open innovation; ELDER "Big Bang" challenge (Turkey) | Open calls; rules for foreign firms **(unverified)** | Past İVME deadline 7 March (year unclear); a 2026 distribution competition paid 550,000 TL to 3 winners of 423 [37] | Later, only with a Turkish partner |
| EuroHPC AI Factories Fast Lane | Via d.o.o. only | Free GPU time, 1–3 months | Not needed for the MVP |

## Build vs refer vs hybrid

| | **Build (staged: service → software)** | **Refer (vendor partner)** | **Hybrid (recommended)** |
|---|---|---|---|
| What | Sell site packs to Greek private renewables; software later | Introduce utilities to LiveEO/Overstory for commission | Build the private-network niche; refer utility leads |
| Time to first revenue | 2–4 months if owners pay for a pre-season pack (Jan–Apr) **(estimate)** | 6–18 months (utility cycle) | 2–4 months |
| Money needed | $2–5k to 3 pilots; $30–100k for real software (grant/investor) | ~$0–300 | $2–5k |
| Probability of ≥€20k revenue by month 18 (my judgement) | ~15–20% | ~10–15% | ~25% |
| Upside | Owns customers and data. Could grow into an "Eastern Med private-grid fire compliance" tool. Exit to a vendor or engineering firm | Commission only; vendor owns the client | Both, and referrals add credibility |
| Key risks | A local drone/engineering firm does it cheaper; Greek licensing; **liability if a mapped line later burns**; seasonal demand; founder has no Greek | Vendor declines; no language; tenders | Split focus; same liability risk |
| Liability | High: E&O cover and a contract cap needed; criminal-case subpoenas possible **(lawyer)** | Low | Medium–high |

**Honest judgement.**
- A **software** product competing with Overstory, AiDASH or LiveEO for utilities is not viable for this founder. They have $40m+ funding, reference customers and existing pilots in the region [6][9].
- A **service-first niche build is viable only if** three things hold:
  - a Greek partner with an engineering licence or O&M access co-delivers;
  - owners pay before the 2027 fire season;
  - the founder accepts that the moat is **speed, price and paperwork**, not technology.
- The main threat is not LiveEO. It is a Greek drone or fire-safety firm adding the same map to its existing service. Hence the recommendation to **partner with such firms, not fight them**.

## Recommended plan

**6-week build test (≈$0–300; no company formation, no imagery purchase, no sign-ups).**
- **Week 1: make the sample.**
  - With a contractor at ≤$150, or alone in QGIS, make one anonymised sample pack for a public-domain example: a short overhead line or fence near a 2025–2026 burn scar.
  - Use only free layers: Sentinel-2, WorldCover, the 1 m canopy height map, EFFIS and the Greek risk map.
  - Show span ranking, and state what free data **cannot** show.
  - Do not name or depict a real company's asset without permission.
- **Week 2: build the target list.**
  - **25 Greek wind/PV owners and O&M firms:** members of the wind association (ELETAEN) and the PV association (HELAPCO); listed operators such as PPC Renewables, Metlen, HELLENiQ Renewables, Principia and Terna/Masdar; smaller independent owners.
  - **5 Greek fire-safety engineering firms** that will write Circular 60013 studies.
  - **5 Cypriot PV owners.**
  - Screen each for sanctions.
- **Weeks 3–5: run 15 conversations in English.**
  - Use a Greek translator for the one-pager (~$100).
  - Ask:
    - Did the July 2026 probe or Circular 60013 change what you must document?
    - Who maps vegetation on your line or fence today, and at what cost?
    - Would you pay €500–1,500 per site for a pre-season pack delivered by March 2027?
    - Must a Greek engineer sign it?
  - Offer **one free pilot pack** to the first owner who shares a line route.
  - Ask one Greek drone/O&M firm about a revenue-share partnership.
  - In parallel, send the referral proposal to LiveEO (the hybrid part).
- **Week 6: go/no-go gate.**
  - **GO (build):** ≥5 of 15 confirm a documentation need; ≥2 commit to a paid pilot at ≥€500 (written order or deposit); 1 Greek partner agrees to co-deliver.
  - **PIVOT:** engineers want the annex but owners do not, so sell to engineers only. Or Cyprus responds better than Greece.
  - **STOP:** nobody pays, or a Greek firm already sells this at under €300.

**Months 2–6 (Dec 2026–Apr 2027: pre-season window).**
- Deliver 3–5 paid pilots before May 2027, the start of the fire season.
- Use archive VHR or partner drone flights.
- Field-check 20–30 spans per pilot and publish the hit rate.
- Get a lawyer's terms (screening only, liability cap) and a PI insurance quote **before** the first paid delivery.
- **Gate (end Apr 2027):** ≥€3,000 collected, ≥1 owner asks for a repeat or a second site, no unresolved liability issue.

**Months 6–18.**
- Form the Montenegrin d.o.o. and apply to the Montenegro Innovation Fund (≤€30k) for a semi-automated pipeline and a customer web map.
- Bring in a technical co-founder on equity.
- Add Cyprus. Add Turkey only with a Turkish partner, aiming at private renewables, not distributors.
- Consider EuroHPC Fast Lane only if training a species, fuel or canopy model becomes the bottleneck.
- **Gate (month 18):** ≥15 paying sites and ≥€20k revenue → seek seed or EIC. Otherwise fold the client list into a vendor or engineering partnership.

## Questions for a lawyer / accountant

1. Under Greek law, could a third-party vegetation screening report that missed a hazard expose the founder or the LLC to criminal or civil liability after a fire? What disclaimer, liability cap and governing law hold up?
2. Does Circular 60013/2026 apply to existing PV parks, and must the Fire Risk Assessment Study be signed by a Greek-licensed engineer (TEE member)? Are there similar written rules for wind-farm MV lines (strip widths, deadlines)?
3. Can a US LLC owned by a Montenegro resident invoice Greek and Cypriot companies for reports? Does reverse-charge VAT apply? Does working from Montenegro create a permanent establishment?
4. Will an insurer write professional indemnity for wildfire-related screening, and at what limit and premium? Are wildfire exclusions standard?
5. Imagery licences: may Pléiades or SkySat derivatives be included in client reports and shared with authorities or courts?
6. If a report is requested in a criminal investigation, what are our duties, and how do we protect client confidentiality?
7. Revenue-share with a Greek engineering partner: is it allowed, and does it make us their subcontractor for professional-liability purposes?
8. Accountant: when should the d.o.o. be formed relative to the Innovation Fund call, and how do LLC and d.o.o. revenues stay separate?

## Sources

1. Balkan Green Energy News, "Wildfire in Greece sparks nation-wide wind farm investigation" (11 Aug 2026) — https://balkangreenenergynews.com/wildfire-in-greece-sparks-nation-wide-wind-farm-investigation/ — checked 2026-11-18 (read directly)
2. Protothema, "Operation of wind farm in Boeotia suspended… three defendants remanded" (7 Aug 2026) — https://en.protothema.gr/2026/08/07/operation-of-wind-farm-in-boeotia-suspended-due-to-major-fire-three-defendants-remanded-in-custody/ ; To Vima, "Nationwide probe into wind farms after Boeotia fire" — https://www.tovima.com/society/nationwide-probe-into-wind-farms-after-boeotia-fire/amp/ — checked 2026-11-18 (via search summary)
3. Brussels Signal, "Greece's ageing power grid accounts for 75 per cent of land burned this year" (Aug 2026) — https://brusselssignal.eu/2026/08/greeces-ageing-power-grid-accounts-for-75-per-cent-of-land-burned-this-year/ — checked 2026-11-18 (read directly)
4. OENET, Εγκύκλιος 60013 οικ. Φ.701.45.4/2026, Πυροπροστασία φωτοβολταϊκών σταθμών επί εδάφους στην ύπαιθρο (22 Oct 2026) — https://www.oenet.gr/online/oen/item/139411-piroprostasia-fotovoltaikon-stathmon-paragogis-ilektrikis-energeias-epi-edafous-stin-ipaithro — checked 2026-11-18 (summary read; full text paywalled)
5. E.DSO, ALTITUDE drones (HEDNO pilot) — https://edsoforsmartgrids.eu/radar/drones ; E.DSO, 3D digital model success case — https://edsoforsmartgrids.eu/success_cases/3d-digital-model — checked 2026-11-18 (via search summary)
6. E-REDES, "Earth Observation for Vegetation Management" — https://www.e-redes.pt/en/energy-transition-innovation-and-development/inovative-projects/vegetation-management-through — checked 2026-11-18 (read directly); E.DSO, Analytics4Vegetation (Oct 2024) — https://edsoforsmartgrids.eu/content/uploads/2024/10/2.-e.dso-success-cases_e-redes-pt_analytics4vegetation-final.pdf — (via search summary)
7. Cyprus Mail, "Electricity cables continue to pose a significant fire risk" (11 Oct 2026) — https://cyprus-mail.com/2026/10/11/electricity-cables-continue-to-pose-a-significant-fire-risk — checked 2026-11-18 (read directly)
8. Ayedaş/Enerjisa, drone fleet press release — https://ayedas.com.tr/basin-bulteni/zor-kosullarda-hizli-mudahale-enerjisa-dagitim-sirketleri-drone-filosunu-buyutuyor/4881 — checked 2026-11-18 (via search summary)
9. Business Wire, AiDASH and Sabancı Holding (25 Mar 2024) — https://www.businesswire.com/news/home/20240325842637/en — checked 2026-11-18 (via search summary)
10. Forbes Türkiye, "EPDK 2026-2030 elektrik dağıtım yol haritasını belirledi" (1 Jan 2026) — https://www.forbes.com.tr/para-yatirim/epdk-2026-2030-elektrik-dagitim-yol-haritasini-belirledi-yatirim-butcesi-1-5-katina-cikti — checked 2026-11-18 (read directly)
11. LandInfo, imagery price sheet (Jan 2026) — https://landinfo.com/wp-content/uploads/Imagery_LandInfo_202601-1.pdf ; LandInfo pricing page — https://landinfo.com/satellite-imagery-pricing/ — checked 2026-11-18 (via search summary)
12. ESA Earth Online, SPOT/Pléiades data terms of applicability (25 km² minimum, 5 km width) — https://earth.esa.int/eogateway/documents/d/earth-online/spot-pleiades-data-terms-of-applicability ; Apollo Mapping, Pléiades Neo — https://apollomapping.com/pleiades-neo-satellite — checked 2026-11-18 (via search summary)
13. To Vima, "Greece's wind energy capacity tops 6 GW" — https://www.tovima.com/climate/greeces-wind-energy-capacity-tops-6-gw-for-first-time/ ; PV Europe, Greece renewables 2026 — https://www.pveurope.eu/markets/greece-renewables-set-record-4-gw-2026-storage-lags — checked 2026-11-18 (via search summary)
14. e-nomothesia, ΥΑ ΥΠΕΝ/ΔΙΠΑ/59842/4142/2024 (planting zones around PV) — https://www.e-nomothesia.gr/energeia/ya-upen-dipa-59842-4142-2024.html — checked 2026-11-18 (via search summary)
15. Newmoney, ΔΕΔΔΗΕ €3bn works tender incl. αποψιλώσεις — https://www.newmoney.gr/roh/palmos-oikonomias/energeia/deddie-ergolavia-mamouth-e3-dis-gia-erga-diktiou-smart-meters-ke-apopsilosis/ — checked 2026-11-18 (via search summary; date unclear)
16. Powergame, ministry–ADMIE fire-protection memorandum (3 Jul 2026) — https://www.powergame.gr/green-power/1381726/pyroprostasia-synergasia-ypourgeiou-klimatikis-krisis-me-admie-gia-tin-enischysi-ton-energeiakon-ypodomon/ — checked 2026-11-18 (read directly)
17. Powergame, ΑΔΜΗΕ drone surveillance pilot — https://www.powergame.gr/green-power/1042920/admie-pilotiko-programma-gia-24ori-epitirisi-ton-ypodomon-me-drones/ — checked 2026-11-18 (via search summary)
18. = 7 (Cyprus Mail, Oct 2026)
19. Cyprus Mail, "Efforts underway to reduce risk of wildfires" (30 Mar 2025) — https://cyprus-mail.com/2025/03/30/efforts-underway-to-reduce-risk-of-wildfires ; Cyprus Mail, Limassol fire pylons (Jul 2025) — https://cyprus-mail.com/2025/07/29/more-than-half-of-limassols-fire-damaged-electricity-pylons-now-replaced — checked 2026-11-18 (via search summary)
20. ProCiv, DL 82/2021 framework — https://prociv.gov.pt/media/ahofecar/dl-82-quadro-geral.pdf ; Diário da República, Despacho 675/2026 — https://diariodarepublica.pt/dr/detalhe/despacho/675-2026-1016754080 — checked 2026-11-18 (via search summary; strip widths for solar parks not confirmed)
21. Agroportal, E-REDES €14.5m vegetation management — https://bo.agroportal.pt/e-redes-investe-145-milhoes-de-euros-na-gestao-da-vegetacao — checked 2026-11-18 (via search summary)
22. Evrensel (4 Jul 2025) — https://www.evrensel.net/haber/559922/ozellestirme-cetesi-ormanlari-yakiyor ; 24 Saat, KDK decision on GDZ — https://www.24saatgazetesi.com/kdk-karari-uzerinden-bir-ay-gecti-orman-yanginlariyla-baglantili-elektrik-hatlari-icin-denetim-cagrisi — checked 2026-11-18 (via search summary; direct fetch blocked)
23. = 8
24. pv magazine, "How to protect solar assets from wildfires" (21 Aug 2026) — https://www.pv-magazine.com/2026/08/21/how-to-protect-solar-assets-from-wildfires/ (read directly) ; Willis Towers Watson renewable market review (insurers ask for vegetation plans) — https://willistowerswatson.turtl.co/story/renewable-energy-market-review-2021-gated/page/20 ; Risk & Insurance, "Beyond hail" — https://riskandinsurance.com/beyond-hail-the-new-risks-reshaping-insuring-solar-power/ — checked 2026-11-18 (last two via search summary)
25. OSM Wiki, Power networks/Greece — https://wiki.openstreetmap.org/wiki/Power_networks/Greece ; OpenInfraMap stats Greece/Portugal/Turkey — https://openinframap.org/stats/area/Greece , https://openinframap.org/stats/area/Portugal , https://openinframap.org/stats/area/Turkey ; OSM Wiki Power networks/Portugal — https://wiki.openstreetmap.org/wiki/Power_networks/Portugal — checked 2026-11-18 (via search summary)
26. Mongabay, Meta/WRI canopy height map (Apr 2024) — https://news.mongabay.com/2024/04/ai-model-maps-global-tree-canopy-heights-in-hi-res-with-carbon-counting-in-mind/ ; ESG News, Meta/WRI launch — https://esgnews.com/meta-wri-and-land-carbon-lab-launch-global-ai-powered-tree-canopy-height-map — checked 2026-11-18 (via search summary; 2.8 m error from one outlet)
27. Naftemporiki, national fire-risk map approved, three municipal categories — https://www.naftemporiki.gr/green/climate/2041152/pyrkagies-egkrithike-o-chartis-ektimisis-kindynoy-se-treis-katigories-katatassontai-oi-dimoi/ ; Forin, approval of the map — https://www.forin.gr/articles/article/88013/upourgeio-periballontos-upegrafh-h-egkrish-tou-ethnikou-xarth-ektimhshs-kindunou-dasikwn-purkagiwn — checked 2026-11-18 (via search summary)
28. Apollo Mapping, SkySat 50 cm minimum order — https://apollomapping.com/blog/new-minimum-order-announcement-for-50-cm-skysat-imagery ; UP42 SkySat — https://docs.up42.com/data/skysat ; Geopera cost guide (vendor) — https://geopera-website.pages.dev/blog/satellite-imagery-cost-guide — checked 2026-11-18 (via search summary)
29. UP42, tasking minimum charges — https://docs.up42.com/data/tasking-min-charges — checked 2026-11-18 (via search summary)
30. DJI Enterprise, I.D.S. and Eunice wind-farm drone inspections — https://enterprise-insights.dji.com/user-stories/wind-turbine-inspection-ids?hsLang=en — checked 2026-11-18 (via search summary)
31. Upwork, GIS developer cost — https://www.upwork.com/hire/gis-developers/cost/ ; Upwork remote-sensing job post — https://www.upwork.com/freelance-jobs/apply/Remote-Sensing-Data-Analysis_~022068993208198897892/ — checked 2026-11-18 (via search summary)
32. GetIndemnity, PI insurance cost benchmarks (UK) — https://getindemnity.co.uk/professional-indemnity/cost — checked 2026-11-18 (via search summary)
33. Biznis.rs, Montenegro Innovation Fund early-stage call €350,000 — https://biznis.rs/vesti/region/za-podrsku-ranoj-fazi-razvoja-startapa-350-000-evra/ ; Fund Q&A (2024) — https://biznis-api.gov.me/media/files/1717159015-pitanja-i-odgovori-rana-faza-razvoja-startapova-2.docx — checked 2026-11-18 (via search summary)
34. EIC, Accelerator FAQ (2026 cut-offs) — https://eic.ec.europa.eu/eic-frequently-asked-questions/faqs-eic-accelerator_en ; Deloitte Malta, EIC Accelerator 2027 — https://www.deloitte.com/mt/en/services/tax/perspectives/gi3/eic-accelerator-2027-call.html — checked 2026-11-18 (via search summary)
35. Innovate UK Business Connect, Horizon Europe 2026–27 Cluster 5 — https://iuk-business-connect.org.uk/opportunities/horizon-europe-2026-27-climate-energy-and-mobility-cluster-5/ ; CINEA call page — https://cinea.ec.europa.eu/funding-opportunities/calls-proposals/horizon-europe-eu1767-million-projects-supporting-cross-sectoral-solutions-climate-transition-and_en — checked 2026-11-18 (via search summary)
36. HeySuccess, Free Electrons 2026 Program — https://www.heysuccess.com/opportunity/Free-Electrons-2026-Program-44139 ; EDP, Free Electrons 10 years — https://edp.com/en/media/news/free-electrons-marks-10-years-and-more-eur124-million-generated-business-outcomes — checked 2026-11-18 (via search summary)
37. Ekonomi Gazetesi, Enerjisa NAR/İVME applications — https://www.ekonomigazetesi.com/sirket-haberleri/enerjisa-enerjinin-programlarina-basvurular-basladi-57612 ; CNBC-e, "423 başvurudan 3 kazanan" — https://www.cnbce.com/enerji/enerjinin-gelecegi-icin-yaristilar-423-basvurudan-3-kazanan-cikti-h41378 — checked 2026-11-18 (via search summary)
