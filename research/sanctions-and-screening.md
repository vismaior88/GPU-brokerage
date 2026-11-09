# Sanctions and restricted-party screening (OFAC and others)
_Last checked: 2026-11-09_

Covers kickoff Q22 (sanctions half), Q24, and section 6 items 3, 5, 6 and 8 (sanctions half). Export controls (EAR, chips, China) are in a separate file. This file is for staying compliant and knowing which deals to refuse. It is not legal advice.

## Summary

- **Your US LLC is a "US person" for OFAC, wherever you live.** OFAC says all US-incorporated entities and their foreign branches must comply [1]. Living in Montenegro changes nothing.
- **Civil liability is strict.** OFAC can fine you even if you did not know a party was sanctioned. The IEEPA civil maximum is the greater of **$377,700 or twice the transaction value, per violation** [2][3]. Wilful violations are crimes: up to **$1,000,000 and 20 years in prison** for an individual [4].
- **A broker who only introduces parties can still violate sanctions.** "Facilitating" a deal by non-US parties that a US person could not do itself is one of the root causes of violations OFAC lists [5]. Taking no money from the sanctioned party does not make it safe.
- **Hard no-go list (November 2026):** Cuba, Iran, North Korea, Crimea and the so-called Donetsk and Luhansk "republics"; anyone on the SDN list; anyone 50% or more owned by blocked persons. Treat Russia and Belarus as no-go in practice. **Syria is no longer comprehensively sanctioned** (programme ended 1 July 2025) but targeted listings remain [6][7].
- **For GPU compute specifically, the EU has banned providing GPU-as-a-Service and AI model/platform access to Russian entities** (see `eu-uk-local-rules.md`). This makes any Russia-linked compute deal a refusal.
- **Screening can be done for free** with official tools: OFAC Sanctions List Search, the US Consolidated Screening List (covers OFAC plus BIS Entity/MEU/Unverified/Denied lists), the UK Sanctions List search, and the EU list. Budget option when volume grows: OpenSanctions API at €0.10 per check (500 checks for €50) [8][9][10].
- **Screen both sides** (buyer, supplier, their owners and directors, the paying party, the bank country) before any introduction, again before contract and payment, and re-screen active counterparties at least monthly. Save dated proof. **Keep records 10 years** [11].
- **Recommendation:** adopt a written one-page sanctions policy on day one, screen every party with the free tools, save PDFs, and refuse anything on the no-go list without debate. Cost: $0 to about €50 in the first six months.

## Details

### Q22 (sanctions half): how OFAC reaches a US LLC run from Montenegro

**Who is bound.** OFAC FAQ 11: US citizens and permanent residents anywhere, everyone in the US, and "all U.S. incorporated entities and their foreign branches" [1]. Your LLC is bound in everything it does. You personally (if you are not a US citizen or green-card holder) are not a "US person" as an individual, but that gives no room: when you act for the LLC, the LLC acts. Separately, OFAC states that non-US persons may not *cause* or conspire to cause a US person to violate sanctions [1], and the statute penalises anyone who violates, attempts, conspires to violate, or **causes** a violation [4]. Doing a prohibited deal "personally" or through another company instead of the LLC is not a solution; it is evasion and it is also likely to breach Montenegrin law (see the EU/local file).

**Strict liability.** For a civil penalty OFAC does not have to prove you knew. Knowledge matters for the *size* of the penalty and for criminal exposure, not for whether a violation occurred [3].

**Facilitation.** OFAC's compliance framework lists "Facilitating transactions by non-U.S. persons" as a typical root cause of violations [5]. In practice: if a buyer is in Iran or is an SDN, you may not introduce them to any supplier (US or not), negotiate for them, refer them onward, or take a fee. The right response is to stop and decline.

**Services count.** Sanctions programmes prohibit exporting *services*, not only goods. Brokerage, sourcing and referral are services. OFAC also treats cloud services as in scope: its Russia FAQ defines "cloud-based services" as including software delivered through SaaS [12] (the US has banned certain IT consultancy and cloud-based services to Russia since 2024; exact scope **(unverified today)** — treat Russia as no-go anyway).

### Section 6 item 3: sanctioned places and programmes as of November 2026

OFAC lists 36 active programmes [6]. The ones that matter for you:

| Jurisdiction / programme | Status Nov 2026 | Broker rule |
|---|---|---|
| **Cuba, Iran, North Korea** | Comprehensive embargoes, all active [6] | Refuse any party located, organised or ordinarily resident there, or owned by their governments |
| **Crimea, so-called DNR/LNR regions of Ukraine** | Comprehensive regional embargo (Ukraine-/Russia-related programme) [6] | Refuse |
| **Russia** | Not a full embargo, but very broad: thousands of SDNs, services bans, export controls. Some limited US easing in 2026 (delistings, temporary licences); no general lifting found [13] | Treat as refuse. EU bans GPU/AI services to Russian entities outright |
| **Belarus** | Active programme; notable US easing in 2026 (Directive 1 rescinded 26 Mar 2026, some delistings) [13]. EU measures remain | Treat as refuse unless a sanctions lawyer clears it |
| **Syria** | **Changed.** OFAC's Syria programme ended 1 July 2025; Caesar Act repealed Dec 2025; Assad-linked persons moved to the "PAARSS" programme; HTS-related terrorism listings were reported as remaining in 2025 [7][6]. Export controls on Syria are a separate question (see export-control file) | Not automatically banned, but high risk. Screen carefully; get advice before any Syria-linked deal |
| **Venezuela** | Framework still in force; government of Venezuela remains blocked; eased through general licences during 2026 [14] | Lawyer-only |
| **List-based programmes** (terrorism, narcotics, cyber, Global Magnitsky, Balkans-related, Chinese military companies, etc.) | Active [6] | Covered by name screening. Note the **Balkans-related** programme: it lists individuals and companies in Serbia, Bosnia, Montenegro and Kosovo |

Old conduct stays punishable: in February 2026 OFAC fined an individual $3,777,000 for Syria violations committed while the programme was in force, after it had been lifted [15].

**The 50% rule.** Any entity owned 50% or more, directly or indirectly, by one or more blocked persons is itself blocked even if it is not on any list. Stakes of several blocked persons are added together. Control without 50% ownership does not trigger the rule automatically, but OFAC urges caution, and a blocked individual cannot sign or act for a non-blocked company (FAQs 398–401) [16]. This is why you must ask who owns a counterparty, not only screen its name.

**Front companies.** Typical signs: company formed recently, no web presence or staff, address at a formation agent, owner is a nominee, business line unrelated to AI, payment from a different company or country. OFAC's 2025 cases stress that it looks through formal ownership to proxies: a venture firm was fined $216 million for dealing with a known proxy of a sanctioned oligarch, and a lawyer was fined $1.09 million although he had legal advice, because a family member was in fact acting as the oligarch's proxy [17][18].

Note on BIS: a separate BIS "Affiliates Rule" (50% rule for the Entity List) was suspended from 10 Nov 2025 to 9 Nov 2026 [19]. **Its status from 10 Nov 2026 could not be confirmed (unverified)** — check bis.gov. Safest practice: treat any company 50%+ owned by an Entity List or MEU List party as restricted.

### Section 6 item 8 (sanctions half): penalties and what "knowledge" means

| Item | Rule | Source |
|---|---|---|
| Civil maximum (IEEPA) | Greater of $377,700 or 2x transaction value, per violation; no 2026 inflation increase reported | [2][3] |
| Criminal (wilful) | Up to $1,000,000 fine; individuals up to 20 years | [4] |
| Time limit | 10 years (statute of limitations extended in 2024); records must be kept 10 years | [11] |
| Base penalty, non-egregious + self-disclosed | Half the transaction value, capped at $188,850 per violation | [3] |
| Base penalty, non-egregious, not disclosed | "Schedule amount" ($1,000 to $377,700 depending on deal size) | [3] |
| Base penalty, egregious | Statutory maximum (half if self-disclosed) | [3] |

- **How OFAC decides (Enforcement Guidelines, 31 CFR 501 App. A)** [3]: was it wilful or reckless; did you know or have **reason to know** (should you have known from available information and reasonable due diligence); harm to the sanctions programme; your size, sophistication and finances; whether you had a compliance programme; remediation; cooperation. Outcomes range from no action or a cautionary letter up to a penalty or criminal referral.
- **Recklessness** includes ignoring warning signs. Deliberately not asking, so that you do not "know", counts against you; in criminal law it can be treated as knowledge (wilful blindness — confirm with counsel).
- **Small size helps but does not exempt.** Size and financial condition are mitigating factors [3]. A first violation can cut the base penalty by up to 25%; substantial cooperation 25–40% [3].
- **Voluntary self-disclosure (VSD):** telling OFAC yourself before or at the same time as the government finds out. It roughly halves the base penalty [3]. If you ever discover a problem: stop, preserve records, call a sanctions lawyer the same day.

**Instructive enforcement cases**

| Case | Amount | Lesson |
|---|---|---|
| TradeStation Securities, Mar 2026 | $1.11M | Online broker's IP geo-block silently failed on its mobile app; users in Iran, Syria, Crimea traded. Self-disclosed, non-egregious [20] |
| Interactive Brokers, Jul 2025 | $11.8M | Had customer IP data but blocking and screening had gaps [21] |
| SAP, 2021 | $8.3M combined (OFAC/DOJ/BIS) | Cloud and software delivered to Iranian IP addresses and via resellers; ignored internal audit warnings about geolocation [22] |
| Extreme Networks, Oct 2026 | $1.53M | Purchase orders named one end user but contained contact details of a Russian defence firm majority-owned by a designated company. Red flags in paperwork were ignored [23] |
| GVA Capital, Jun 2025 | $216M | Knew the real party was a sanctioned oligarch acting through a proxy [17] |
| Individual (lawyer), Dec 2025 | $1.09M | "Gatekeepers" and intermediaries are held responsible; legal advice based on wrong facts did not protect him [18] |
| Individual, Feb 2026 | $3.78M | Individuals are fined personally; lifted programmes do not erase past violations [15] |
| Rice Lake Weighing Systems (Aug 2026), Pegasus Worldwide Logistics (Oct 2026) | $60,764 and $175,015 | OFAC does pursue small cases (details not reviewed) [24] |

Takeaway for a compute broker: OFAC expects you to use information you already hold (IP addresses, email domains, phone codes, billing address, paperwork inconsistencies). Sidley's review of 2025 notes OFAC treats advisers and intermediaries as gatekeepers [18].

### Q24: how to screen buyers and suppliers

**Who to screen in every deal:** the buyer company; the supplier company; each one's parent, 25%+ owners and directors/signatories; your individual contacts; the actual end user if different from the buyer; the payer if different; the data-centre operator/owner if different from the supplier.

**Lists and free official tools**

| List | Tool | Cost | Notes |
|---|---|---|---|
| OFAC SDN and other OFAC lists | sanctionssearch.ofac.treas.gov | Free | Fuzzy matching with adjustable score; shows list date (updated 9 Nov 2026 when checked) [25] |
| **US Consolidated Screening List** (OFAC SDN, SSI, FSE, CMIC etc. + BIS Entity List, Denied Persons, Unverified List, Military End User List + State Dept lists) | trade.gov/data-visualization/csl-search; CSV/JSON download; API | Free (API key free per trade.gov) | Fuzzy search; updated daily 5:00 AM ET. Trade.gov warns it is an aid, not a substitute for due diligence [8] |
| UK Sanctions List | search-uk-sanctions-list.service.gov.uk | Free | Since 28 Jan 2026 the only UK list; the old OFSI consolidated list is closed [26] |
| EU consolidated financial sanctions list | sanctionsmap.eu / EU Financial Sanctions Files | Free | Could not load today **(unverified today)** |
| UN Security Council consolidated list | un.org (Security Council) | Free | Largely included in EU/UK/US lists **(unverified today)** |
| Montenegro consolidated register of designated persons | Ministry of Interior | Free | Montenegrin law requires checking it before a business relationship (see local-rules file) [27] |

**Aggregators (one search across all lists)**

| Tool | Price | Comment |
|---|---|---|
| OpenSanctions | Data is CC BY-NC: **any use inside a for-profit business needs a licence**. Hosted API: €0.10 per query; bundles 500 = €50, 5,000 = €400; 2,000 free trial credits with a business email; credits valid one year [9][10] | Best value. Covers US, EU, UK, UN and many national lists plus PEPs. Do not use the free bulk data commercially |
| SanctScan | Free tier 25 screenings/month; paid from $19/month (third-party listing, **unverified on vendor site**) [28] | |
| TrueCheck | $19/month for 50 scans (third-party listing, **unverified**) [28] | |
| SanctionsLookup | From $49/month (third-party listing, **unverified**) [28] | |
| AML Watcher | $95/month (third-party listing, **unverified**) [28] | Includes adverse media, monitoring |
| Sanction Scanner, AEB, enterprise tools | ~€990/month and up (third-party listing, **unverified**) [28] | Not for this budget |

**Recommendation:** months 1–6 use the official free tools (OFAC search + CSL + UK + EU). When you have more than a handful of live counterparties, buy a €50 OpenSanctions bundle. A paid subscription is not needed before revenue.

**How to document a screening (do this every time)**
1. Save a PDF/screenshot of each search showing the name searched, the tool, the date/time and the list date.
2. Search legal name, trading name, former names, and local-script spelling (Cyrillic, Chinese) where relevant; set fuzzy score around 80–85 and review near matches.
3. For each possible match, write one line why it is or is not the same party (date of birth, address, registration number).
4. Record ownership: who owns 25%+ and who ultimately controls; source of that information.
5. Log in a spreadsheet: deal ID, party, role, date, tools, result, your decision, your initials.
6. If a true match: stop all work, do not "tip off" with advice on alternatives, record the refusal, and call a lawyer before doing anything else (blocked-property reporting duties can apply to US persons).

**How often**
- Before first substantive engagement (before sending supplier names or quotes).
- Again before signing and before each payment or commission.
- All active buyers, suppliers and partners: monthly, and when a major new sanctions action is announced. Lists change almost daily (OFAC's list was updated on the day of this check [25]).
- When ownership, payer or end user changes.

**Beneficial-ownership sources**

| Source | Use | Note |
|---|---|---|
| Customer's own signed ownership declaration + registry extract | Primary method | Ask for it in intake |
| GLEIF LEI search | Free; has "who owns whom" parent data for entities with an LEI [29] | Many small firms have no LEI |
| OpenCorporates, UK Companies House (PSC register) | Free basic search **(unverified today)** | |
| Serbia APR and Montenegro CRPS company registers | Free online; show founders/directors **(unverified today)** | Useful for local counterparties |
| EU beneficial-ownership registers | Access often restricted to those with "legitimate interest" since a 2022 EU court ruling **(unverified today)** | |
| OpenSanctions | Links sanctioned persons to companies they own | Paid for business use [9] |

If ownership cannot be established, treat that as a red flag in itself.

### Section 6 item 5: payment and behaviour red flags (sanctions view)

- Wants to pay in crypto, cash, or through a personal account.
- Payer is a different company or in a different country from the buyer, with no clear reason (OFAC lists "non-standard payment or commercial practices" as a root cause of violations [5]).
- Payment routed from or via a sanctioned or high-risk jurisdiction; bank you cannot identify.
- Refuses to name the end user or owners; gives a free-mail address; newly formed shell.
- Email domain, phone code, time zone, language or IP address point to Russia, Belarus, Iran, Cuba, North Korea, Crimea while the paperwork says UAE, Turkey, Kazakhstan, Kyrgyzstan, Armenia, Serbia, Hong Kong, etc.
- Asks you to remove names from documents, split invoices, or use a different contracting entity "for compliance reasons".
- Urgency, no price sensitivity, no technical questions.
- Asks whether the supplier checks IPs or allows VPN access.

Any one of these means pause and resolve it in writing. Two or more unresolved means decline. Never suggest how a buyer could restructure to pass.

### Section 6 item 6: supplier-side sanctions risks

- **Sanctioned or 50%-owned suppliers.** Receiving a commission from a blocked supplier is as prohibited as serving a blocked buyer. Screen the supplier, its parent, and its investors.
- **Data-centre location.** Refuse capacity physically located in Russia, Belarus, Iran, Cuba, North Korea, or occupied Ukrainian regions. Treat capacity in jurisdictions known as diversion hubs with extra checks on who owns the operator.
- **Russian-owned hosting outside Russia.** OFAC has designated hosting providers that served cybercriminals ("bulletproof hosting") in 2025 [21]. Check hosting brands and their owners.
- **Unknown hardware origin.** Chips that were smuggled or diverted are an export-control problem (see other file) and often go with opaque ownership.
- **Payment chain.** A supplier asking you to accept commission from an unrelated offshore company is a red flag on the supply side too.

## Questions for a lawyer / accountant

1. Confirm the facilitation analysis for a pure referral model (no money handled): which exact activities are prohibited when a prospect turns out to be in a sanctioned jurisdiction?
2. If a counterparty is a true SDN match, what blocking/reject reports must the LLC file and by when?
3. Does my personal nationality (and any second citizenship) change which sanctions regimes bind me personally?
4. Status of the BIS Affiliates Rule after 9 Nov 2026 and how it interacts with screening.
5. Is a one-page sanctions policy plus the screening log an adequate "risk-based compliance programme" for a one-person broker?
6. Any deal touching Syria, Venezuela or Belarus: is a licence or general licence needed?

## Sources

1. OFAC FAQs – Basic information (FAQ 11, 7, 13, 91), https://ofac.treasury.gov/faqs/topic/1501 — checked 2026-11-09
2. 31 CFR 505.401 text via CustomsMobile (IEEPA maximum $377,700), https://www.customsmobile.com/regulations/expand/title31_chapterV_part505_subpartD_section505.401 ; Baker McKenzie civil penalties category (OMB M-26-11, no 2026 adjustment), https://sanctionsnews.bakermckenzie.com/category/ofac/civil-monetary-penalties/ — checked 2026-11-09 (search summary)
3. OFAC Economic Sanctions Enforcement Guidelines, 31 CFR Part 501 App. A, https://www.law.cornell.edu/cfr/text/31/appendix-A_to_part_501 — checked 2026-11-09
4. 50 U.S.C. § 1705 (IEEPA penalties), https://www.law.cornell.edu/uscode/text/50/1705 — checked 2026-11-09
5. OFAC, A Framework for OFAC Compliance Commitments, https://ofac.treasury.gov/media/16331/download?inline — checked 2026-11-09
6. OFAC Sanctions Programs and Country Information, https://ofac.treasury.gov/sanctions-programs-and-country-information — checked 2026-11-09
7. OFAC Syria FAQs, https://ofac.treasury.gov/faqs/topic/1571 ; Willkie, "A new era: United States lifts comprehensive sanctions on Syria", https://www.willkie.com/publications/2025/07/a-new-era-united-states-lifts-comprehensive-sanctions-on-syria ; Sheppard Mullin on Caesar Act repeal, https://www.sheppard.com/insights/blogs/unpacking-the-u-turn-what-the-syria-sanctions-repeal-really-means — checked 2026-11-09 (search summary)
8. US ITA, Consolidated Screening List, https://www.trade.gov/consolidated-screening-list — checked 2026-11-09
9. OpenSanctions licensing and non-commercial exemption, https://www.opensanctions.org/licensing/ and https://www.opensanctions.org/docs/commercial/exemption/ — checked 2026-11-09
10. OpenSanctions API pricing, https://www.opensanctions.org/api/ — checked 2026-11-09
11. Federal Register, OFAC recordkeeping rule (10 years), 21 Mar 2025, https://www.govinfo.gov/content/pkg/FR-2025-03-21/html/2025-04864.htm ; Greenberg Traurig summary, https://www.gtlaw.com/en/insights/2025/4/us-treasury-extends-recordkeeping-requirement-for-economic-sanctions-compliance-to-10-years — checked 2026-11-09 (search summary)
12. OFAC FAQ 1186 (cloud-based services definition), https://ofac.treasury.gov/faqs/1186 — checked 2026-11-09 (search snippet only)
13. Mondaq, OFAC rescinds Belarus Directive 1, https://www.mondaq.com/unitedstates/export-controls-trade-investment-sanctions/1779588/ ; Steptoe sanctions update 30 Mar 2026, https://www.steptoe.com/en/news-publications/stepwise-risk-outlook/sanctions-update-march-30-2026.html ; FDD brief 2 Nov 2026, https://www.fdd.org/?p=311972 — checked 2026-11-09 (search summary)
14. Faegre Drinker, Venezuela sanctions changes (Mar 2026), https://www.faegredrinker.com/en/insights/publications/2026/3/unpacking-the-recent-changes-to-the-venezuela-sanctions-program — checked 2026-11-09 (search summary)
15. OFAC enforcement release, individual, 25 Feb 2026, https://ofac.treasury.gov/system/files/2026-02/20260225_individual.pdf ; Hogan Lovells summary, https://www.hoganlovells.com/en/publications/ofac-settles-37-million-enforcement-action-for-apparent-violations-of-syria-sanctions — checked 2026-11-09 (search summary)
16. OFAC FAQs – Entities owned by blocked persons (50% rule), https://ofac.treasury.gov/faqs/topic/1521 — checked 2026-11-09
17. OFAC 2025 enforcement information, https://ofac.treasury.gov/civil-penalties-and-enforcement-information/2025-enforcement-information — checked 2026-11-09
18. Sidley, Five key takeaways from 2025 US sanctions enforcement, https://www.sidley.com/en/insights/newsupdates/2026/02/five-key-takeaways-from-2025-us-sanctions-enforcement — checked 2026-11-09
19. Arnold & Porter, DOC suspends enforcement of the Affiliates Rule for one year, https://www.arnoldporter.com/en/perspectives/blogs/enforcement-edge/2025/11/doc-suspends-enforcement-of-the-affiliates-rule-for-one-year — checked 2026-11-09 (search summary)
20. OFAC recent action 17 Mar 2026 (TradeStation), https://ofac.treasury.gov/recent-actions/20260317 ; Paul Hastings analysis, https://www.paulhastings.com/insights/client-alerts/ofac-settlement-highlights-importance-of-testing-and-auditing-sanctions-compliance-controls — checked 2026-11-09 (search summary)
21. Willkie, Interactive Brokers $11.8M settlement, https://complianceconcourse.willkie.com/articles/u-s-broker-dealer-reaches-11-8-million-settlement-with-ofac-for-apparent-violations-of-u-s-sanctions/ ; Treasury press release on bulletproof hosting designations (2025), https://home.treasury.gov/news/press-releases/sb0319 — checked 2026-11-09 (search summary)
22. Kelley Drye, SAP case and cloud providers, https://www.kelleydrye.com/viewpoints/client-advisories/over-8-million-in-fines-sap-case-highlights-sanctions-risks-and-compliance-expectations-for-cloud-providers-and-software-companies — checked 2026-11-09 (search summary)
23. AML Watcher, OFAC fines Extreme Networks, https://amlwatcher.com/news/ofac-fines-extreme-networks-1-53-million-over-russia-sanctions-violations/ ; MLex, https://www.mlex.com/mlex/articles/2543182 — checked 2026-11-09 (secondary sources; OFAC release not read)
24. OFAC 2026 enforcement information, https://ofac.treasury.gov/civil-penalties-and-enforcement-information — checked 2026-11-09
25. OFAC Sanctions List Search, https://sanctionssearch.ofac.treas.gov/ — checked 2026-11-09
26. UK FCDO, The UK Sanctions List, https://www.gov.uk/government/publications/the-uk-sanctions-list — checked 2026-11-09
27. Montenegro, Zakon o restriktivnim mjerama (Sl. list CG 119/24), Art. 18, https://www.cbcg.me/slike_i_fajlovi/fajlovi/fajlovi_brzi_linkovi/propisi/zakoni/zakon_o_restriktivnim_mjerama_119-24.pdf — checked 2026-11-09
28. Capterra/GetApp/FitGap listings (SanctScan, TrueCheck, SanctionsLookup, AML Watcher, Sanction Scanner), e.g. https://www.capterra.com/p/10047441/SanctionsLookup/ , https://www.capterra.com/p/10015265/AML-Watcher/ , https://us.fitgap.com/search/anti-money-laundering-software/small-business — checked 2026-11-09 (search summary; vendor sites not verified)
29. GLEIF Global LEI Index, https://www.gleif.org/en/lei-data/global-lei-index — checked 2026-11-09
