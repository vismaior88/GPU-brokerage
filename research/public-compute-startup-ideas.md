# Startup ideas that use public compute (without reselling it)
_Last checked: 2026-11-16_

Builds on `government-compute.md` (public compute cannot be resold; the founder's US LLC is not an eligible EuroHPC user) and `opportunities.md` (South-East Europe niche). Programme rules are being researched in parallel; this file works from the **known constraints** in the brief and marks where an idea depends on them.

## Summary

- **Direct answer: yes, a few businesses could legitimately use free public compute for their build phase, but none of the good ones depend on it.** Free compute saves a few thousand euros of GPU time during R&D. It does not find customers, build the product or run the service later. Fast Lane gives 1–3 months and up to 50,000 GPU-hours [1]; Large Scale gives 3, 6 or 12 months [2]. That is a head start, not a way to "keep the business running for years".
- **Top 3 ideas:**
  1. **Western Balkans tender and public-records intelligence** (tenders, court decisions, official gazettes turned into searchable, English-language structured data). It has the clearest paying demand and the best fit with the founder's languages. It needs only medium compute.
  2. **Local-language AI evaluation lab** (BCMS, Albanian, Macedonian): tests which AI models work in these languages, red-teams them and builds evaluation data for banks, telecoms, public bodies and AI vendors. It uses public compute heavily, it is all R&D, and it needs no internet on the compute nodes.
  3. **Cyrillic/Latin document digitisation (OCR and handwriting recognition) for archives, libraries and companies**, with cleaned text datasets as a second product. This is the heaviest real compute need, it is batch-friendly, and buyers spend grant money.
- **The core trap:** in every idea the bottleneck is a product people pay for, plus an engineer to build it, not GPUs. About 25 of the 33 ideas below need a technical co-founder **before** the first sale. All the science ideas (docking, materials, proteins, genomics) and all the Earth-observation ideas fail the "non-technical founder can start it" test.
- **Eligibility trap:** EuroHPC access needs an entity in an EU or participating state. Serbia and Montenegro qualify; the US LLC does not [3]. Serbia's free National AI Platform is for universities and for startups that are members of a Serbian science-technology park [5][6]. Either way the founder must first set up a local company (cost **unverified**; ask an accountant).
- **Rules trap:** free access is for R&D and innovation, for months, not for running a production service. AI Factory pages describe mainly training-type uses [2]. Whether pure **data processing or batch inference** counts as "AI innovation" for the free tracks is **not confirmed**, so check this with the parallel rules research before building a plan on it.
- **Legal hot spots:** copyright and text-and-data-mining (TDM) opt-outs for any dataset sold to AI builders. The CJEU has not yet ruled (case C-250/25), and national courts disagree on what a valid opt-out looks like [29]. GDPR also applies to court decisions, archives and voices. Military, surveillance and dual-use ideas are dropped.
- **Recommendation:** do not start "a public-compute startup". Run a 6-week, near-zero-cost demand test of idea 1 (and, if time allows, idea 2) using paid APIs and manual work. Only if someone pays for a pilot, form a local company, find a technical partner and apply for Fast Lane or the Serbian platform to build the bulk version. With under $2,000 and 20–40 hours a week, the founder cannot run this **and** the brokerage at full intensity. Pick one as primary after the test.

## Long list

Compute: **H** = genuinely needs GPU clusters for weeks; **M** = useful for a one-off backfill but a paid API or a single rented GPU would also do; **L** = a laptop or cheap cloud is enough. "Fits rules?" assumes the known constraints (R&D phase, batch jobs, no internet on nodes, civilian use, no resale).

| # | Idea | Category | Compute | Fits public-compute rules? | Demand evidence | Technical co-founder needed? | Legal/data risk | Verdict |
|---|---|---|---|---|---|---|---|---|
| 1 | Western Balkans tender and public-records intelligence (EN + local languages): tenders, awards, court decisions, gazettes, extracted into structured data and alerts | Public-records data | M | Yes, for the one-off extraction backfill; serve on cheap cloud | Akta built a Serbian legal assistant on ~50,000 court decisions [18]; Prozone's Lex AI runs inside Paragraf Lex [19]; tender trackers sell Serbia/Montenegro feeds [21]; the state's case-law search is free [35] | Data engineer (part-time or freelance is possible) | Low–medium: personal data in court decisions; portal terms; accuracy liability | **Shortlist** |
| 2 | Local-language AI evaluation lab: benchmarks, model comparison and red-teaming in BCMS/Albanian/Macedonian | Evaluation | M–H | Yes: pure R&D batch jobs on open-weight models; data staged in advance | Community Serbian benchmarks exist but are machine-translated or volunteer-made [12][34]; Giskard (AI testing) got EU AI Act grant funding [28] | Yes (NLP/ML engineer) | Low | **Shortlist** |
| 3 | Licensed, rights-cleared BCMS/Albanian/Macedonian text datasets for model builders | Dataset curation | H (dedup, filtering, translation) | Yes for processing; crawl elsewhere | Karya sells low-resource language data to Google and Microsoft [9]; 42 known publisher licensing deals in 2024 [11]; but open corpora exist [13][14], Serbia's state LLM project collects data for free [15] and OpenEuroLLM targets Albanian with open data [33] | Yes | **High**: copyright, TDM opt-outs [29] | Maybe (as a by-product of 2 and 4) |
| 4 | Cyrillic/Latin document digitisation and handwriting recognition for archives, libraries, municipalities and firms | OCR / digitisation | H at scale | Yes: offline batch on staged scans | Transkribus sells credits (1,000 credits €199) [17]; UNDP/National Library of Serbia say commercial OCR fails on mixed-script material [16]; Interreg archive project DIGIARCH (HR–RS) received €267k [36] | Yes (OCR/vision ML) | Medium: GDPR in archives; client data on a public machine | **Shortlist** |
| 5 | EU-accession language toolkit: aligned EU-law corpus EN↔Montenegrin/Serbian/Albanian/Macedonian, terminology, MT quality checks | Translation data | M | Yes | Montenegro has ~190,000 pages of acquis to translate; the EU is considering a derogation because it may fall short [22] | Yes (NLP), but the founder can do terminology QA | Low (EU legal texts are reusable; **unverified** for national translations) | **Shortlist** |
| 6 | Bulk transcription and subtitling of BCMS broadcast and media archives | Speech | H for backlog | Backlog yes; daily service no | Media monitors with large archives: Ninamedia (91 staff), Presscut (TV/radio since 2007) [32]; large open Serbian speech data already exists [14] | Yes | Medium: broadcast copyright; voices are personal data | Maybe |
| 7 | Paid speech-data collection (recordings) for BCMS/Albanian | Speech data | L (the work is human) | Not needed | Karya model [9] | No, but operations-heavy | Medium–high: biometric data consent | Drop (compute is not the bottleneck) |
| 8 | Synthetic instruction and dialogue data in local languages for chatbot builders | Synthetic data | H | Yes | NVIDIA bought synthetic-data firm Gretel above a $320m valuation [10] | Yes | Medium: generator-model licence terms; quality | Maybe |
| 9 | Embeddings/vector index of the BCMS web and news sold as an API | Embeddings | H | Crawl outside, embed inside; serving no | None found | Yes | **High**: copyright and opt-outs [29] | Drop |
| 10 | Wildfire and vegetation risk near power lines for Adriatic/Balkan utilities | Earth observation | H (historical archive) | Yes for model building and backfill | Overstory raised $43m doing this for utilities [23]; Montenegro called in EU firefighting help in Aug 2025 [27] | Yes (EO scientist) | Low | **Shortlist** (#5) |
| 11 | Crop-condition and loss-evidence layers for Serbian agricultural insurers | EO / agriculture | H | Yes | DDOR, Dunav and Generali already use satellite tools; agricultural premiums ~€25m [26] | Yes | Low; strong local competitor (BioSense Institute) [26] | Maybe |
| 12 | Coastal and tourism monitoring (erosion, beach use, sea state) for Montenegrin municipalities | EO | M | Yes | No paying buyer found **(unverified)** | Yes | Low–medium | Drop |
| 13 | Illegal-construction detection for municipalities | EO / aerial | M | Yes | **Unverified** | Yes | Surveillance-adjacent; political | Drop |
| 14 | Forest carbon MRV for Balkan forests | EO | H | Yes | Weak voluntary-carbon demand **(unverified)** | Yes | Greenwashing claims | Drop |
| 15 | Downscaled climate physical-risk scores for Balkan banks and property | Climate | H | Yes | Climate X raised $18m; Cervest and Gro Intelligence collapsed [24] | Yes (climate scientist) | Low | Maybe |
| 16 | Hyperlocal weather/agro-met forecasting | Weather | H, daily | **No**: it is an ongoing production run | **Unverified** | Yes | Low | Drop |
| 17 | Solar/wind siting and yield reports for Balkan developers | Energy | M | Yes | Paid market exists, but Solargis gives annual data free via the Global Solar Atlas [25] | Yes | Low | Maybe |
| 18 | Grid hosting-capacity simulation for distribution operators | Energy | H | Yes | Buyers are state utilities using procurement **(unverified)** | Yes (power engineer) | Low; procurement and lobbying issues | Drop |
| 19 | Molecular docking / virtual screening for biotechs | Science | H | Yes (classic HPC) | CRO market exists **(unverified specifics)** | PhD-level chemist | Medium: toxin/dual-use screening | Drop |
| 20 | Materials screening (batteries, catalysts) | Science | H | Yes | **Unverified** | PhD | Medium–high: export control | Drop |
| 21 | Protein-structure prediction as a service | Science | H | Yes | Free tools and databases undercut it **(unverified)** | PhD | Biosecurity | Drop |
| 22 | CFD/structural simulation consultancy for regional engineering firms | Engineering | H | Yes; FFplus funds such SME experiments [see `government-compute.md`] | **Unverified** locally | Yes (simulation engineer) | Low | Maybe (it is consulting, not a startup) |
| 23 | Genomics pipelines for clinics/biobanks | Genomics | H | Partly | **Unverified** | Yes | **High**: health data | Drop |
| 24 | Film and TV archive restoration, upscaling and tagging | Media | H | Yes (batch) | **Unverified** | Yes | Medium: copyright | Maybe |
| 25 | AI dubbing / voice localisation into BCMS | Media | H | Partly | **Unverified** | Yes | **High**: voice cloning consent | Drop |
| 26 | AI Act-style safety testing of local-language chatbots (banks, telecoms) | Evaluation | M | Yes | An Albanian LLM-safety dataset appeared only in 2026 (the gap is real) [13]; Giskard's AI Act product [28] | Yes | Low | Merge into #2 |
| 27 | Small fine-tuned domain models (legal, banking BCMS). **Note: this is model training**, though light | Fine-tuning | H | Yes | **Unverified**; the state LLM [15] may crowd it out | Yes | Medium | Maybe |
| 28 | Monte Carlo risk simulation for Balkan banks/insurers | Finance | M | **No**: bank data cannot sit on a public machine; ongoing | **Unverified** | Yes (quant) | **High**: regulated, bank secrecy | Drop |
| 29 | Urban digital twin / traffic simulation for cities | Digital twin | H | Yes | Municipal procurement **(unverified)** | Yes | Medium | Drop |
| 30 | Company-ownership and adverse-media data for Western Balkans KYC | Public records | L–M | Partly | KYC providers need local coverage **(unverified)** | Data engineer | Medium–high: personal data; defamation | Maybe (merge with #1) |
| 31 | Montenegro coastal real-estate price analytics | Data | L | Not needed | **Unverified** | Some | Scraping terms | Drop (no heavy compute) |
| 32 | Searchable historical newspaper archive for the diaspora/genealogy | OCR + consumer | H | Yes | LORYA processed 16,000 periodicals for the National Library of Serbia (open-source, donor-funded) [16] | Yes | Medium: copyright on newer issues | Maybe (merge with #4) |
| 33 | GPU/inference benchmarking reports for brokerage buyers | Evaluation | M | **No**: benchmarking for clients' commercial benefit is not R&D; use vendor trial credits | Buyers want it (see `opportunities.md`) | Yes | Low | Maybe (on credits, not public compute) |

**Count:** 6 Shortlist candidates (5 kept below), 12 Maybe, 15 Drop. Most ideas are weak for this founder. They are either science businesses that need a PhD, production services that public compute cannot host, or data products with copyright exposure.

## Top 5 in detail

All five share a pattern:
- **Phase 0 (no compute):** prove demand with a paid API, manual work and samples.
- **Phase 1 (public compute):** the bulk R&D build (backfill extraction, model comparison, large OCR runs) on a Fast Lane allocation or the Serbian platform.
- **Phase 2 (credits or cheap cloud):** serve the product. Google's startup programme offers up to $200k–$350k for funded or AI-first startups [7]; AWS Activate figures are **unverified**.
- **Phase 3:** pay for compute from revenue.

Applying needs a Montenegrin or Serbian entity [3][5]. The result of each allocation should be a dataset, pipeline or evaluation the company **owns**, never compute time someone else uses (resale and sharing access are prohibited [4]).

### 1. Western Balkans tender and public-records intelligence

**What it is.** A subscription data product that collects public tenders, contract awards, court decisions and official-gazette changes from Serbia, Montenegro, Bosnia and Herzegovina and North Macedonia. It extracts the key fields (buyer, value, deadline, winner, CPV code, parties, outcome), translates summaries into English and sends alerts. A second tier sells due-diligence packs: "every public contract and court case involving company X".

**Customers and what they pay for.** Foreign contractors and consultancies bidding on EU-, WBIF-, EBRD- or EIB-funded projects (WBIF publishes its pipeline [21]); local SMEs that bid; law firms; and compliance or due-diligence firms. They pay for time saved and English access, not for AI.

**Use of public compute.**
- Phase 0: scrape and download on an ordinary server; extract a few thousand documents with a paid LLM API.
- Phase 1: one Fast Lane allocation runs an open-weight model over the full historical backlog (millions of pages, staged onto the cluster in advance). It also compares extraction quality across models.
- Phase 2: daily new documents are a small load, handled by a cheap API or one rented GPU.

Be honest: this idea would also work with no public compute at all. That is a strength.

**First 90 days.**
- Weeks 1–3: interview 15 potential buyers (5 foreign bidders, 5 local firms, 5 law/compliance firms) and check each portal's terms and data formats. Transparency Serbia found most Serbian portal data was not machine-reusable (2018 finding, may be outdated) [20].
- Weeks 4–8: deliver a hand-made weekly English tender digest for one sector (for example water and energy) to 10 trial users.
- Weeks 9–12: ask for payment (for example €50–150 per month; **price untested**). Recruit a freelance data engineer only after 3 paying users.

**What a technical partner must do.** Build reliable scrapers and parsers (PDFs, scanned annexes), the extraction pipeline and its quality checks, a database, and a simple alert and search front end. Later, write the Slurm batch jobs for the backfill.

**Evidence of demand.**
- Akta (Novi Sad) built a paid Serbian legal assistant on ~50,000 court decisions [18].
- Prozone's Lex AI has run inside Paragraf Lex since 2026 [19]; Paragraf sells annual subscriptions across the region [19].
- Blackridge sells Serbia and Montenegro tender databases [21].

This shows that buyers pay, and also that the **legal-research segment is already served**. Lead with tenders and cross-border English access, not Serbian legal research.

**Key risks.** Incumbents (Paragraf, Akta) add tender features; portal terms or anti-scraping measures; GDPR on names in court decisions (pseudonymisation needed); an extraction error causing a missed deadline (limit liability in the terms). Lobbying law does not apply to selling data, but it would if the product were used to influence officials (see `government-compute.md`).

**Rough cost to first paying customer.** ~$300–800: domain and email ~$30, a small server ~$10–20 a month, LLM API ~$50–200, a landing page (free tier), and Montenegrin company set-up only when applying for compute (cost **unverified**).

### 2. Local-language AI evaluation lab (BCMS, Albanian, Macedonian)

**What it is.** Independent, regularly updated tests of how well commercial and open models handle Serbian, Croatian, Bosnian, Montenegrin, Albanian and Macedonian: accuracy, legal and banking vocabulary, script handling (Cyrillic/Latin), safety and bias. It is sold as (a) a public free leaderboard for visibility, (b) paid private evaluations ("which model should our bank's chatbot use, and where does it fail?") and (c) licensed test sets.

**Customers.** Banks, telecoms and insurers deploying chatbots; software houses building for local clients; public bodies; AI vendors entering the region. Serbia's own national LLM [15] will also need independent evaluation.

**Use of public compute.**
- Phase 1: run dozens of open-weight models across thousands of prompts. This is classic batch inference with no internet needed, and clearly R&D (no model training).
- Phase 2: client evaluations of closed models use the vendors' APIs and need little compute.

**First 90 days.**
- Recruit an NLP co-founder (Belgrade and Novi Sad universities and the authors of existing benchmarks are the obvious pool).
- Build 500–1,000 native-written test items in BCMS, which the founder can help write and check.
- Publish one comparison report.
- Offer 3 fixed-price pilot evaluations (e.g. €1,500–3,000; **untested**).
- Apply for Fast Lane once the test set exists.

**What a technical partner must do.** Design the evaluation methods, run the evaluation tooling, deploy open models on HPC (Slurm, containers, offline model weights) and check results statistically.

**Evidence of demand.**
- Gap evidence: the main Serbian LLM benchmark is machine-translated from English [12], and community tests found even models built for Serbian scoring poorly [12].
- Serbian SuperGLUE (2026) covers only encoder models [34]; the first Albanian LLM-safety dataset appeared only in 2026 [13].
- Paying-demand evidence is weaker: Giskard's EU funding for AI Act testing [28] shows public money for testing, not local enterprise budgets. **No local paying buyer verified.**

**Key risks.** Enterprises may simply use the leading global model without testing; the state LLM project may fund free evaluations; academic groups publish free benchmarks; test sets leak into training data.

**Rough cost to first paying customer.** ~$400–1,200, mostly API calls to closed models and annotator time if the founder cannot write all items.

### 3. Cyrillic/Latin document digitisation and handwriting recognition

**What it is.** A service that turns scanned archives (municipal records, company files, church and museum collections, old newspapers) into searchable, corrected text and structured metadata in mixed Cyrillic and Latin scripts. A second product is a rights-cleared text corpus licensed to language-model builders, **only** where the owner agrees.

**Customers.** Archives, libraries, museums and municipalities, usually paying with EU, Interreg or donor project money (e.g. DIGIARCH) [36]; private firms digitising old records; universities. A partnership with the National Library of Serbia/LORYA is possible: LORYA is an open-source orchestration platform, "not itself an OCR engine" [16]. A startup could supply the engine and the processing capacity it needs.

**Use of public compute.**
- Phase 1: train/adapt and benchmark OCR/vision models on sample collections. This is light training; **note it**.
- Run large offline batch jobs on staged scans. This is the most HPC-native idea in the shortlist.
- Phase 2: client production runs at scale are a commercial service, so do them on credits or paid compute, not free allocations (they are not R&D).

**First 90 days.**
- Get 3 sample collections (100–500 pages each) from archives the founder can reach in Montenegro and Serbia.
- Compare Transkribus [17] and open models on them.
- Write one grant-backed pilot offer with an archive (Interreg/IPA, Montenegrin Innovation Fund vouchers [31]).

**What a technical partner must do.** OCR/handwriting model selection and adaptation, layout analysis, quality metrics, batch pipelines on HPC, and secure data handling.

**Evidence of demand.**
- Transkribus sells credits (€199 per 1,000 credits; 1 credit ≈ 1 handwritten page) [17].
- UNDP and the National Library say commercial OCR struggled with their mixed-script material [16].
- Interreg funded a cross-border HR–RS archive digitisation project with €267k [36].

**Key risks.**
- **Free competitors:** LORYA, donor projects, Transkribus.
- **Slow buyers:** public budgets and procurement.
- **GDPR:** civil records contain personal and sometimes sensitive data, so check that the HPC centre's terms allow processing client personal data and sign data-processing agreements.
- **Copyright:** newer newspapers.

**Rough cost to first paying customer.** ~$300–900 (Transkribus credits for comparison, travel to archives, a portable scanner if needed).

### 4. EU-accession language toolkit (translation data and quality checks)

**What it is.** Aligned bilingual corpora (EU law in English ↔ Montenegrin, Serbian, Albanian, Macedonian), term banks and automated quality checks for legal translations. It is sold to translation agencies, law firms and consultancies doing accession work. Possibly also to public bodies, but only through open, rule-following procurement.

**Customers.** Translation agencies working on acquis and legal texts; law firms; EU-funded technical assistance projects.

**Use of public compute.** Phase 1: sentence alignment, terminology extraction and large-scale machine-translation comparison over hundreds of thousands of pages (batch, offline). Fine-tuning a translation model would count as training: keep it optional and small. Phase 2: quality checks run cheaply.

**First 90 days.**
- Map who translates the acquis for Montenegro (the Ministry of European Affairs coordinates the work [22]) and which agencies win the contracts.
- Interview 10 agencies and build a free term-checker demo for one chapter.
- The founder's languages are directly useful in terminology review.

**What a technical partner must do.** Alignment pipelines, MT evaluation and integration with translation tools (TMX/TBX formats).

**Evidence of demand.** Montenegro faces ~190,000 pages of acquis, and the EU is considering a temporary derogation because of quality and speed problems [22]. Croatia has raised quality concerns [22]. **No private buyer verified.**

**Key risks.** The main buyer is government, which means procurement, slow payment and FCPA/lobbying sensitivity (see `government-compute.md`). Big translation-tech vendors may cover these languages. Reuse rights for national translations are **unverified**.

**Rough cost to first paying customer.** ~$200–600.

### 5. Wildfire and vegetation risk for Adriatic and Balkan utilities and insurers

**What it is.** Satellite-based maps of vegetation encroachment and fuel risk along power lines and roads, plus burned-area and fire-history layers, for distribution operators, forestry agencies, insurers and large tourism properties.

**Customers.** Electricity distribution companies, insurers and reinsurers covering the coast, and large resorts. Most are state-owned or large, so sales are slow.

**Use of public compute.** Phase 1: process years of free Copernicus Sentinel data (commercial use allowed with attribution [8]) and build the models (light training; note it). Phase 2: seasonal updates are modest and run on credits.

**First 90 days.**
- Find an EO co-founder (a hard requirement).
- Build one demo map for a Montenegrin coastal municipality from free EFFIS and Sentinel data.
- Pitch two insurers and one distribution company.

**What a technical partner must do.** All of the remote-sensing science, validation against ground truth, and the HPC pipelines.

**Evidence of demand.** Overstory raised $43m and serves 6 of the 10 largest utilities in the Americas [23]. Montenegro triggered the EU Civil Protection Mechanism for fires in August 2025, and 2025 was Europe's worst fire year in two decades [27]. **No Balkan buyer verified.** Climate-analytics firms also fail (Cervest, Gro) [24].

**Key risks.** Buyer concentration and procurement; free EU services (EFFIS) cover the basics; credibility needs a scientist; it must stay civilian (avoid security or "monitoring people" uses).

**Rough cost to first paying customer.** ~$200–500 for the demo, but realistically 9–18 months to a first contract.

## How this fits with the brokerage

- **Complement, in knowledge only.** Applying for public compute, writing Slurm jobs and moving from public allocations to credits and then paid capacity is exactly what the brokerage's buyers go through. Doing it yourself gives real credibility. A data or AI startup would also become a small future **buyer** of paid GPUs.
- **Conflict risks.**
  - Do not use the startup's free allocation to run anything for brokerage clients (benchmarks, test jobs). That would be using public compute for a third party's benefit, which is close to resale.
  - Keep the two businesses' records separate.
  - Tell brokerage clients when free public compute suits them better, as `government-compute.md` already requires.
- **Distraction, in practice.** Both need the founder's 20–40 hours for selling. The brokerage needs supplier and buyer outreach; each idea above needs customer discovery **plus** recruiting a co-founder. Under $2,000 cannot fund two entity set-ups, travel to two sets of buyers and a freelancer.
- **Honest view.** Pick one primary business by the end of a 6-week test. Idea 1 is the only one that fits the founder's current skills and can earn money without an engineer from day one. If it gets paying pilots, it is probably a better business than brokerage for a non-technical founder with these languages. If not, return to the brokerage and keep public compute as a lead source.

## Questions for a lawyer / accountant

1. Which entity should apply for EuroHPC or Serbian National AI Platform access: a new Montenegrin d.o.o., a Serbian company in a science-technology park, or both? Set-up and running costs, and the founder's tax position in Montenegro?
2. Do data products, model evaluation, OCR or batch inference count as eligible "AI innovation" under AI Factories Fast Lane/Large Scale and the Serbian platform? Can outputs built on a free allocation be sold commercially afterwards, and must results be published or reported? (Check with the parallel rules research.)
3. Can client-owned personal data (archives, court decisions) be processed on a public HPC system? What data-processing agreements are needed, and does the centre act as a sub-processor?
4. For licensed text datasets: how should Art. 4 TDM opt-outs be checked and documented? What warranties can the startup safely give buyers, given pending CJEU case C-250/25 and the AI Act training-data summary duty that buyers (GPAI providers) carry [29][30]?
5. Are Serbian/Montenegrin court decisions, tender documents and gazettes free to reuse commercially? Do portal terms forbid automated collection?
6. Selling to state-owned utilities, archives or ministries: procurement thresholds, FCPA exposure for the US LLC and the founder, and whether pitching ministries counts as lobbying in Serbia/Montenegro.
7. Accountant: can grant or voucher income (Innovation Fund Montenegro [31], Interreg) and later revenue sit in the local company while the US LLC continues the brokerage? Transfer-pricing or Form 5472 issues between the two?

## Sources

1. EuroHPC JU, Fast Lane access to AI Factories — https://www.eurohpc-ju.europa.eu/ai-factories/ai-factories-access-modes/fast-lane-access-ai-factories_en — checked 2026-11-16
2. EU AI Continent (euacc.ai), AI Factories programme summary (Large Scale 3/6/12 months; temporary closures) — https://www.euacc.ai/programmes/ai-factories ; Bayern Innovativ summary — https://www.bayern-innovativ.de/en/emagazine/detail/opens-ai-data-centers-for-industrial-innovation — checked 2026-11-16 (via search summary)
3. EuroHPC JU Access Policy v2025.12 and eligibility summary, as cited in `government-compute.md` [1][5] — https://www.euacc.ai/can-i-apply/ai-factories — checked 2026-11-16
4. PetaSC, Discoverer Acceptable Use Policy (resale prohibited), as cited in `government-compute.md` [14] — https://docs.discoverer.bg/_downloads/4f6e6f119f308241c158462a8b844cdd/aup.pdf — checked 2026-11-16
5. Biznis.rs, startup applications for free National AI Platform use via science-technology parks — https://biznis.rs/vesti/srbija/pocela-prijava-startap-kompanija-za-besplatno-koriscenje-nacionalne-ai-platforme/ — checked 2026-11-16 (via search summary)
6. Office for IT and eGovernment (Serbia), National Platform for AI — https://www.ite.gov.rs/tekst/en/35/government-data-centredr-location-in-kragujevac.php — checked 2026-11-16 (via search summary)
7. Google for Startups Cloud Program FAQ — https://cloud.google.com/startup/faq — checked 2026-11-16 (via search summary; AWS Activate figures not verified on AWS's own site)
8. Copernicus Sentinel data licence (rev. 1) — https://ewds.climate.copernicus.eu/licences/ec-sentinel — checked 2026-11-16
9. Karya impact page — https://karya.in/impact/ ; ThePrint, Google.org $1m grant to Karya — https://theprint.in/economy/google-org-awards-usd-1-mn-grant-to-karya-to-boost-ai-based-economic-opportunities-for-low-income-communities/2352884 — checked 2026-11-16 (via search summary)
10. TechCrunch, "Nvidia reportedly acquires synthetic data startup Gretel" (19 Mar 2025) — https://techcrunch.com/2025/03/19/nvidia-reportedly-acquires-synthetic-data-startup-gretel — checked 2026-11-16 (via search summary)
11. Neudata, "Feeding the machines" (AI data licensing deals) — https://www.neudata.co/blog/ai-data-licensing-market-analysis — checked 2026-11-16 (via search summary)
12. Serbian LLM eval dataset card — https://huggingface.co/datasets/gordicaleksa/serbian-llm-eval-v1 ; YugoGPT model card — https://huggingface.co/gordicaleksa/YugoGPT ; EQ-Bench-Serbian — https://huggingface.co/datasets/Stopwolf/EQ-Bench-Serbian — checked 2026-11-16 (via search summary)
13. Krsteski et al., open corpus and model for Macedonian (arXiv 2506.09560) — https://arxiv.org/pdf/2506.09560 ; AlbanianLLMSafety (SIGUL 2026), reported via ACL Anthology — https://aclanthology.org/people/isra-fejzullaj/unverified/ — checked 2026-11-16 (via search summary; Albanian item unverified)
14. Mozilla Common Voice 25.0 Serbian — https://prod.datacollective.mozillafoundation.org/datasets/cmn2bjv8101aho107xj4uoklm ; CLARIN.SI Serbian speech corpora (ParlaSpeech-RS, JuzneVesti-SR) — https://www.clarin.si/repository/xmlui/handle/11356/1834 and https://www.clarin.si/repository/xmlui/handle/11356/1679 — checked 2026-11-16 (via search summary; which handle is which not double-checked)
15. UNDP Serbia, Cooperation Protocol on a National Large Language Model (29 Apr 2026) — https://www.undp.org/node/581891 ; Biznis.rs on the protocol with 11 media and institutions — https://biznis.rs/vesti/srbija/potpisan-protokol-o-saradnji-za-izradu-jezickog-modela-za-srpski-jezik-sa-11-medija-i-institucija/ — checked 2026-11-16 (via search summary)
16. UNDP, "LORYA launched" (1 Apr 2026) — https://www.undp.org/node/577236 ; UNDP Digital X, LORYA — https://digitalx.undp.org/lorya_dx3.html ; UNDP blog — https://www.undp.org/node/581001 — checked 2026-11-16 (via search summary; direct fetch blocked)
17. Transkribus, credit packages — https://www.transkribus.org/credit-packages — checked 2026-11-16 (via search summary)
18. DataDrill case study, Akta AI legal intelligence platform — https://pangea.ai/agencies/datadrill/case-studies/akta-ai-legal-intelligence-platform — checked 2026-11-16 (via search summary; developer's own claim)
19. Stanford CodeX TechIndex: Prozone AI — https://techindex.law.stanford.edu/companies/prozone-ai ; Paragraf Lex — https://techindex.law.stanford.edu/companies/paragraf-lex — checked 2026-11-16 (via search summary)
20. Transparency Serbia, Open data in public procurements — https://transparentnost.org.rs/en/projects/221-open-data-in-public-procurements ; Public Procurement Office — https://www.ujn.gov.rs/en/about-us/ — checked 2026-11-16 (via search summary)
21. Western Balkans Investment Framework, procurements — https://www.wbif.eu/procurements ; Blackridge Research, Montenegro tenders database (example) — https://www.blackridgeresearch.com/new-projects-near-me/warehouse-construction-database/tender-rfp-rfq-bid/montenegro/subscribe — checked 2026-11-16 (via search summary)
22. Euronews, "Lost in translation: Montenegro's EU accession faces a language barrier" (1 Oct 2026) — https://www.euronews.com/2026/10/01/lost-in-translation-montenegros-eu-accession-faces-a-language-barrier ; Government of Montenegro, Montenegrin version of the EU acquis — https://gov.me/en/article/montenegrin-version-of-the-eu-acquis — checked 2026-11-16 (via search summary)
23. ESG Today, "Overstory raises $43 million…" — https://www.esgtoday.com/overstory-raises-43-million-to-help-utilities-avoid-wildfires-with-ai/ — checked 2026-11-16 (via search summary)
24. ESG Today, Climate X raises $18m — https://www.esgtoday.com/climate-risk-assessment-platform-climate-x-raises-18-million/ ; Verdantix on Climate X and failures of Cervest/Gro — https://www.verdantix.com/insights/blog/climate-x-raises-18-million-dollars-in-series-a-to-fuel-growth-in-north-america — checked 2026-11-16 (via search summary)
25. Solargis, Global Solar Atlas for the public good — https://solargis.com/es/blog/solargis-news/solargis-develops-global-solar-atlas-for-the-public-good — checked 2026-11-16 (via search summary)
26. BioSense, new technologies in agricultural insurance — https://biosens.rs/en/themes/nove-tehnologije-uspostavljaju-poverenje-izmedju-proizvodjaca-i-osiguravajucih-kuca ; Dunav, soil-moisture deficit insurance — https://www.dunav.com/en/insurance/agriculture/soil-moisture-deficit-insurance/ ; DDOR agricultural innovations — https://www.ddor.rs/en/news/ddor-presents-innovations-in-agricultural-insurance-in-zlatibor/ — checked 2026-11-16 (via search summary)
27. EUMETSAT, wildfires across Europe in 2025 — https://www.eumetsat.int/features/satellite-imagery-captures-devastating-wildfires-across-europe-2025 ; ERCC daily map, Montenegro wildfires (12 Aug 2025) — https://www.gdacs.org/contentdata/maps/daily/WF/1024555/ECDM_20250812_WF_Montenegro.pdf — checked 2026-11-16 (via search summary)
28. Tech.eu, Giskard raises €1.5m (Dec 2022) — https://tech.eu/2022/12/15/helping-keep-quality-in-ai-industry-job-one-giskard-raises-eur15-million/ ; CORDIS, Giskard EIC project — https://cordis.europa.eu/project/id/190198093 — checked 2026-11-16 (via search summary)
29. Freshfields, "AI training & copyright part 2: TDM under court scrutiny" — https://technologyquotient.freshfields.com/post/102mebl/ai-training-copyright-part-2-text-and-data-mining-under-court-scrutiny ; Kneschke v LAION appeal (10 Dec 2025) — https://www.technologyslegaledge.com/2025/12/robert-kneschke-v-laion-judgment-of-10-december-2025-ref-5-u-104-24/ ; EU IP Helpdesk on first CJEU generative-AI hearing (Apr 2026) — https://intellectual-property-helpdesk.ec.europa.eu/news-events/news/cjeu-grand-chamber-rules-music-sampling-and-pastiche-first-cjeu-hearing-generative-ai-and-copyright-2026-04-24_en — checked 2026-11-16 (via search summary)
30. Mayer Brown, EU AI Act GPAI rules and training-data summary template (Aug 2025) — https://www.mayerbrown.com/en/insights/publications/2025/08/eu-ai-act-news-rules-on-general-purpose-ai-start-applying-guidelines-and-template-for-summary-of-training-data-finalized — checked 2026-11-16 (via search summary)
31. Innovation Fund of Montenegro calls (aggregators) — https://www2.fundsforngos.org/business-industry/montenegro-innovation-fund-seeks-projects-to-boost-public-services/ ; innovation vouchers — https://westernbalkans-infohub.eu/?p=8963 — checked 2026-11-16 (via search summary; confirm on fondzainovacije.me)
32. British-Serbian Chamber, interview with Ninamedia owner — https://britserbcham.com/interview-with-dragan-radic-owner-of-ninamedia ; Presscut media archives — https://www1.presscut.hr/en/services/media-archives/ — checked 2026-11-16 (via search summary)
33. Tübingen AI Center, OpenEuroLLM first-year progress — https://tuebingen.ai/news/openeurollm-first-year-progress-and-next-steps ; Fortune on OpenEuroLLM language scope — https://fortune.com/2025/02/10/openeurollm-european-languages-ai-compliance-gdpr-silo-aleph-alpha/ — checked 2026-11-16 (via search summary)
34. Serbian SuperGLUE (LoResLM 2026) — https://preview.aclanthology.org/new-sigs/2026.loreslm-1.30/ — checked 2026-11-16 (via search summary)
35. Serbian court-practice database (Sudska praksa), IRCAI radar listing — https://radar.ircai.org/en/tools/court-practice-database-baza-sudske-prakse/ — checked 2026-11-16 (via search summary)
36. keep.eu, DIGIARCH – Digitization of Archives for Cross-Border Cooperation (Interreg IPA HR–RS) — https://keep.eu/projects/29403 — checked 2026-11-16 (via search summary)
