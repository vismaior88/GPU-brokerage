# EU, UK, Montenegro and Serbia rules that touch a GPU compute broker
_Last checked: 2026-11-09_

Covers kickoff Q25. US sanctions are in `sanctions-and-screening.md`; US export controls are in a separate file. Not legal advice. Research note: web search capacity ran out part-way through, so several points rest on primary texts I could read plus prior knowledge; those are marked **(unverified)**.

## Summary

- **The EU explicitly bans renting GPU compute to Russia.** Article 5n(1)(h) of Regulation 833/2014 prohibits providing "high-performance computing services, including access to GPU-accelerated computing" to the Russian government and to entities established in Russia. The Commission's FAQ (22 Jan 2026) says this covers "renting GPU-powered virtual machines or bare-metal servers via compute marketplaces or cloud platforms". Article 5n(1)(g) bans AI model access and AI training/fine-tuning/inference platforms [1]. Every EU supplier you work with is bound by this.
- **Indirect supply is also banned.** Serving a non-Russian subsidiary is prohibited if the service is really for the benefit of the Russian parent [1]. This is the key test for Russian-owned companies in Serbia, UAE, Kazakhstan, Armenia, etc.
- **Montenegro aligns with EU sanctions and has its own law.** The Law on Restrictive Measures (Official Gazette 119/24) applies to companies *and natural persons*. It requires checking the national consolidated register **before any business relationship or transaction**; fines are €500–4,000 for an individual and €1,000–40,000 for a company [2]. You are personally inside this regime because you live there.
- **Serbia does not apply EU sanctions on Russia.** As of July 2026 it again declined to align with Russia-related EU decisions [3]. That does not relax anything for you: your LLC is bound by US law, your EU suppliers by EU law, and you personally by Montenegrin law. Serbia-based, Russian-owned buyers need enhanced checks.
- **You are probably not an AML "obliged entity" in Montenegro.** The list in Article 4 of the AML law covers banks, payment and crypto firms, accountants, tax advisers, company-formation agents, real-estate agents and similar. A broker of IT/cloud services is not on it [4]. Confirm with a local lawyer.
- **EU dual-use rules (Reg. 2021/821) and UK rules bind EU/UK parties, not your US LLC directly**, but they shape what your suppliers can accept. The **EU AI Act** and **EU Data Act** put duties on AI providers and cloud providers, not on a referral broker.
- **Open local question (lawyer needed):** whether running a US LLC's business day-to-day from Montenegro requires registering a branch or creates a local taxable presence. Not verified here.
- **Recommendation:** one policy for all regimes — refuse any deal where the buyer, end user, owner or beneficiary is Russian, Belarusian or otherwise sanctioned under US, EU, UK or UN lists; screen against all four plus the Montenegrin register; book one hour with a Montenegrin lawyer on the local-presence and personal-liability questions.

## Details (Q25)

### 1. EU sanctions

**Who is bound.** EU sanctions regulations apply within EU territory, to EU nationals anywhere, to companies incorporated in the EU, and to any business done in whole or in part in the EU **(scope clause from prior knowledge; unverified today)**. Your US LLC, run from Montenegro, is not automatically bound. But:
- if you hold an EU citizenship (for example Croatian), you personally are bound everywhere — tell your lawyer;
- every EU supplier and EU buyer you deal with is bound, and will push the obligations onto you by contract;
- Montenegro imports EU measures into its own law (section 4).

**The GPU/AI services ban (most important finding).** The Commission's services FAQ, updated 22 January 2026 [1]:

| Provision | What is banned for the Russian government and entities established in Russia |
|---|---|
| Art. 5n(1)(h) | High-performance computing services incl. GPU-accelerated computing: renting GPU VMs or bare metal "via compute marketplaces or cloud platforms", API access to GPU/HPC clusters, supercomputer time; quantum computing services |
| Art. 5n(1)(g) | AI services: access to hosted models (LLM, image, translation, code) and to platforms for training, fine-tuning and inference, including providing GPU/TPU resources for training |
| Art. 5n(1)(e) and 5n(3) | IT consultancy; certain enterprise and design software in any form, including SaaS. General cloud services are *not* "IT consultancy" (FAQ 29), but HPC and AI services are caught by (g) and (h) |

- "Directly or indirectly": services to a non-Russian entity are prohibited if they "would actually be for the benefit of the parent company established in Russia" (FAQ 4). Outsourcing through someone else is also indirect provision (FAQ 5) [1].
- Article 12 separately prohibits knowingly taking part in circumvention [1].
- The date these two limbs were added and the exact legal text were not checked **(unverified; I believe the 19th package, autumn 2025)**.
- The **20th package** was adopted 23 April 2026 (Regulation 2026/506). It added, among other things, a ban on managed cybersecurity services to Russia, a ban on dealing with Russian crypto-asset service providers, and the first use of the anti-circumvention tool against a third country (Kyrgyzstan) [5]. Whether a later package exists was not checked **(unverified)**.
- **Belarus:** the EU adopted parallel Belarus measures with the 20th package [5]. Whether the GPU/AI services ban is mirrored for Belarus was not checked **(unverified)** — treat Belarus the same as Russia.
- **Iran:** after the 2025 return of UN nuclear sanctions, the EU re-imposed dual-use and other restrictions on Iran (Regulation 2026/759, 30 March 2026) [6].

**What it means for the broker.** A deal where an EU supplier's GPUs end up serving a Russia-established entity is illegal for the supplier. If you arranged it, you would be the person who caused the breach, with contract liability and, in Montenegro, likely a direct offence. Refuse.

### 2. EU dual-use Regulation (EU) 2021/821

- It controls export, brokering, technical assistance, transit and transfer of listed dual-use *items* (goods, software, technology) [7]. "Technical assistance" means technical support such as repair, development, manufacture, testing, maintenance or other technical service related to a listed item, and the recast regulation added a licence requirement for some technical assistance by EU providers [7].
- **Is selling cloud access caught?** Renting compute is a service; it is not in itself the export of a listed item. The regulation bites when controlled *technology or software* is transferred electronically (for example a customer uploading controlled data to servers abroad, or giving foreign staff access). That is primarily the customer's and supplier's obligation. I found no EU-wide rule equivalent to the US approach on remote access to advanced chips **(unverified — absence of evidence only)**.
- "Brokering services" in this regulation means arranging the sale or supply of dual-use *items* between third countries **(definition from prior knowledge; unverified today)**. Brokering cloud capacity is not that. If you ever broker physical GPU servers, this changes: get advice first.
- The EU control list (Annex I) was updated by Delegated Regulation 2025/2003 (adopted 8 Sept 2025); sources conflict on its effective date [7].
- The regulation binds EU-established persons. Your LLC is outside, but Montenegro has a parallel law (section 4).

### 3. UK

- UK sanctions apply to all conduct in the UK and to UK persons anywhere; a non-UK company was penalised in 2026 on the basis of a UK bank account it controlled [8].
- Civil liability has been strict since June 2022 (no need to prove knowledge) [8].
- The **UK Sanctions List** is, since 28 January 2026, the single UK list; the OFSI consolidated list is closed [9]. Search it free at search-uk-sanctions-list.service.gov.uk.
- The UK has its own Russia services and technology bans; whether they name GPU/cloud compute as the EU does was not checked **(unverified)**.
- UK export-control rules on cloud storage of controlled technology exist (ECJU guidance) **(unverified)**.
- Relevance to you: only when a UK buyer, UK supplier, UK national or a UK bank account is involved. Then screen against the UK list and assume UK parties cannot touch Russian/Belarusian business.

### 4. Montenegro (your country of residence)

**Alignment with EU sanctions — verified.** Montenegro declared alignment with the EU's July 2026 Russia-related Council decisions, as it has with earlier ones; the Prime Minister states Montenegro fully follows EU foreign policy [3][10].

**Law on Restrictive Measures (Zakon o restriktivnim mjerama, Sl. list CG 119/24, adopted 10 Dec 2024)** — read in the original [2]:

| Point | What the law says |
|---|---|
| Sources of measures (Art. 2) | UN Security Council resolutions; EU acts (introduced by Government decision); other international organisations; plus a national list |
| Types (Art. 5) | Includes restrictions on "providing assistance and services, including IT services and software" |
| Who must apply (Art. 18(1)) | State bodies, legal persons, **natural persons carrying on a business, and natural persons generally** |
| Screening duty (Art. 18(2)) | Check the Consolidated Register of Designated Persons and Restrictive Measures **before establishing any business relationship or executing a transaction** |
| Reporting (Art. 18(3)–(4)) | If you refuse a designated person, or a counterparty is later designated, notify the Ministry of Interior without delay and end the relationship |
| Fines (Arts. 60–61) | Natural person €500–4,000; legal person €1,000–40,000; entrepreneur €500–4,000 |
| Coordination | Standing Coordination Body for Restrictive Measures; Ministry of Foreign Affairs publishes the acts |

- The Government adopts decisions transposing EU measures on Russia, Iran and others (for example a decision of 14 May 2026) [11]. Whether the EU GPU/AI services ban has been transposed word-for-word was not checked **(unverified)** — assume yes.
- US (OFAC) lists are not a source under this law; you follow those because of the LLC.
- Practical step: find out how a private person accesses the Consolidated Register (Ministry of Interior) and add it to your screening routine **(access method unverified)**.
- Criminal-law exposure for sanctions breaches in Montenegro was not researched **(unverified)**.

**Export control.** The Law on Export Control of Dual-Use Goods (Sl. list CG 145/21) regulates export and transit of dual-use goods and "provision of brokerage services and technical assistance related to dual-use goods"; the national control list (30/25) is harmonised with the EU list; licences come from the ministry responsible for the economy [12]. Brokering cloud *services* is not brokering dual-use *goods*, so no licence should be needed for the planned model — but brokering hardware from Montenegro could need one. Text of the law not read **(unverified detail)**.

**AML.** The Law on Prevention of Money Laundering and Terrorist Financing (110/23, last amended 59/26) lists obliged entities in Article 4: banks, lenders, payment and e-money institutions, investment and insurance firms, gambling, pawnshops, crypto-asset service providers, auditors/accountants/tax advisers, company-formation and "business or fiduciary services", asset managers, real-estate, dealers in vehicles/vessels/precious goods above €10,000, lawyers and notaries in certain transactions [4]. **A broker of cloud/IT services is not listed.** Two cautions:
- do not hold or pass client money (that moves you toward payment services, which are regulated);
- accepting crypto does not make you a crypto service provider, but it is a red flag for other reasons (see payments research).

**Does working from Montenegro for a US LLC create a local issue? (flag for local lawyer)** Not verified. Questions that normally arise: whether continuous business activity by a foreign company through a resident manager requires registering a "part of a foreign company" (branch) in the business register; whether it creates a permanent establishment for corporate tax; your personal income tax and social contributions on LLC profits; whether the LLC is then "established" in Montenegro for data-protection purposes (see GDPR file). No special licence for brokering compute services was found in any text read.

### 5. Serbia

- **Not aligned on Russia — verified.** On 29 July 2026 N1 reported Serbia did not align with four EU decisions of 13 July, including the Russia-related ones, while Montenegro, Albania, North Macedonia and Bosnia did [3]. Reporting in August 2026 states Serbia has not imposed sanctions on Russia [13].
- **US action has reached Serbia anyway.** OFAC has sanctioned Serbian companies for supplying Russia (MCI Trading, Kominvex, Goodforwarding, Soha Info, TR Industries, and in October 2024 Ventrade); the same action hit a Montenegrin company, IBC Bar, owned by a Russian national living in Montenegro [14]. RFE/RL counted eleven Serbian firms on Western blacklists and at least $71 million of dual-use goods moved to Russia via Serbian companies [14].
- **NIS**, Serbia's oil company majority-owned by Gazprom Neft, is under US sanctions and has operated on short OFAC licences while a sale to Hungary's MOL is negotiated (still pending in August 2026; later status **unverified**) [13]. Lesson: a household-name Serbian company can be a sanctioned party through its ownership.
- **Implications for deals:**
  - Serbian law will not stop a Serbian buyer from working with Russia; your obligations do. Do not rely on "it is legal in Serbia".
  - Many Russian-founded IT companies have operated from Serbia since 2022 **(general context; unverified today)**. Russian nationality or ownership alone is not a prohibition under OFAC. The questions are: is any owner an SDN or EU/UK-listed (50% rule)? Is there a Russian parent, Russian staff using the compute from Russia, or Russian customers benefiting? If the service is for the benefit of an entity established in Russia, EU suppliers cannot provide it [1] and you should refuse.
  - For Serbia-based buyers ask for: company register extract (APR), ownership up to natural persons, where the users log in from, who the end customers are, and a written end-use statement. Decline if answers are evasive.
  - Serbian suppliers/data centres: check owners for Russian state or listed-party links before offering their capacity to EU or US buyers.
- Serbia's own sanctions, export-control and AML laws were not reviewed **(unverified)**. They matter only if you form a Serbian entity or act as an agent there.

### 6. EU AI Act and EU Data Act — only where they touch a broker

| Law | Who carries the duties | Effect on a referral/fee broker |
|---|---|---|
| EU AI Act (Reg. 2024/1689) | Providers and deployers of AI systems; providers of general-purpose AI models **(from prior knowledge; unverified today)** | None directly. You do not build or deploy AI by brokering compute. Do not tell buyers that a supplier makes them "AI Act compliant" |
| EU Data Act (Reg. 2023/2854), applies since 12 Sept 2025 [15] | "Providers of data processing services" (cloud/IaaS suppliers): must enable switching between providers [15]; must protect non-personal data in the EU against unlawful foreign-government access; switching fees phased out by Jan 2027 **(last two points unverified today)** | None directly as a broker. Useful as a checklist: ask EU-facing suppliers about exit terms and egress fees. If you later **resell** capacity under your own contract you may become a provider yourself — get advice before that step |
| NIS2 / DORA | Cloud providers and regulated buyers (banks, insurers) **(unverified)** | Regulated buyers will send long supplier questionnaires; pass them to the supplier, do not answer for them |

## Questions for a lawyer / accountant

1. (Montenegro) Must the US LLC register a branch or does it have a permanent establishment because I run it from Montenegro? Any business licence needed for intermediary services?
2. (Montenegro) How do I access the Consolidated Register of Designated Persons, and does Art. 18 apply to each referral I make for a foreign company?
3. (Montenegro) Has the EU ban on GPU/AI services to Russia been transposed, and what is my personal (including criminal) exposure?
4. (Montenegro) Confirm that a compute/IT services broker is not an AML obliged entity under Art. 4.
5. (EU) Do EU sanctions bind me personally through any EU citizenship I hold? Does soliciting EU customers count as business "done in the Union"?
6. (Serbia) If I sign Serbian suppliers or buyers, or later set up a Serbian company, which Serbian licensing, AML and export rules apply?
7. (EU/UK) Has the UK adopted an equivalent GPU/AI services ban, and is there one for Belarus?

## Sources

1. European Commission, FAQs – Provision of services, Article 5n of Council Regulation 833/2014, as of 22 January 2026 (FAQs 4, 5, 29, 38, 39), copy hosted by Czech Customs: https://celnisprava.gov.cz/cz/Documents/2026-01-26--FAQs-sanctions-Russia-Services-provision_en.pdf — checked 2026-11-09 (full text read)
2. Montenegro, Zakon o restriktivnim mjerama, Sl. list CG 119/24 (Central Bank copy), https://www.cbcg.me/slike_i_fajlovi/fajlovi/fajlovi_brzi_linkovi/propisi/zakoni/zakon_o_restriktivnim_mjerama_119-24.pdf — checked 2026-11-09 (Arts. 1–5, 18, 60–61 read)
3. N1, "Serbia fails to align with four new EU foreign policy decisions", 29 July 2026, https://n1info.rs/english/news/serbia-fails-to-align-with-four-new-eu-foreign-policy-decisions/ — checked 2026-11-09
4. Montenegro, Zakon o sprečavanju pranja novca i finansiranja terorizma, consolidated text to Sl. list CG 59/26 (Central Bank copy), https://www.cbcg.me/slike_i_fajlovi/fajlovi/fajlovi_brzi_linkovi/propisi/zakoni/zakon_o_sprecavanju_pranja_novca_i_finansiranja_terorizma_prec_tekst_59-26.pdf — checked 2026-11-09 (Art. 4 read)
5. Crowell, "Deadlock broken: EU adopts 20th Russia sanctions package", https://www.crowell.com/en/insights/client-alerts/deadlock-broken-eu-adopts-20th-russia-sanctions-package ; DLA Piper, https://www.dlapiper.com/insights/publications/global-sanctions-alert/2026/20th-package-of-eu-sanctions-against-russia ; Morgan Lewis, https://www.morganlewis.com/pubs/2026/05/eu-adopts-20th-sanctions-package-against-russia-expands-anti-circumvention-efforts — checked 2026-11-09 (search summary)
6. Council Regulation (EU) 2026/759 of 30 March 2026 (Iran), https://eur-lex.europa.eu/eli/reg/2026/759/oj/eng — checked 2026-11-09
7. Sidley, "New EU Dual-Use Regulation enters into force", https://datamatters.sidley.com/2021/09/09/new-european-union-dual-use-regulation-enters-into-force/ ; European Commission, 2025 update of the EU control list, https://policy.trade.ec.europa.eu/news/2025-update-eu-control-list-dual-use-items-2025-09-08_en ; Cooley, https://www.cooley.com/news/insight/2025/2025-12-05-eu--issues-2025-update-to-dual-use-control-list — checked 2026-11-09 (search summary)
8. WilmerHale, "A new era of enforcement in UK sanctions" (June 2026), https://www.wilmerhale.com/en/insights/client-alerts/20260625-a-new-era-of-enforcement-in-uk-sanctions ; Steptoe on the Apple Distribution International settlement, https://www.steptoe.com/en/news-publications/international-compliance-blog/ofsi-makes-first-use-of-new-settlement-mechanism-in-apple-distribution-international-limited-enforcement-action.html — checked 2026-11-09 (search summary)
9. UK FCDO, The UK Sanctions List, https://www.gov.uk/government/publications/the-uk-sanctions-list — checked 2026-11-09
10. Brussels Times, non-EU countries align with EU Russia sanctions, https://www.brusselstimes.com/2391716/non-eu-countries-align-with-eu-sanctions-pile-up-pressure-on-russia-over-ukraine — checked 2026-11-09 (search summary)
11. Službeni list Crne Gore, Government decisions introducing international restrictive measures (examples), https://www.sluzbenilist.me/propisi/394681/download — checked 2026-11-09 (search summary; not read in full)
12. FAOLEX/UNEP record, Montenegro Law on Export Control of Dual-Use Goods, https://leap.unep.org/en/countries/me/national-legislation/law-export-control-dual-use-goods ; WTO QR notification Montenegro, https://qr.wto.org/en/qrs/6403 — checked 2026-11-09 (search summary)
13. bne IntelliNews, "Serbia says will not hinder NIS sale as Gazprom-MOL talks progress", https://www.intellinews.com/serbia-says-will-not-hinder-nis-sale-as-gazprom-mol-talks-progress-447529/ ; EUalive, US waiver for NIS, https://eualive.net/serbia-secures-another-u-s-sanctions-waiver-for-russian-owned-nis-oil-firm/ — checked 2026-11-09 (search summary)
14. RFE/RL, OFAC sanctions on Serbian and Montenegrin firms, 31 Oct 2024, https://www.rferl.org/a/ofac-sanctions-serbia-montenegro-russia/33182071.html ; RFE/RL investigation on Serbian dual-use exports, https://www.rferl.org/amp/serbia-russia-sanctions-dual-use-technology/32676159.html — checked 2026-11-09
15. European Commission, Data Act policy page, https://digital-strategy.ec.europa.eu/en/policies/data-act — checked 2026-11-09
