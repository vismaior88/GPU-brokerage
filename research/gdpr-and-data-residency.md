# GDPR, Montenegrin data protection, and supplier "data residency" claims
_Last checked: 2026-11-09_

Covers section 6 item 7. Not legal advice. Research note: web search capacity ran out before this topic was fully checked. Statute texts cited were read directly; commentary-level points from prior knowledge are marked **(unverified)**.

## Summary

- **You handle two very different kinds of data.** (a) Your own business data: buyer and supplier contact details and KYC documents. You are the *controller* of that. (b) The buyer's workload data on the GPUs. You never touch it; the **supplier is the processor** and the buyer is the controller. Keep it that way.
- **GDPR may apply to your US LLC even though you are outside the EU.** Article 3(2) covers non-EU businesses that offer goods or services to individuals in the EU [1]. Whether a purely business-to-business broker is "offering services to data subjects" is arguable; the safe and cheap course is to behave as if GDPR applies.
- **Article 27 representative:** required when Article 3(2) applies, unless processing is "occasional", involves no large-scale sensitive data and is low-risk [2]. The EDPB says "occasional" means not regular and outside your normal course of business [3]. Regular KYC on EU clients probably does not qualify as occasional. Decide with a lawyer once you have EU clients; it is not a month-one cost.
- **Montenegro has a new GDPR-style law.** It entered into force 19 September 2026 and applies from **19 March 2027**; fines rise from a €20,000 maximum to up to €2 million or 4% of turnover; it does not recognise EU adequacy decisions or EU standard contractual clauses until accession [4]. Because you work from Montenegro, this law probably applies to you more directly than GDPR does. Local advice needed before March 2027.
- **A US-owned supplier with an EU data centre is still reachable by US authorities.** Under 18 U.S.C. § 2713 (CLOUD Act) a provider must disclose data in its "possession, custody, or control" regardless of whether it is stored inside or outside the United States [5]. "EU data residency" (where the servers are) is not "sovereignty" (who can be compelled).
- **Never make residency or compliance promises in your own name.** Pass on the supplier's written statement, name the data-centre location and the owning group, and let the buyer contract directly with the supplier.
- **KYC data:** collect the minimum, store it encrypted, keep closed-deal and screening records 10 years (US sanctions record rule [6]), delete prospect data that goes nowhere after about 12 months.
- **Recommendation:** a short privacy notice on the website, a one-page data inventory, encrypted storage, a standard supplier residency questionnaire, and a clause in your buyer agreement saying you are not the processor of workload data. Cost: essentially zero.

## Details (section 6 item 7)

### 1. The broker's own position under GDPR

**What you process:** names, work emails, phone numbers and job titles of buyer and supplier staff; CRM notes; and for KYC: company documents, names and possibly ID details of directors and beneficial owners; screening results.

**Does GDPR apply to a US LLC run from Montenegro?**

| Test | Text | Applies to you? |
|---|---|---|
| Art. 3(1) establishment in the EU | Processing "in the context of the activities of an establishment … in the Union" [1] | No. Neither the US nor Montenegro is in the EU |
| Art. 3(2)(a) targeting | Non-EU controller processing data of people in the Union where activities relate to "offering goods or services" to them [1] | Possibly. You market to EU companies; the individuals whose data you hold are their staff and owners. Regulators have not been consistent on pure B2B cases **(unverified)**. Assume yes |
| Art. 3(2)(b) monitoring behaviour | Tracking individuals in the EU [1] | Only if you run tracking/analytics or scrape profiles. Keep website tracking minimal |

Reasons to simply comply regardless: EU enterprise buyers will ask for it in procurement; Montenegro's new law imposes nearly the same duties; the work is small.

**Minimum GDPR-style setup for a solo broker**

1. **Privacy notice** on your site and linked in the intake form: who you are, what you collect, why (quoting, contracting, sanctions/KYC checks), legal basis, who you share with (the suppliers you introduce, screening tools), retention, rights, contact email.
2. **Legal bases:** contract/pre-contract steps for quoting; *legitimate interests* for sanctions and KYC screening and for B2B outreach. Note: a US legal duty (OFAC) is not an "EU legal obligation" basis under GDPR, so rely on legitimate interests for screening **(interpretation; confirm with counsel)**.
3. **Data inventory** (one page): what data, where stored, who has access, retention period.
4. **Security:** encrypted cloud storage, password manager, two-factor authentication, no KYC documents in ordinary email threads where avoidable.
5. **Sharing with suppliers:** tell the buyer before you pass their details to a supplier; you and the supplier are each independent controllers of contact data.
6. **Cold outreach:** B2B email rules are national (ePrivacy) and differ by country **(unverified)**; always identify yourself and offer opt-out.
7. **Screening tools:** using a third-party screening API makes that vendor your processor; accept their data-processing terms.
8. **Breach plan:** if KYC files leak, GDPR expects notification to the regulator within 72 hours where there is risk **(from prior knowledge; unverified today)**.

**Article 27 EU representative.** Text: where Art. 3(2) applies the controller "shall designate in writing a representative in the Union", except for processing that is occasional, not large-scale sensitive data, and unlikely to result in risk [2]. EDPB Guidelines 3/2018: processing is "occasional" only if "not carried out regularly, and occurs outside the regular course of business"; appointing a representative does not shift your own liability [3]. Honest assessment: with a handful of EU contacts and no ID documents you are low-risk and low-priority for any regulator; once KYC on EU clients becomes routine, the exemption is hard to argue. Commercial representative services exist for small firms; prices were not checked **(unverified)**.

**International transfers.** An EU buyer sending staff/KYC data to you is a transfer out of the EU. Montenegro has no EU adequacy decision **(unverified)**; a US LLC is covered by the EU–US Data Privacy Framework only if it self-certifies **(unverified)**. In practice an EU customer may ask you to sign Standard Contractual Clauses. Sign them; they are standard.

### 2. Montenegro's data protection law

- New Law on Personal Data Protection: in force 19 Sept 2026, **applies from 19 March 2027** after a six-month transition (Legal 500 country note) [4]. A second source reports adoption by parliament on 4 Sept 2026 [7]. Official Gazette number not confirmed **(unverified)**.
- GDPR-like: extraterritorial reach to foreign businesses offering goods/services to people in Montenegro, with a local representative requirement; fines up to €2 million or 4% of worldwide turnover (serious breaches) and €1 million or 2% (others); current maximum is €20,000 [4].
- **Transfers out of Montenegro are awkward:** until EU accession the law does not recognise the EU's adequacy list or EU SCCs, and the regulator cannot issue its own clauses; other tools (regulator approval, derogations) must be used unless the Government issues its own adequacy decisions [4]. This matters to you because you sit in Montenegro and store data with US cloud tools.
- Until March 2027 the older law (2008, as amended) remains applicable [4][8]. Regulator: Agency for Personal Data Protection and Free Access to Information (AZLP) [8].
- **Does it apply to a US LLC?** If you run the LLC's business from Montenegro on a stable basis, the LLC may be treated as having an establishment there, bringing all its processing under Montenegrin law **(interpretation; confirm locally)**. This links to the branch/permanent-establishment question in `eu-uk-local-rules.md`.

### 3. Workload data: the supplier is the processor, not you

- The buyer decides what data goes on the GPUs (controller). The supplier hosts it (processor). GDPR Art. 28 requires a data-processing agreement (DPA) between *those two* **(from prior knowledge)**.
- You must stay out of that chain. Rules for yourself:
  - never hold buyer credentials, SSH keys, datasets or model weights;
  - never sign the DPA or the cloud contract on the buyer's behalf;
  - no admin access to the buyer's tenant "to help with setup";
  - state in your buyer agreement: "Broker does not host, access or process Customer workload data. Supplier is the provider and processor under Customer's direct agreement with Supplier."
- If you move to **reselling** (your contract, your invoice), you become a processor (and the supplier a sub-processor). That brings DPAs, security duties, transfer rules and liability. Another reason to delay reselling.

### 4. Handling "EU data residency" and "sovereign" claims

**Three different claims that sellers blur together**

| Claim | Means | Does not mean |
|---|---|---|
| "EU data residency" / "EU region" | Hardware and stored data are physically in an EU country | That non-EU staff cannot access it, or that foreign authorities cannot compel the provider |
| "GDPR compliant" | Provider offers a DPA and security measures | A certification; no official "GDPR compliant" stamp exists for clouds **(unverified today)** |
| "Sovereign" | Usually: EU-owned and EU-operated, outside non-EU jurisdiction | Anything precise. No single legal definition; national schemes (for example France's SecNumCloud) set their own tests **(unverified today)** |

**CLOUD Act exposure — verified from the statute.** 18 U.S.C. § 2713: a provider "shall comply with the obligations of this chapter to preserve, backup, or disclose" data "within such provider's possession, custody, or control, regardless of whether such communication, record, or other information is located within or outside of the United States" [5]. The US Department of Justice describes the Act as covering electronic evidence "wherever it happens to be located" [9]. So:
- a US-headquartered neocloud's Frankfurt or Paris region is EU-resident but not immune from US legal process;
- an EU-incorporated supplier with a US parent, or one that is itself subject to US jurisdiction, may be in the same position — this turns on control and is a legal question;
- an EU-owned supplier renting space in a third-party EU data centre is generally outside direct CLOUD Act reach, but may use US-owned sub-processors (support tools, monitoring, object storage).

**How to verify a location/sovereignty claim (supplier questionnaire)**

1. Exact data-centre address(es) and the name of the facility operator (colocation provider).
2. Legal entity that signs the contract; its ultimate parent and country; any US parent, US listing or US-based administrators.
3. List of sub-processors and where support/admin staff sit (remote access from outside the EU is a "transfer").
4. Where backups, logs, telemetry and billing data go.
5. Evidence: ISO 27001 or SOC 2 report whose *scope* names that site; any national certification claimed, with certificate number; the standard DPA.
6. A contract clause committing to the named location and to notice before any change.
7. Policy on government access requests (notify customer, challenge where lawful).
8. Sanctions/ownership screening of the operator (see `sanctions-and-screening.md`).

A network test (latency, traceroute, IP geolocation) is only a rough sanity check; it can be wrong and it says nothing about backups or ownership. A site visit or a colocation provider's confirmation letter is stronger evidence for large deals.

**What to promise and never promise**

| OK to say | Never say |
|---|---|
| "Supplier X states in writing that this capacity is in [facility, city, country]; statement attached." | "Your data will never leave the EU." |
| "Supplier X is owned by [group], headquartered in [country]." | "This supplier is immune to the CLOUD Act / US access." |
| "Supplier offers a DPA; your lawyer should review it." | "This setup is GDPR compliant" or "AI Act compliant". |
| "I have not independently audited the facility." | "Sovereign", "certified" or "guaranteed" in your own words, unless quoting a named certificate |
| "For health, financial or public-sector data, ask your DPO whether a US-owned provider is acceptable." | Any legal opinion on the buyer's transfer or sector obligations |

Put a disclaimer in the buyer agreement: location and compliance statements are the supplier's; the broker passes them on without warranty. Then make sure the supplier's own contract with the buyer repeats the location commitment, so the buyer has a remedy against the party that controls the hardware.

### 5. KYC data: a short retention approach

Two pressures pull in opposite directions: GDPR-style rules say keep as little as possible for as short as possible; US sanctions rules require records of transactions to be kept **10 years** [6], and the statute of limitations is also 10 years.

| Data | Keep | Why |
|---|---|---|
| Screening log (party, date, tool, result, decision) and saved search PDFs | 10 years from the deal or the refusal | Proof of diligence; OFAC record rule [6] |
| Closed-deal KYC file (company documents, ownership declaration, end-use statement, contracts, invoices) | 10 years after the relationship ends | Same |
| Refused deals | Short refusal note + screening evidence: 10 years. Delete other documents | Shows why you declined; minimises data |
| Prospects that never progressed | Contact data up to 12 months after last contact, then delete; delete any KYC documents at once | No ongoing purpose |
| Passport/ID copies | Avoid collecting if a registry extract and signed declaration are enough. If collected, encrypt; same period as the deal file | Highest harm if leaked |
| Marketing contacts | Until opt-out, review every 24 months | |

State these periods in the privacy notice. Whether a 10-year period based on US law is acceptable under GDPR and Montenegrin law for EU/Montenegrin individuals should be confirmed (legitimate interests / defence of legal claims is the usual justification) **(unverified)**.

## Questions for a lawyer / accountant

1. Does GDPR Art. 3(2) apply to my B2B brokerage, and do I need an Art. 27 representative once I run KYC on EU clients regularly?
2. Is my US LLC "established" in Montenegro for the new data protection law, and what must be done before 19 March 2027 (registration, representative, records)?
3. How can I lawfully store KYC data from Montenegro on US-hosted tools, given the new law's transfer rules?
4. Is a 10-year retention period for KYC and screening records defensible under GDPR and Montenegrin law?
5. Wording of the "not a processor / no warranty on supplier location claims" clauses in the buyer agreement.
6. When an EU supplier has a US parent, how should I describe CLOUD Act exposure to buyers without giving legal advice?

## Sources

1. GDPR Article 3 (territorial scope), https://gdpr-info.eu/art-3-gdpr/ — checked 2026-11-09
2. GDPR Article 27 (representatives), https://gdpr-info.eu/art-27-gdpr/ — checked 2026-11-09
3. EDPB Guidelines 3/2018 on the territorial scope of the GDPR (final, 12 Nov 2019), https://www.edpb.europa.eu/sites/default/files/files/file1/edpb_guidelines_3_2018_territorial_scope_after_public_consultation_en_1.pdf — checked 2026-11-09 (section on Art. 27 read)
4. Legal 500, "GDPR comes to Montenegro: is your business ready?", https://www.legal500.com/intelligence/montenegro/privacy/gdpr-comes-to-montenegro-is-your-business-ready — checked 2026-11-09
5. 18 U.S.C. § 2713 (CLOUD Act), https://www.law.cornell.edu/uscode/text/18/2713 — checked 2026-11-09
6. Federal Register, OFAC Reporting, Procedures and Penalties Regulations (10-year recordkeeping), 21 Mar 2025, https://www.govinfo.gov/content/pkg/FR-2025-03-21/html/2025-04864.htm — checked 2026-11-09 (search summary)
7. PPC Land, "Firms face up to 4% turnover fines under Montenegro's new data law", https://ppc.land/firms-face-up-to-4-turnover-fines-under-montenegros-new-data-law/ — checked 2026-11-09 (search summary)
8. CMS Expert Guide to data protection laws – Montenegro, https://cms.law/en/int/expert-guides/cms-expert-guide-to-data-protection-and-cyber-security-laws/montenegro — checked 2026-11-09 (search summary; partly out of date)
9. US Department of Justice, CLOUD Act resources, https://www.justice.gov/criminal/cloud-act-resources — checked 2026-11-09
