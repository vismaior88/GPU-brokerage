# Tax, VAT and entity structure notes (Q26, Q27, Q29)
_Last checked: 2026-11-09_

> This is research, not tax advice. Every conclusion below must be confirmed by a US accountant who works with non-resident-owned LLCs and by a Montenegrin accountant before you rely on it. Items I could not confirm from a primary or Big-4 source are marked **(unverified)**.

## Summary

- **The US filing you cannot skip:** a foreign-owned single-member LLC must file Form 5472 attached to a pro-forma Form 1120 every year it has a "reportable transaction" with its owner (money in, money out, expenses paid personally). Penalty for missing or incomplete filing: **$25,000**. It is filed by fax or mail, not online [1]. If the LLC already existed in earlier years, check now whether those years were filed.
- **US income tax is probably zero, but only if the facts stay clean.** Services are taxed where they are performed. Commissions earned by work you do from Montenegro are foreign-source and generally not US-taxable, as long as you have no US office, no US-based staff or dependent agents, and you do not work while physically in the US [4][5][6]. An accountant must confirm this for your actual facts.
- **There is no US–Montenegro income tax treaty** (checked on the IRS treaty list and on PwC's Montenegro treaty list) [2][3]. So there is no treaty safety net: the stricter US domestic rules apply, and Montenegro gives no treaty relief either.
- **"US LLC = no tax" is false for you.** Montenegro taxes its residents on worldwide income [7]. A foreign company with its place of effective management in Montenegro can itself be a Montenegrin tax resident and owe corporate tax at 9–15% [8][9]. A US LLC run entirely by one person in Montenegro fits that description. This is the single biggest open question; it needs a Montenegrin accountant before the first commission arrives.
- **BOI/CTA reporting: not required.** FinCEN's final rule (issued 11 Aug 2026, effective 14 Aug 2026) permanently exempts US-formed companies from beneficial ownership reporting [10][11]. Ignore "file your BOI" mailings.
- **W-8 forms:** US suppliers will ask for one. For a disregarded LLC, the **owner** gives a **Form W-8BEN** in their own name and mentions the LLC on line 7. Not a W-8BEN-E, not a W-9 [12][13].
- **VAT:** B2B services to EU business customers are normally taxed where the customer is, and the customer self-accounts under reverse charge. You do not charge EU VAT on B2B invoices [14]. US sales tax rarely reaches B2B brokerage services **(unverified at state level)**. Montenegro's VAT registration threshold is EUR 30,000 of turnover in 12 months [15]; whether your LLC's turnover counts toward it is a question for the Montenegrin accountant.
- **Structure (Q29):** keep the existing US LLC for now and form nothing new. Spend the money on one Montenegrin tax consultation and the annual 5472 filing. Revisit a Montenegrin d.o.o. when revenue is real (roughly EUR 30k+/year) or if the accountant says the LLC must be registered in Montenegro anyway.

## Details

### Q26 — US side

**1. Form 5472 + pro-forma Form 1120** [1]

| Item | What the IRS instructions say |
|---|---|
| Who | A US disregarded entity (single-member LLC) wholly owned by one foreign person |
| What | Form 5472 attached to a pro-forma Form 1120. On the 1120 only name, address and items B and E are filled in; write "Foreign-owned U.S. DE" across the top |
| When | By the Form 1120 due date including extensions. For a calendar-year filer that is normally 15 April; extension via Form 7004 (confirm the exact date with the accountant) |
| How | Fax to 855-887-7737 or mail to the IRS in Ogden, UT. E-filing is not allowed for these filers |
| Penalty | $25,000 for failing to file on time or filing a substantially incomplete form; a further $25,000 per 30 days if not fixed within 90 days of an IRS notice |
| Records | You must keep books and records that support the form (same penalty for not keeping them) |
| Tax ID | The LLC needs an EIN; the form also asks for your foreign tax ID |

"Reportable transactions" for a foreign-owned LLC are wider than normal: they include any money or value moving between you and the LLC — capital contributions, distributions to you, formation costs you paid, expenses you paid personally for the LLC, loans [1]. Putting $500 into the LLC bank account is reportable. In practice almost every active LLC must file every year. Whether a year with literally zero owner–LLC transactions still needs a filing is a question for the accountant.

**Action:** if the LLC existed in 2025 or earlier and no 5472 was filed, tell the accountant immediately. Late filings with a "reasonable cause" statement are a known procedure, and it is much better to fix it voluntarily than after an IRS notice.

**2. EIN.** The EIN is free. Applicants whose principal place of business is outside the US cannot use the online tool and must apply by phone, fax or mail [16]. Banks and Form 5472 both need it.

**3. Is the commission income US-taxable?**

Because the LLC is disregarded, the IRS looks through it to you, a non-resident individual. A non-resident pays US income tax on business income only if it is "effectively connected" with a US trade or business (ETBUS) [4].

- **Source rule:** pay for services is sourced where the services are performed. Work done outside the US is foreign-source (Internal Revenue Code §§861(a)(3), 862(a)(3)) [5].
- **Foreign-source income is generally not effectively connected.** The exception requires an office or fixed place of business in the US to which the income is attributable, and applies only to limited categories of income [6]. An accountant must confirm that referral/brokerage commissions fall outside those categories.
- **Agents:** the office of an agent is ignored unless the agent has, and regularly uses, authority to conclude contracts in your name and is not an independent agent [6].

What keeps you on the safe side (to confirm):

| Keep it this way | Why |
|---|---|
| All work done physically outside the US | Performing services in the US is itself a US trade or business [4][6] |
| No US office, co-working desk or employee | A US fixed place of business is the main trigger [6] |
| No US-based person who signs deals for you | Dependent-agent rule [6] |
| Registered agent / mail address only | Generally not treated as an office **(unverified — ask)** |
| You refer; the supplier contracts directly with the buyer | You are not selling US-located goods or holding inventory |

Risks to raise with the accountant: (a) trips to the US for conferences where you negotiate deals; (b) hiring a US-based sub-agent later; (c) whether a supplier might treat your commission as US-source and withhold 30%.

**4. No treaty.** Montenegro is not on the IRS list of treaty countries [2] and the US is not among Montenegro's 47 treaty partners [3]. Consequences: no treaty "permanent establishment" protection (the lower US domestic ETBUS threshold applies); no reduced withholding rates; no tie-breaker rules; if both countries ever taxed the same income you would rely only on Montenegro's domestic foreign tax credit [17].

**5. W-8 forms** [12][13]

- A disregarded entity does not give its own W-8. The single foreign owner gives the form. You are an individual, so you give **Form W-8BEN** in your own name, with your Montenegrin address and tax number, and put the LLC's name on line 7.
- **W-8BEN-E** is for foreign *entities*; it would apply only if the LLC elected to be taxed as a corporation or the owner were a company.
- **W-8ECI** is only for income that *is* effectively connected with a US business. Signing it means you are saying you owe US tax and must file a US return. Do not sign it just because a supplier's form asks for "a W-8".
- **W-9** is for US persons. A foreign-owned disregarded LLC should not sign one, even though it has an EIN.
- A W-8BEN is generally valid until the end of the third calendar year after signing.
- Without a treaty you claim no reduced rate; the form only documents that you are foreign. Whether the payment is then free of withholding depends on it being foreign-source services income — have the accountant give you one paragraph you can send to supplier finance teams.

**6. State level.** Depends on the state of formation (not stated in your brief):

| State | Annual obligation | Source quality |
|---|---|---|
| Delaware | $400 annual LLC tax, due 1 June, $200 penalty + 1.5%/month if late; no annual report | Official state page [18]. Many third-party sites still say $300 — check your invoice |
| Wyoming | Annual report with about $60 minimum licence tax, due in the anniversary month | Third-party only **(unverified)** [19] |
| New Mexico | No annual report or franchise tax | Third-party only **(unverified)** [19] |

Every state also requires a registered agent (a yearly fee). State income tax and sales tax normally need activity in the state; with no US operations this is usually nil **(unverified — confirm for your state)**.

**7. FinCEN beneficial ownership (BOI / Corporate Transparency Act).** The March 2025 interim rule exempted US-formed companies. FinCEN made this permanent in a final rule issued 11 August 2026, effective 14 August 2026. Reporting now applies only to certain foreign-formed companies registered to do business in the US [10][11]. The statute itself was not repealed, so this could change under a future administration; have the accountant re-check yearly. Your bank will still collect beneficial-owner details under its own KYC rules.

### Q26 — Montenegro side

What is confirmed (PwC Worldwide Tax Summaries, reviewed 7 Aug 2026):

| Topic | Rule |
|---|---|
| Residents | Taxed on worldwide income [7] |
| Self-employment / business income | 0% to EUR 8,400; 9% from EUR 8,400.01 to 12,000; 15% above (annual) [7] |
| Dividends and profit shares | 15% on the gross amount [20] |
| Municipal surtax | 13% of the income tax due (15% in Podgorica and Cetinje) [7] |
| Corporate tax | 9% to EUR 100,000 profit; 12% to EUR 1.5m; 15% above [8] |
| Company residence | Incorporated in Montenegro, **or** foreign company with place of effective management in Montenegro [9] |
| Permanent establishment | Fixed place of business of a non-resident; includes a "place of management" and an office [9] |
| CFC rules | None [21] |
| Foreign tax relief | Credit for foreign tax, capped at the Montenegrin tax [17] |
| Social contributions | Pension 10% (employee), unemployment 0.5% + 0.5% on salaries; contributions also apply to other personal income but PwC gives no rates for the self-employed [22] |

What is **not** confirmed and decides everything: how the Montenegrin tax administration classifies a US single-member LLC. Montenegro has no US-style "disregarded entity" concept that I could find **(unverified)**. Three possible outcomes:

1. **LLC treated as a foreign company managed from Montenegro** → the LLC is a Montenegrin tax resident (or has a PE here). It would need to register, keep Montenegrin-standard books and pay 9% corporate tax on profit; you then pay 15% (plus surtax) when you take profit out. Rough combined burden on distributed profit: about 23–25% (my arithmetic from the rates above).
2. **Income treated as your own business/self-employment income** → 0/9/15% bands plus surtax plus social contributions; you may need to register as an entrepreneur (preduzetnik).
3. **Taxed only when distributed, as a foreign dividend at 15%** → the outcome people hope for, but it sits badly with the effective-management rule above. Do not assume it.

In all three, Montenegro taxes the money. Because the US charges no income tax (if section 3 holds), there is no foreign tax to credit. The absence of CFC rules does not help: the effective-management and PE rules already reach a one-person company run from your home.

Not declaring is the real risk. Montenegro is in EU accession talks and is aligning its tax rules with the EU; bank information exchange is expanding. Assume the LLC is visible.

**Comparison: just using a Montenegrin d.o.o.** Corporate tax 9% on the first EUR 100,000 [8], dividends 15% [20], minimum capital EUR 1 (multiple vendor sources) [23]. Vendor estimates: bookkeeping about EUR 100–250/month, first-year all-in EUR 600–4,500 depending on provider; one vendor says a founder-director must take at least a minimum salary with monthly contributions **(all unverified vendor figures)** [23]. The d.o.o. gives a clear, defensible local tax position; the cost is monthly accounting that would consume most of a $2,000 budget.

**Recommendation (Q26):** before the first commission, pay for one consultation with a Montenegrin accountant on the classification question, and engage a low-cost US preparer for the 5472. Do not rely on formation-agent marketing that says the LLC is tax-free.

### Q27 — VAT and sales tax

**EU business customers (B2B).** For services sold to a business in the EU, VAT is normally due in the customer's country and the customer accounts for it under reverse charge; the supplier does not charge VAT [14]. EU businesses buying from a non-EU supplier likewise self-account [14]. Practical steps: collect and check the customer's VAT number (EU VIES tool), put it on the invoice, add "Reverse charge — VAT to be accounted for by the recipient", and charge no VAT. You do not need an EU VAT registration for this. There are exceptions for some service types [14]; a plain broker fee or referral commission billed to a business should follow the general rule **(confirm)**. The detailed rules are on the Commission's place-of-supply page [24] (page was rate-limited today; not re-read).

- Commissions paid to you **by a US or other non-EU supplier**: no EU VAT.
- **Consumers (B2C):** different rules, possible registration duties. Sell to businesses only.
- **UK and other non-EU customers:** similar reverse-charge logic is common **(unverified)**.

**US sales tax.** There is no federal sales tax or VAT. State sales taxes mostly target goods; B2B brokerage/referral services are generally not taxed, though a few states tax services broadly, and a state can only require collection if you have nexus there (physical presence or sales above its threshold) **(unverified — I could not complete this check today; ask the US accountant, especially if the LLC is formed in New Mexico, which has a gross receipts tax)**.

**Montenegro VAT.** Standard rate 21%; registration is mandatory once turnover exceeds EUR 30,000 in the last 12 months; once registered you cannot deregister for three years [15]. The VAT law was amended in February 2026 (Official Gazette 012/26): place-of-supply rules were reorganised without substantive change and are described as aligned with the EU VAT Directive; reverse charge applies and must be stated on the invoice where the place of supply is outside Montenegro; non-resident suppliers of B2C services taxable in Montenegro must register a PE or appoint a VAT representative [25][26]. A new VAT law adopted in July 2026 reportedly applies only from EU accession **(unverified)**.

What this means for you (all to confirm locally):
- If the LLC is treated as managed from Montenegro, its supplies may be treated as made from Montenegro. B2B services to foreign businesses should then have their place of supply abroad (no Montenegrin VAT charged), but ask whether that turnover still counts toward the EUR 30,000 threshold.
- A Montenegrin business customer buying from the US LLC would normally self-account under reverse charge.
- Services you buy from abroad (software, data tools) can create reverse-charge duties once you are a Montenegrin VAT payer.

**Recommendation (Q27):** B2B only; collect VAT numbers; no VAT on EU B2B invoices with the reverse-charge note; ask the Montenegrin accountant the threshold question in the same consultation as the classification question.

### Q29 — Stay in the US LLC or change structure?

| Option | Pros | Cons | Rough cost | Verdict now |
|---|---|---|---|---|
| **Keep US LLC only** | Already exists; US suppliers and partner programmes know how to onboard a US entity; USD banking; likely no US income tax | Montenegrin position unclear (effective management / PE); annual 5472 with $25k penalty risk; no treaty; banks can drop non-resident accounts | 5472 filing about $300–1,500/yr [see questions-for-accountant.md]; state fee; registered agent | **Keep, but get the Montenegro answer first** |
| **Montenegrin d.o.o. only** | Clear local position; 9% corporate tax; SEPA banking since Oct 2025; 47 tax treaties (not with US) [3] | Monthly bookkeeping; possible director salary/contributions **(unverified)**; VAT admin; some US suppliers may be slower to onboard a Montenegrin company; LLC must be closed properly | Vendor estimates EUR 100–250/month **(unverified)** [23] | Likely the long-term home if revenue is steady; too costly before revenue |
| **Estonian OÜ (e-Residency)** | EU entity; 0% tax on retained profit, 22% on distribution [27]; trusted by EU customers | Same effective-management problem in Montenegro (run from your home); no Estonia–Montenegro treaty on PwC's list [3]; Estonia itself has no management test, so no help there [28]; another country's compliance | Typically over EUR 1,000/yr with a service provider **(unverified)** | **Not recommended**: adds cost without solving the Montenegro question |
| **Both: US LLC + d.o.o.** | US face for suppliers, local entity for substance | Double accounting; transfer-pricing rules apply between related parties [21]; pointless at small scale | Sum of both | Only if a supplier contract truly requires a US entity and revenue justifies it |

**Recommendation (Q29):** stay in the US LLC for the first six months. Do not form anything new on a sub-$2k budget. Decision points to revisit: (1) the Montenegrin accountant says the LLC must register here anyway — then compare the cost with simply moving to a d.o.o.; (2) revenue approaches EUR 30,000/year; (3) a bank or key supplier refuses the non-resident LLC; (4) you hire anyone.

## Questions for a lawyer / accountant

See `finance/questions-for-accountant.md` for the full prioritised list. The three that cannot wait:
1. Montenegro: how is my US single-member LLC classified, and what must I register and declare?
2. US: were all past Form 5472s filed; if not, how do we fix it?
3. US: confirm in writing that my commissions are foreign-source and not effectively connected income, and that W-8BEN is the right form.

## Sources

1. IRS, Instructions for Form 5472 (Rev. 12/2024; page updated 30 Apr 2026) — https://www.irs.gov/instructions/i5472 — checked 2026-11-09
2. IRS, United States income tax treaties A to Z (updated 3 Jan 2026) — https://www.irs.gov/businesses/international-businesses/united-states-income-tax-treaties-a-to-z — checked 2026-11-09
3. PwC Worldwide Tax Summaries, Montenegro – Corporate – Withholding taxes (treaty list) — https://taxsummaries.pwc.com/montenegro/corporate/withholding-taxes — checked 2026-11-09
4. IRS, Effectively connected income (ECI) (updated 18 Aug 2026) — https://www.irs.gov/individuals/international-taxpayers/effectively-connected-income-eci — checked 2026-11-09
5. 26 U.S. Code §861 (and §862), source rules — https://www.law.cornell.edu/uscode/text/26/861- — seen in search results 2026-11-09; statute text not read in full
6. 26 U.S. Code §864 (trade or business; foreign-source income; office of an agent) — https://www.law.cornell.edu/uscode/text/26/864 — checked 2026-11-09
7. PwC, Montenegro – Individual – Taxes on personal income (reviewed 7 Aug 2026) — https://taxsummaries.pwc.com/montenegro/individual/taxes-on-personal-income — checked 2026-11-09
8. PwC, Montenegro – Corporate – Taxes on corporate income (reviewed 7 Aug 2026) — https://taxsummaries.pwc.com/montenegro/corporate/taxes-on-corporate-income — checked 2026-11-09
9. PwC, Montenegro – Corporate – Corporate residence — https://taxsummaries.pwc.com/montenegro/corporate/corporate-residence — checked 2026-11-09
10. Morrison Foerster, "FinCEN Ends Beneficial Ownership Reporting Requirements for U.S. Companies" (Aug 2026) — https://www.mofo.com/resources/insights/260820-fincen-ends-beneficial-ownership-reporting — search summary checked 2026-11-09
11. Ballard Spahr, "FinCEN permanently exempts US entities and persons from beneficial ownership reporting" (Aug 2026) — https://www.ballardspahr.com/insights/alerts-and-articles/2026/08/fincen-permanently-exempts-us-entities-and-persons-from-beneficial-ownership-reporting — search summary checked 2026-11-09 (FinCEN's own notice not read directly)
12. IRS, Instructions for Form W-8BEN (Rev. 10/2021) — https://www.irs.gov/instructions/iw8ben — checked 2026-11-09
13. IRS, Instructions for Form W-8BEN-E (Rev. 10/2021) — https://www.irs.gov/instructions/iw8bene — checked 2026-11-09
14. European Union, Your Europe – Cross-border VAT — https://europa.eu/youreurope/business/taxation/vat/cross-border-vat/index_en.htm — checked 2026-11-09
15. PwC, Montenegro – Corporate – Other taxes (VAT) — https://taxsummaries.pwc.com/montenegro/corporate/other-taxes — checked 2026-11-09
16. IRS, Get an employer identification number — https://www.irs.gov/businesses/small-businesses-self-employed/get-an-employer-identification-number — checked 2026-11-09
17. PwC, Montenegro – Individual – Foreign tax relief and tax treaties — https://taxsummaries.pwc.com/montenegro/individual/foreign-tax-relief-and-tax-treaties — checked 2026-11-09
18. Delaware Division of Corporations, LLC/LP/GP franchise tax instructions — https://corp.delaware.gov/alt-entitytaxinstructions/ — checked 2026-11-09
19. LLC University, LLC annual fees by state (third-party) — https://www.llcuniversity.com/llc-annual-fees-by-state/ — search summary checked 2026-11-09
20. PwC, Montenegro – Individual – Income determination — https://taxsummaries.pwc.com/montenegro/individual/income-determination — checked 2026-11-09
21. PwC, Montenegro – Corporate – Group taxation (CFC, transfer pricing) — https://taxsummaries.pwc.com/montenegro/corporate/group-taxation — checked 2026-11-09
22. PwC, Montenegro – Individual – Other taxes (social contributions) — https://taxsummaries.pwc.com/montenegro/individual/other-taxes — checked 2026-11-09
23. Vendor pages on Montenegrin company costs (marketing; unverified): https://adriacom.me/pricing-company-formation-montenegro/ and https://www.healyconsultants.com/montenegro-company-registration/setup-llc/ — search summaries checked 2026-11-09
24. European Commission, Place of taxation – services — https://taxation-customs.ec.europa.eu/taxation/vat/vat-directive/place-taxation/place-taxation-services_en — could not be loaded 2026-11-09 (rate-limited)
25. KPMG Montenegro, Tax Alert: Amendments to the VAT Law in Montenegro (March 2026) — https://assets.kpmg.com/content/dam/kpmgsites/me/pdf/2026/03/KPMG-Tax-Alert-Amendments-to-the-VAT-Law-in-Montenegro-March-2026.pdf.coredownload.inline.pdf — checked 2026-11-09
26. BDK Advokati, "Montenegro further harmonizes its VAT regime with EU VAT Directive" — https://bdkadvokati.com/montenegro-further-harmonizes-its-vat-regime-with-eu-vat-directive — checked 2026-11-09
27. EY, "Estonia abolishes temporary defense tax, increases several tax rates" (Jul 2025) and later reports that the rise to 24% was cancelled in Dec 2025 — https://taxnews.ey.com/news/2025-1409-estonia-abolishes-temporary-defense-tax-increases-several-tax-rates — search summary checked 2026-11-09; confirm the 22% rate
28. PwC, Estonia – Corporate – Corporate residence — https://taxsummaries.pwc.com/estonia/corporate/corporate-residence — checked 2026-11-09
