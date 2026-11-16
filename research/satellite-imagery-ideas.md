# Satellite imagery (Earth observation) business ideas
_Last checked: 2026-11-16_

Builds on `public-compute-startup-ideas.md` (ideas 10–18; wildfire was #5 of the top 5) and `public-compute-for-startups.md` (EuroHPC free compute: AI projects only, 1–12 months, no production use; a Montenegrin d.o.o. is eligible, the US LLC is not). Facts marked **(unverified)** could not be confirmed from a primary or reliable source. "Via search summary" in Sources means I read a search-engine summary, not the page itself.

## Summary

- **What the opportunity is.** Europe gives away very good satellite data for free (Copernicus Sentinel, Landsat, ready-made EU maps of fires, land cover and ground movement). The money is in turning that data into **a specific answer someone must have**: "is this forest plot deforestation-free?", "is this road embankment sinking?", "how much of this field burned?". Data is cheap. A trustworthy answer delivered in a customer's workflow is the product.
- **Best idea for a quick test: EUDR evidence packs** for Western Balkan wood, furniture and pellet exporters. The EU Deforestation Regulation applies from **30 December 2026** for large and medium companies and for all timber-sector firms; the Commission's 4 May 2026 package confirmed no further delay [1][2][3]. EU buyers cannot place wood on the EU market without plot geolocation, even from low-risk countries [3][4]. Serbia has ~8,000 wood-sector firms, and 89% say they do not know the relevant EU rules [5]. Bosnia's wood exports were ~€854m in 2025 [6]. Low compute, modest technical skill, a hard deadline: the best fit for a non-technical founder.
- **Best long-term idea: ground-motion (InSAR) monitoring** of roads, railways, dams and slopes. The free European Ground Motion Service (EGMS) **does not cover Serbia, Montenegro, Bosnia, North Macedonia, Albania or Kosovo** [7], and Serbia has 39,000+ registered landslides [8]. The gap is real, but the work needs a radar specialist and buyers are slow state bodies. Several large projects use Chinese contractors (e.g. POWERCHINA-led consortium on Bar–Boljare section 2 [9]), which this founder's policy rules out as customers.
- **Third: wildfire / vegetation risk** (existing idea). It drops from "Shortlist" to **Maybe**. No Balkan buyer found, EFFIS is free, and well-funded firms (Overstory $43m Series B, Nov 2025; LiveEO €28m, May 2026) sell to utilities [10][11].
- **Serbian crop insurance is taken.** BioSense built DDOR TERRA (claims app with satellite checks) with DDOR and Generali [12]; Dunav sells soil-moisture insurance with Swiss Re and VanderSat [13]. **Drop** for this founder.
- **Funding is thinner than it looks.** CASSINI Challenges (€100,000 × 12 winners) are **closed to Montenegrin/Serbian firms for Copernicus-led solutions**: EO-led entries are limited to EU, Iceland, Norway and UK entities [14]. Neither Serbia nor Montenegro has an ESA cooperation agreement that I could find [15][16]. Horizon Europe is open (both are associated), but needs a consortium.
- **Fit for this founder:** EO is a technical field and a poor fit without a co-founder. The exception is EUDR, where the hard part is chasing suppliers for plot data and packaging it, not science. Free tools (FAO's open-source Whisp, QGIS) do the satellite check [17].
- **Recommendation:** run a 6-week, ~$0–150 EUDR customer test now, because the deadline creates urgency until early 2027. Do not build InSAR or wildfire products without a technical co-founder and a named buyer. Free EuroHPC compute is mostly irrelevant here: EO work is data-heavy CPU processing, not AI training.

## How it works (plain language)

**Free data (all usable commercially with attribution).**
- **Sentinel-2 (optical camera).** 10 m pixels (a pixel is a 10×10 m square), a new picture every ~5 days, but clouds block it. Good for vegetation, crops, burn scars and forest loss.
- **Sentinel-1 (radar).** Roughly 5×20 m, every 6–12 days, and it sees through cloud and at night. Radar "InSAR" compares passes to measure ground movement of millimetres per year.
- **Landsat (US).** 30 m, archive back to the 1980s, public domain. Useful for long histories.
- **Licence.** Sentinel data are free, full and open, including commercial use, with attribution [18]. Copernicus Land products are also free, but you must say if you modified them [19].
- **Ready-made EU services:**
  - **EFFIS:** fire danger, active fires and burned areas for Europe including the Balkans.
  - **EGMS:** ground motion. EU/EEA countries only (not the Western Balkans), annual updates, 2020–2024 period, next release Q4 2026 [7].
  - **Copernicus Land Monitoring:** 10 m land-cover "backbone", forest, cropland and grassland layers, and vegetation phenology [19][20].
  - **CAMS:** air quality and atmosphere.

**Commercial imagery.** Use it when you need to see individual trees, poles or buildings.
- Resellers list 30 cm Pléiades Neo archive images at about **$22.50/km²** (5 km² minimum) and 50 cm Pléiades at about **$10/km²** [21].
- Other resellers impose 25–100 km² minimums [21].
- Planet sells area-based annual monitoring subscriptions; the small tiers were shown at ~$2,700–5,100/year, marked "coming soon" **(unverified)** [22].
- Maxar prices were not checked.

**What needs heavy compute, and what doesn't.**
- **Light (laptop or free platform):** checking a few thousand plots against forest maps, burn-scar maps for one region, crop indices for a portfolio.
- **Medium to heavy (CPU clusters, lots of storage):**
  - **InSAR time series** over a country (hundreds of radar scenes, terabytes).
  - **Multi-year continental archives**.
  - **Training AI models** (e.g. tree-species or landslide detectors): this last one is the only part that uses GPUs.
- **Where EuroHPC Fast Lane fits.** The AI Factory calls need an **AI project** (see `public-compute-for-startups.md`). Training a deforestation, fire-fuel or landslide-detection model qualifies. Plain InSAR processing probably does not, and would belong in Benchmark/Development or Regular access instead **(unverified: ask NCC Montenegro)**.

**Platforms that remove the need for your own compute.**
- **Copernicus Data Space Ecosystem (CDSE).** Free data access plus 10,000 free openEO processing credits per user per month (confirmed March 2026) [23]. Whether free credits may be used commercially depends on the CDSE terms (chapter 3) **(unverified)**; paid commercial capacity is offered by partner clouds [23].
- **Google Earth Engine.** Free only for non-commercial and research use. Commercial plans [24]:
  - "Limited": usage fees only.
  - **Basic: $500/month**, with 100 batch and 33 online EECU-hours included.
  - **Professional: $2,000/month**.
  - Premium: on request.

  Basic alone would eat the whole 6-month budget, so use CDSE or Earth Engine only for non-commercial prototyping.
- **Sentinel Hub (now inside Planet Insights Platform).** A 30-day trial. Standalone plans were reported at €25–833/month **(unverified)** [22].
- **Microsoft Planetary Computer.** The public data catalogue still runs. Microsoft now pushes **Planetary Computer Pro**, a paid Azure service for private geospatial data. Microsoft's own page still called it "preview" when checked; one reseller says it is generally available **(unverified)** [25].

## Ideas assessed

Compute: H/M/L. Skill: what a technical partner must know. Verdict for **this** founder.

| # | Idea | Who pays | Driver | Competitors (verified) | Regional buyers named | Compute | Technical skill | Risk | Verdict |
|---|---|---|---|---|---|---|---|---|---|
| 1 | **EUDR geolocation and deforestation-free evidence packs** for wood/furniture/pellet exporters | Balkan exporters and their EU importers | **Regulation**: EUDR 30 Dec 2026 [1][2] | LiveEO ($10m round for EUDR, 2023), Epoch ($6.26m total), Source Intelligence, OpenAtlas [26]; certifiers (SGS Serbia [27], FSC Adria-Balkan) | Serbian wood sector (~8,000 firms [5]); BiH Furniture & Wood cluster (~80 members [6]); Šume Republike Srpske (geolocation pilot with FSC [28]) | L | GIS basics (QGIS, GeoJSON); free tools [17] | Low–medium: liability if a pack is wrong; GDPR for private owners' parcels | **Do-test** |
| 2 | **Ground-motion (InSAR) monitoring** of roads, rail, dams, slopes, tailings | Road/rail/dam owners, engineering consultants, supervisors, insurers | Infrastructure build-out; landslides; EGMS gap [7][8] | TRE Altamira (CLS group), 3vGeomatics (Terra Insights), SkyGeo, Sensar (majority bought by Itility, Jul 2025), Detektia (small Madrid spin-off) [29][30] | Putevi Srbije (has a landslide database with Univ. Belgrade [8]); Monteput and supervisor IRD Engineering on Bar–Boljare [9]; EPCG/EPS dams **(no demand verified)** | M–H (CPU, storage) | **Specialist** InSAR engineer | Medium: Chinese contractors on major projects [9]; liability for missed failure | **Maybe** (only with InSAR co-founder) |
| 3 | Wildfire / vegetation risk near power lines, resorts, insurers (existing #10) | Distribution operators, insurers, resorts | 2025 fire season; Montenegro asked for EU help on 11 Aug 2025 [31] | Overstory ($43m, Nov 2025), LiveEO (€28m, May 2026), AiDash [10][11]; EFFIS free | None verified | M–H | EO scientist | Low | **Maybe** (downgraded) |
| 4 | Crop condition / index insurance, Serbia (existing #11) | Insurers | Drought losses | BioSense + DDOR + Generali (DDOR TERRA) [12]; Dunav + Swiss Re + VanderSat [13]; free AgroSense [12] | DDOR, Generali, Dunav (all served) | M | Agro-EO scientist | Low | **Drop** |
| 5 | CAP-style area monitoring for paying agencies (Serbia, Montenegro, N. Macedonia) | Ministries / paying agencies, often via IPA projects | EU accession (IACS/LPIS) | BioSense (provincial grant checks in Vojvodina [32]); large EU consortia **(unverified)** | Serbian Directorate for Agrarian Payments (IACS body [33]) | M | Senior EO + public tenders | Procurement, politics | **Drop** |
| 6 | Climate physical-risk data for Balkan banks | Bank subsidiaries of EU groups | ECB/EBA expectations, passed down by parents | Global vendors (Moody's, S&P etc. **(unverified)**); Climate X ($18m) | NBS only monitors banks' climate-risk work "taking local specifics into account" [34] | H | Climate scientist | Low | **Drop** |
| 7 | Water: reservoirs, drought, hydro inflow, algal blooms (Skadar, Ohrid, coast) | Utilities (EPCG, EPS), water agencies, donors | Drought, Water Framework Directive alignment | Copernicus/Sentinel-3 free products [35] | Vode Vojvodine uses satellite + drones [36]; Skadar buyer not found | M | Hydrology + EO | Low | **Maybe-low** (grant-funded, not commercial) |
| 8 | Solar/wind siting, rooftop solar maps (existing #17) | Developers, municipalities | Renewables auctions | Solargis/Global Solar Atlas and EU PVGIS free; rooftop needs aerial/LiDAR, not satellites | — | M | Energy modeller | Low | **Drop** |
| 9 | Methane / emissions monitoring | Operators, regulators | EU methane rules | GHGSat, Kayrros **(unverified)**; Sentinel-5P too coarse for small sites | Few emitters; buyers abroad | M–H | Atmospheric scientist | Medium | **Drop** |
| 10 | Mining, quarry and tailings monitoring | Mining firms, regulators, NGOs | Safety, permitting | Same as #2 | Largest Serbian mine is Chinese-owned; lithium project politically contested **(unverified details)** | M–H | InSAR + optical | **High**: China links, political | **Drop** (fold safe parts into #2) |
| 11 | Illegal dumping / landfills / illegal construction | Municipalities, inspectors | Enforcement | — | — | M | Optical ML | **Surveillance-adjacent, political** | **Drop** |
| 12 | Coastal erosion / tourism (existing #12) | Municipalities | — | — | None found | M | EO + coastal | Low | **Drop (confirmed)** |
| 13 | Forest carbon MRV (existing #14) | Carbon developers | Voluntary market | Many global firms | None found | H | Forestry EO | Greenwashing | **Drop (confirmed)** |
| 14 | Post-event damage evidence (fire, flood, hail) for loss adjusters | Insurers, adjusters | Claims cost | DDOR TERRA [12] | Montenegrin insurers **(unverified)** | L–M | EO analyst | Low | **Maybe** (add-on to #1 or #3) |

### 1. EUDR evidence packs (Do-test)
- **What the law requires.**
  - EUDR covers wood, cattle, cocoa, coffee, oil palm, rubber and soy, and products made from them, such as furniture and pellets.
  - The May 2026 draft would **remove leather** from scope (consultation closed 1 June 2026; adoption date not found) [3][4].
  - Dates: **30 Dec 2026** for medium/large companies and **all micro/small timber-sector firms**; 30 June 2027 for other micro/small firms [1][2].
  - Serbia, Bosnia and Herzegovina and Montenegro are classed **low risk** under Implementing Regulation (EU) 2025/1093 [4][37]. Low risk removes the risk-assessment step but **not** the duty to collect plot geolocation [2][4]. "Geolocation must be submitted; otherwise the product cannot be placed on the EU market" [4].
  - Rules for plots: a point for plots up to 4 ha, a polygon for larger ones, and geolocation of all wood components in composite products [38].
- **Who pays.** Non-EU exporters are not directly bound, but their EU buyers cannot comply without their data [38].
  - The pain sits with mid-sized sawmills and furniture makers that mix wood from many lots, including private forests.
  - State forest companies may solve their own part: Šume Republike Srpske piloted stump-level GPS + QR tagging with FSC back in 2023 [28].
  - NALED asked whether Serbia should build its own origin-verification mechanism [5]. If the state does that, demand shrinks.
- **The service.**
  - Collect plot data from suppliers.
  - Clean it into EU-format GeoJSON.
  - Screen each plot against 2020 forest-cover and loss data with FAO's open-source **Whisp** [17].
  - Hand over a short PDF evidence file per shipment or per supplier.
  - The founder's languages and the ability to chase small suppliers are the moat; the satellite part is commodity.
- **Competition.** EU SaaS firms (LiveEO's free TradeAware Lite, Epoch for SMEs) target importers [26]. SGS Serbia sells EUDR services [27]. Workshops are run by FBiH chambers with Swiss SIPPO [6] and by NALED with Swedish funding [5]. There is room for a local hands-on service, but price pressure will be high.
- **Risk.** If a pack is wrong, the EU importer bears the legal liability, but you bear the reputation damage and possibly contract claims (see lawyer questions). Treat private forest owners' names and parcels as personal data.

### 2. Ground motion / InSAR (Maybe)
- **Why there is a gap.** EGMS gives EU countries free, annual ground-motion maps but stops at the EU/EEA border [7]. Serbia has 39,000+ registered landslides, about 25% of its territory is exposed, and the 2014 floods activated 2,000+ slides on state roads [8].
- **The value story.** Big projects (Bar–Boljare section 2: €694m, financed by EBRD €200m + EU €150m grant [9]) and Serbia's road programme are ideal "before and during construction" monitoring cases.
- **Who buys.**
  - **Supervision engineers and EU/EBRD-funded owners**, not contractors. On Bar–Boljare the contractor is a POWERCHINA-led consortium, which this founder must not sell to [9].
  - Monteput/IRD Engineering would need checking for indirect links.
- **Competition.** Established specialists (TRE Altamira, 3vGeomatics, SkyGeo) sell worldwide [30]. Detektia shows how small a niche player can stay: tiny funding, estimated ~$0.4m revenue **(third-party estimate)** [29].
- **Verdict.** Credible only with an InSAR engineer co-founder from a Belgrade or Podgorica faculty. A university research group could also sell this directly.

### 3. Wildfire / vegetation (Maybe, downgraded)
- Demand is real elsewhere: Overstory raised $43m (Series B, Nov 2025), and LiveEO raised €28m (May 2026) for infrastructure and vegetation work [10][11]. Montenegro triggered the EU Civil Protection Mechanism on 11 Aug 2025 [31].
- But no Balkan utility or insurer was found buying this, and free EFFIS covers basic needs.
- Keep it as a **demo asset**: a free burned-area map of the 2025 Montenegrin fires helps credibility with insurers (idea 14), not as a business on its own.

### 4. Serbian crop/index insurance (Drop)
- BioSense is a Copernicus regional hub. It built DDOR TERRA with **DDOR and Generali Osiguranje Srbija** (2022): a farmer app plus a web tool for assessors that uses satellite footage [12]. Its AgroSense platform is free for farmers [12].
- Dunav offers soil-moisture deficit insurance with **Swiss Re and VanderSat** [13]. VanderSat has since been bought by Planet (2021; not re-checked).
- The three biggest buyers are served. Best use: BioSense as a **partner or co-founder source**, not a rival.

### 5–13 in brief
- **CAP monitoring:** state procurement tied to IPA funding, with BioSense already working with the ministry and Vojvodina [32][33]. Not for a solo founder.
- **Bank climate risk:** NBS takes a light-touch approach [34]. EU parent groups buy centrally from global vendors. Drop.
- **Water:** scientifically attractive (Sentinel-3 daily 300 m data for big lakes [35]), but buyers are public and donor-funded. Pursue only through a grant consortium.
- **Solar, methane, mining, dumping:** dropped for free incumbents, coarse data, China/political links, or surveillance concerns respectively.
- **Coastal erosion and forest carbon:** the "Drop" verdicts stand. No buyer was found, and EUDR is not a carbon market.

## Funding and support for an EO startup

| Source | Open to a Montenegrin/Serbian firm? | Amount / dates | Note |
|---|---|---|---|
| **CASSINI Challenges** (EUSPA) | **Not for EO-led solutions.** Copernicus-led entries: EU + Iceland/Norway/UK only. Horizon-associated countries (ME, RS) only for solutions *without* Copernicus/Galileo prevalence [14] | €100,000 × 12 winners; 2026 deadline 26 Mar 2026 (closed); needs TRL ≥ 5, CRL ≥ 4 [14] | The rule could change in 2027 **(unverified)** |
| CASSINI Hackathons | Local organisers must be EU entities; participant rules **(unverified)** | 12th edition expected Q4 2026, dates not fixed when checked [39] | Good place to meet technical co-founders (online or in Zagreb/Ljubljana if held) |
| Copernicus Masters | No 2026 edition found **(unverified)** | €531,000 prize pool in 2022 [40] | — |
| ESA BIC incubation | Serbia: no ESA membership or cooperation agreement (2026 paper) [15]. Montenegro: only a first ESA visit in 2018; no agreement found [16] | Usually requires incorporation/residence in the host ESA state **(unverified per centre)** | Only via a company in an ESA state, e.g. Slovenia (associate member, applying for full membership) [41] |
| Horizon Europe space | Yes (both associated) | EUSPA downstream call closed 24 Feb 2026; CL4-2027-SPACE-03-34 (EO + AI) opens 9 Mar 2027, €26m total [42] | Consortium research projects. Join as a small partner, do not lead |
| EuroHPC AI Factories | Yes, through a Montenegrin d.o.o. | Free GPU-hours, 1–3 months (Fast Lane) | Only for **AI** model training (e.g. a forest/landslide model), not routine processing |
| Montenegro Innovation Fund | Yes | Early-stage start-up grant up to €30,000 (2024) [see `public-compute-for-startups.md`]; the 2023 call totalled €350,000 [43] | Best cash source for a co-founder's first months |
| Donor-funded EUDR support (Sweden via NALED; Switzerland via SIPPO) [5][6] | Partners, not funders | — | Channel to exporters: offer to present at their workshops |
| Platforms | — | CDSE free credits [23]; Earth Engine free for non-commercial use only [24] | Prototype for free; pay only once a client pays |

## Recommended next step

**6-week EUDR demand test (cost: ~$0–150; no engineer; no company formation).**

- **Week 1: learn and prepare.**
  - Read the EU EUDR guidance/FAQ and the FAO Whisp overview.
  - Install QGIS (free).
  - Draw a polygon for one public forest area and run it through Whisp (web or API access route) [17].
  - Produce a 2-page sample "evidence pack": map, coordinates, 2020 forest status, data sources, disclaimer.
- **Week 2: build a target list.** List 40 exporters from:
  - the PKS wood/furniture section;
  - the BiH Furniture & Wood cluster;
  - FTC BiH workshop participants;
  - Montenegrin sawmills.

  Check each against the compliance policy: no Russian or Chinese ownership, no sanctioned links.
- **Weeks 3–5: run 15 interviews (calls in BCMS).** Ask:
  - Have your EU buyers asked for geolocation?
  - Who will supply plot data: the state forest company, private owners or you?
  - What will you do on 30 December?
  - Would you pay for a done-for-you pack, and how much per shipment/supplier?

  Offer 3 free pilot packs in exchange for a reference. Also speak to one EU importer of Balkan furniture and to NALED/SIPPO.
- **Week 6: decide.**
  - **Continue** if at least 5 of 15 confirm buyer pressure and missing data, and at least 2 agree a paid pilot.
  - **Stop** if state forest companies already supply ready-made geolocation, or nobody will pay.

**If it works:** form the d.o.o., apply to the Montenegro Innovation Fund, and recruit a part-time GIS analyst. Later, apply for EuroHPC Fast Lane to train a Balkan forest/tree-species model as a product upgrade.

**Co-founder profile (for any EO path beyond EUDR):**
- Remote-sensing engineer with Python, Sentinel-1/2 processing, openEO/Earth Engine and QGIS.
- For InSAR: hands-on SNAP/ISCE/StaMPS-type persistent-scatterer experience and geotechnical validation.
- Where to look:
  - University of Belgrade Faculties of Civil Engineering (geodesy) and Mining & Geology (built the landslide database with Putevi Srbije [8]);
  - BioSense/University of Novi Sad [12];
  - University of Montenegro and UDG (which back NCC Montenegro);
  - small GIS firms such as Geosemantica (Tivat) and GILab (Belgrade);
  - Montenegro Space Research (Balkan GeoScan CubeSat team) [44];
  - QGIS user groups and CASSINI Hackathon participants.

## Questions for a lawyer / accountant

1. If we prepare EUDR geolocation/evidence packs and one is wrong, what is our liability to the exporter and the EU importer? What disclaimer, contract cap and professional-indemnity insurance do we need?
2. Does collecting private forest owners' parcel coordinates and names trigger GDPR (for EU importers) and the Serbian/Montenegrin/Bosnian data-protection laws? What consent and contract terms are needed?
3. Does selling maps or coordinates require a geodetic licence in Serbia (RGZ), Montenegro (Real Estate Administration) or BiH?
4. Can a Montenegrin d.o.o. act for exporters with EU authorities (TRACES information system), or must an EU-established authorised representative do that [4]?
5. Copernicus, CLMS and Whisp outputs: attribution and liability terms when resold inside a paid service. CDSE free-credit terms for commercial use. Earth Engine: when does "non-commercial" end?
6. For InSAR work on EU/EBRD-funded projects: how do we screen owners, supervisors and contractors for Chinese/Russian links under our policy, and what if a project mixes a POWERCHINA-led contractor with an EU-funded owner?
7. Accountant: how should grant income (Innovation Fund) and EUDR service revenue be booked in the d.o.o. alongside the US LLC's brokerage? What are the VAT rules on services to EU importers?

## Sources

1. EY Tax News, "EU Deforestation Regulation application postponed to 30 December 2026" — https://taxnews.ey.com/news/2026-0237-eu-deforestation-regulation-application-postponed-to-30-december-2026 ; Council press release 18 Dec 2025 — https://www.consilium.europa.eu/en/press/press-releases/2025/12/18/deforestation-council-signs-off-targeted-revision-to-simplify-and-postpone-the-regulation/ — checked 2026-11-16 (via search summary)
2. HLC, "EUDR: Commission publishes simplification package ahead of December 2026 application date" — https://www.hlc.com/en/publications/eu-deforestation-regulation-commission-publishes-simplification-package-ahead-of-december-2026 — checked 2026-11-16
3. Wikipedia, EU Regulation on Deforestation-free products (leather removal proposal) — https://en.wikipedia.org/wiki/EU_Regulation_on_Deforestation-free_products — checked 2026-11-16 (via search summary)
4. EUSTAFOR, "What the Commission's 4 May 2026 simplification package means for wood, state forests and non-EU operators" — https://eustafor.eu/eudr-what-the-commissions-4-may-2026-simplification-package-means-for-wood-state-forests-and-non-eu-operators/ — checked 2026-11-16
5. NALED, "New EU sustainability rules pose a challenge for 8,000 companies in the wood industry" (18 Jun 2026) — https://naled.rs/en/vest-nova-eu-pravila-o-odrzivosti-izazov-za-8000-preduzeca-u-drvnoj-industriji-12254 — checked 2026-11-16
6. N1 BiH on wood exports 2025 — https://n1info.ba/english/news/bosnian-furniture-manufacturers-return-to-imm-cologne-to-recapture-market-share ; FENA, FTC BiH on EUDR (23 Jun 2026) — https://fena.ba/article/1684956/eudr-alignment-key-to-preserving-competitiveness-of-bosnia-and-herzegovina-exporters ; KFBiH EUDR workshops — https://www.kfbih.com/en/?p=29624 ; Energetski portal on Furniture & Wood cluster — https://www.energetskiportal.com/?p=208526 — checked 2026-11-16 (via search summary)
7. Copernicus Land, EGMS FAQ (country coverage, 2020–2024, next release Q4 2026) — https://land.copernicus.eu/en/faq/products/european-ground-motion-service — checked 2026-11-16
8. 021.rs, "U Srbiji bar 39.000 klizišta" — https://www.021.rs/info/srbija/440012/u-srbiji-bar-39000-klizista-uskoro-gradjanima-dostupna-mapa-sa-svim-lokacijama ; Vreme on roads and landslide exposure — https://www.vreme.com/en/vesti/kako-da-srbija-zastiti-puteve-od-klimatskih-promena/ ; Univ. Belgrade landslide database paper — https://dr.rgf.bg.ac.rs/files/original/1ca1262d52f3be7549e76b217721fe0497be550d.pdf — checked 2026-11-16 (via search summary)
9. Montenegro Business, €693.97m Mateševo–Andrijevica contract — https://montenegrobusiness.eu/montenegro-to-sign-e693-97-million-contract-for-matesevo-andrijevica-section-of-bar-boljare-motorway/ ; ICE (Italy) naming POWERCHINA/STECOL/PCCD — https://www.ice.it/it/news/notizie-dal-mondo/298263 ; Gov.me, Monteput and IRD Engineering supervision contract — https://www.gov.me/en/article/monteput-and-ird-engineering-sign-contract-for-supervision-of-works-on-the-second-section-of-the-highway ; MINA, EU grant agreement — https://mina.news/article/grant-agreement-signed-for-the-matesevo–andrijevica-motorway-section — checked 2026-11-16 (via search summary)
10. ImpactAlpha, "Overstory secures $43 million" — https://impactalpha.com/overstory-secures-43-million-to-predict-and-prevent-utility-sparked-fires/ — checked 2026-11-16 (via search summary)
11. Greencode VC, "LiveEO raises €28M" — https://greencode.vc/insights/liveeo-raises-28m-to-scale-geospatial-intelligence-across-civil-infrastructure-and-defense — checked 2026-11-16 (via search summary)
12. BioSense, "New technologies are restoring the trust between producers and insurance companies" — https://biosens.rs/en/themes/nove-tehnologije-uspostavljaju-poverenje-izmedju-proizvodjaca-i-osiguravajucih-kuca ; BioSense 2022 results (DDOR, Generali) — https://www.uns.ac.rs/images/doc/nauka/vrhunskiRezultati2022/BIOSENSE_2022_VrhRez_4_eng.pdf ; AgroSense — https://biosens.rs/en/themes/agrosense — checked 2026-11-16 (via search summary)
13. Dunav osiguranje, soil-moisture deficit insurance — https://www.dunav.com/en/insurance/agriculture/soil-moisture-deficit-insurance/ ; Dunav partnership note — https://www.dunav.com/en/?p=60157 — checked 2026-11-16 (via search summary)
14. EUSPA, CASSINI Challenges 2026 Rules of Contest EUSPA/PRIZE/01/2026 (section 2.4, prize €100,000, deadline 26 Mar 2026) — https://www.euspa.europa.eu/sites/default/files/documents/EUSPA-PRIZE-01-2026%20-%20Cassini%20Challenges%202026%20-%20Rules%20of%20Contest.pdf — checked 2026-11-16 (PDF text read directly)
15. Stojković & Ilić, Serbia and ESA pathways (2026 conference paper) — https://www.aob.rs/images/doi/konferencije/2026/PDF/2026-1csst/09.pdf — checked 2026-11-16 (via search summary)
16. Government of Montenegro, first official ESA delegation visit (2018) — https://www.gov.me/en/article/183654--the-first-official-visit-of-the-delegation-of-the-european-space-agency-to-montenegro-a-wide-range-of-cooperation-benefits ; Wikipedia, Enlargement of ESA — https://en.wikipedia.org/wiki/Enlargement_of_the_European_Space_Agency — checked 2026-11-16 (via search summary)
17. WRI, "Supporting EUDR compliance with Whisp" — https://www.wri.org/update/supporting-eudr-compliance-whisp ; FAO Whisp overview — https://www.fao.org/fileadmin/user_upload/faoweb/NFM/WhispOverview.pdf — checked 2026-11-16 (via search summary)
18. Copernicus Sentinel data licence — https://ewds.climate.copernicus.eu/licences/ec-sentinel — checked 2026-11-16 (as cited in `public-compute-startup-ideas.md`)
19. EEA catalogue, CLMS access conditions — https://sdi.eea.europa.eu/catalogue/srv/api/records/8171c91b-f147-41ed-b69e-52e3e68e1bfa ; CDSE, CLMS datasets moving to CDSE — https://dataspace.copernicus.eu/node/3136 — checked 2026-11-16 (via search summary)
20. GAF, HRL update 2022–2023 — https://www.gaf.de/major-update-of-the-copernicus-land-monitoring-high-resolution-layers-for-the-years-2022-2023/ ; GeoVille, CLC+ Backbone 2025 — https://www.geoville.com/news/newsdetail/clcplus-backbone-2025-high-resolution-land-cover-for-europe/ — checked 2026-11-16 (via search summary)
21. SkyWatch, satellite imagery pricing — https://skywatch.com/satellite-imagery-pricing/ ; LandInfo price sheet Jan 2026 — https://landinfo.com/wp-content/uploads/Imagery_LandInfo_202601-1.pdf ; Airbus archive and tasking — https://space-solutions.airbus.com/archive-and-tasking-options/ — checked 2026-11-16 (via search summary)
22. Planet pricing — https://planet.com/pricing ; Planet Insights Platform pricing overview — https://support.planet.com/hc/en-us/articles/38144064507293-Overview-of-Pricing-and-Packaging-in-Planet-Insights-Platform — checked 2026-11-16 (via search summary)
23. CDSE, openEO credit usage — https://documentation.dataspace.copernicus.eu/APIs/openEO/credit_usage.html ; CDSE notice on openEO credit billing (Mar 2026) — https://dataspace.copernicus.eu/node/3068 — checked 2026-11-16 (via search summary)
24. Google Cloud, Earth Engine pricing — https://cloud.google.com/earth-engine/pricing — checked 2026-11-16 (page text read directly)
25. Microsoft Learn, Planetary Computer Pro "What's new" — https://learn.microsoft.com/en-us/azure/planetary-computer/whats-new ; SkyWatch–Microsoft integration (Jun 2026) — https://skywatch.com/?p=997693 — checked 2026-11-16 (via search summary)
26. LiveEO $10m funding (Nov 2023) — https://www.live-eo.com/company/press/successful-funding-of-10m-enabling-our-head-start-in-deforestation-compliance-market ; ESG Today, Epoch raises $4.25m — https://www.esgtoday.com/?p=26499 ; Barchart, Source Intelligence EUDR — https://www.barchart.com/story/news/33534252/eudr-solution-from-source-intelligence-simplifies-deforestation-due-diligence ; ESA BIC Noordwijk, OpenAtlas — https://www.sbicnoordwijk.nl/openatlas-enables-geospatial-analysis-for-deforestation-free-supply-chains-esabic/ — checked 2026-11-16 (via search summary)
27. SGS Serbia, EUDR services — https://www.sgs.com/en-rs/service-groups/eu-deforestation-regulation-eudr — checked 2026-11-16 (via search summary)
28. FSC, "The Republic of Srpska pioneers timber geolocation" (6 Dec 2023) — https://fsc.org/en/newscentre/general-news/the-republic-of-srpska-pioneers-timber-geolocation — checked 2026-11-16
29. Detektia: ESA commercialisation profile — https://commercialisation.esa.int/?p=2861 ; PitchBook — https://pitchbook.com/profiles/company/442218-88 ; Prospeo revenue estimate — https://prospeo.io/c/detektia-revenue — checked 2026-11-16 (via search summary)
30. EOMAG, TRE and Altamira together in CLS — https://eomag.eu/tre-and-altamira-together-in-cls-become-the-largest-insar-group-worldwide/ ; PrivSource, RST/Measurand acquires 3vGeomatics (2021) — https://www.privsource.com/acquisitions/deal/ArSR9v ; World M&A, Itility majority stake in Sensar (Jul 2025) — https://world-ma.com/transactions/detail/news/itility-group-acquires-majority-stake-in-sensar — checked 2026-11-16 (via search summary)
31. European Commission, wildfires and the Civil Protection Mechanism — https://civil-protection-humanitarian-aid.ec.europa.eu/what/civil-protection/wildfires_en ; ERCC map 12 Aug 2025 — https://www.gdacs.org/contentdata/maps/daily/WF/1024555/ECDM_20250812_WF_Montenegro.pdf — checked 2026-11-16 (via search summary)
32. BioSense, AgroSense APV (Vojvodina grant monitoring) — https://biosens.rs/en/projects/agrosens-apv ; BioSense government services — https://biosens.rs/en/themes/government — checked 2026-11-16 (via search summary)
33. europa.rs, IACS in Serbia (undated) — https://europa.rs/images/publikacije/IACS.pdf — checked 2026-11-16 (via search summary)
34. National Bank of Serbia, financial stability recommendations / climate-risk monitoring — https://www.nbs.rs/en/ciljevi-i-funkcije/finansijska-stabilnost/finansijska-stabilnost/preporuke/ ; BIS, Tabaković speech (10 Sep 2025) — https://www.bis.org/review/r250910c.htm — checked 2026-11-16 (via search summary)
35. MDPI Remote Sensing 16(19):3734 (Sentinel-3 OLCI for lakes) — https://mdpi.com/2072-4292/16/19/3734 — checked 2026-11-16 (via search summary)
36. Eurisy, PWMC Vode Vojvodine satellite and UAV use — https://www.eurisy.eu/stories/pwmc-vode-vojvodine-merging-satellite-data-and-uavs-for-improved-water-management-and-flood-risk-analysis_245/ — checked 2026-11-16 (via search summary)
37. Ropes & Gray, Commission sets EUDR country risk classifications — https://www.ropesgray.com/en/insights/viewpoints/102kcln/european-commission-sets-country-risk-classifications-for-eu-deforestation-regula — checked 2026-11-16 (via search summary; direct fetch blocked; status after the July 2025 Parliament objection not fully confirmed)
38. Polygon One, EUDR for furniture importers — https://polygon-one.com/en/eudr-furniture-importers ; Tracextech, EUDR for exporters — https://tracextech.com/eudr-for-exporters/ — checked 2026-11-16 (via search summary; vendor sources)
39. CASSINI Hackathons application guide 2026 — https://www.cassini.eu/hackathons/sites/default/files/2025-12/Application%20Guide%20April%20and%20November%202026_update%202025-12-02.pdf — checked 2026-11-16 (via search summary)
40. BELSPO, Copernicus Masters 2022 — https://eo.belspo.be/agenda/copernicus-masters-2022-promoting-earth-observation-innovation-europe — checked 2026-11-16 (via search summary)
41. Payload, "Slovenia applies for full ESA membership" — https://payloadspace.com/slovenia-applies-for-full-esa-membership/ — checked 2026-11-16 (via search summary)
42. EUSPA Horizon Europe page — https://www.euspa.europa.eu/opportunities/horizon-europe ; EU AI Continent, HORIZON-CL4-2027-SPACE-03-34 — https://www.euacc.ai/calls/HORIZON-CL4-2027-SPACE-03-34 — checked 2026-11-16 (via search summary)
43. Biznis.rs, Montenegro Innovation Fund early-stage start-up call €350,000 — https://biznis.rs/vesti/region/za-podrsku-ranoj-fazi-razvoja-startapa-350-000-evra/ — checked 2026-11-16 (via search summary)
44. Nanosats.eu, Balkan GeoScan (Montenegro Space Research) — https://www.nanosats.eu/sat/balkan-geoscan ; DesignRush, Geosemantica — https://www.designrush.com/agency/profile/geosemantica ; Clutch, GILab — https://clutch.co/profile/gilab-doo-beograd — checked 2026-11-16 (via search summary)
