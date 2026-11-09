# Legal and contracts: referral agreements, bypass protection, liability, licensing (Q17, Q18, Q20, Q21)
_Last checked: 2026-11-09_

> **Not legal advice.** This is research to prepare you for a conversation with a qualified US lawyer (and a Montenegro lawyer where flagged). Points that need professional confirmation are marked **[LAWYER]**. Q19 (buyer agreement) is in `/legal/buyer-service-agreement-outline.md`.

## Summary

- **Supplier "partner terms" are written for the supplier, not for you.** Public examples show: non-exclusive, no authority to bind, commissions limited to a short period (often 6 months) or the first transaction, unilateral right to change terms, clawbacks, and little or nothing paid after termination [1][2][3][4].
- **The most dangerous clause for your "combined" model is a ban on being paid by the customer.** DigitalOcean's affiliate agreement removes the commission if the customer "has paid or will pay" you [1]. Check every supplier's terms for this before charging a buyer anything on the same deal.
- **Self-serve affiliate programs are not a brokerage business.** RunPod pays credits (cash only after 25 paying referrals) for 6 months [3]; Thunder pays non-cashable credits [5]; Hyperbolic pays 1% for 6 months [4]. Real income needs negotiated referral agreements on dedicated/reserved deals (ICS, Nebius, Cirrascale style [6][7][8]).
- **Non-circumvention clauses (NCNDAs) are weak protection for you.** US courts have gone both ways [19], and you cannot afford to sue anyone. Treat them as a deterrent and a paper trail, not a shield. What actually protects you: the supplier's written deal-registration confirmation, a signed referral agreement, a buyer engagement letter, and remaining useful after the introduction.
- **As a pure introducer you carry little contractual liability if a supplier fails, provided** you are not a party to the compute contract, you promise nothing about supplier performance, and you do not misdescribe anything. Disclaimers and a liability cap help with that.
- **Some liability cannot be disclaimed:** your own export-control or sanctions violations [20][21], fraud or misrepresentation, and taking an undisclosed commission while acting for the buyer [15][16].
- **No US licence specific to "compute brokerage" was found.** It does not look like a securities, commodities or money-transmission activity **as long as you (a) never hold or pass on customer money and (b) stay away from compute futures/derivatives** [10][11][14]. **[LAWYER]** to confirm.
- **Touching compute futures changes everything.** Soliciting or accepting orders for futures for compensation is "introducing broker" activity requiring CFTC registration and NFA membership [10][11]. Do not do it, and do not advise on hedging for a fee.
- **Disclose commissions in writing, always.** Secret commissions are a civil problem (you can lose the fee) and can be a crime under state commercial-bribery laws [15][16]. Disclosure plus the buyer's written consent is the cure.
- **Insurance:** small-firm tech E&O with a $1M limit is quoted at roughly $800–1,300 per year on US broker sites [18]. Whether a non-resident-owned LLC doing brokerage can get that price is **unverified**. It would take most of your budget; buy it when a deal or a counterparty requires it.

## Details

### Q17. What a referral agreement contains, and the clauses to watch

**What real programs say.** I could read the full legal text of only two cloud partner documents (DigitalOcean's). For GPU-specific clouds the public pages give commercial headlines only; the actual agreement is sent after you apply. Crusoe, Lambda and Vultr publish no agreement text that I could find [9][24] (Vultr: third-party listings only, **unverified**).

| Program | What is public | Source |
|---|---|---|
| DigitalOcean Affiliate Agreement (1 Jan 2025) | Non-exclusive; no agency; commission on the **initial** transaction only; lead must not have been in an active sales process in the prior 60 days; commission lost if the customer pays you; clawback of "fraudulent, questionable, or canceled" transactions, with the right to invoice you; 15 days' termination; commissions only for transactions within 30 days after termination, and none if you terminate without cause or they terminate for cause; terms can change with effect the next business day; their liability capped at 12 months of your commissions; New York law, AAA arbitration in Manhattan; you must comply with export and OFAC rules and state that you are an affiliate | [1] |
| DigitalOcean Partner Terms (May 2024) | Non-exclusive; "neither party ... is an agent of the other"; amounts and timing in a separate Program Guide; may withhold payment while you are in breach; DO may terminate on 30 days, partner on 90; their liability capped at one month of amounts paid; export/sanctions reps | [2] |
| RunPod | Referral: 3% (Pods) / 5% (Serverless) in **credits**, first 6 months. Affiliate: 10% cash for 6 months, only after 25 paying referrals, via PartnerStack; opt-in is permanent. New accounts only | [3] |
| Hyperbolic | 1% of actual revenue, first 6 months only, renewals excluded; customer must sign within 180 days of referral; not an existing customer or in active talks; paid quarterly | [4] |
| Thunder Compute | 3% lifetime, credits only, cannot be cashed out; program may change or end | [5] |
| Nebius | Search results quote the referral page as: commission applies to customer agreements of at least 64 GPUs, possibly higher above 512. The page I fetched today shows a general partner programme with "customized terms" and no figures — **partly unverified** | [6] |
| Ingenuity Cloud Services | 8% month-to-month / 10% on 12+ months (own and select partner data centres); 4% / 5% in partner data centres; requires a signed Referral Agreement, onboarding and use of a Deal Registration Process; "evergreen" commission mentioned. From search snippets of the ICS pages; the brochure link returned 404 today — **partly unverified** | [7] |
| Cirrascale | Non-exclusive, worldwide, monthly recurring commission on multi-GPU dedicated servers; rate not published. Page could not be opened from this session — **from search snippet only** | [8] |

**Clause checklist.** A full clause-by-clause negotiating outline is in `/legal/referral-agreement-outline.md`. The clauses that decide whether the agreement is worth signing:

| Clause | Why it matters | What to look for |
|---|---|---|
| Commission base and rate | "Revenue" can mean invoiced, collected, or net of credits/discounts/taxes | Net **collected** revenue is normal; make sure credits and discounts are defined |
| Tail (duration) | 6 months is common in public programmes [3][4]; GPU contracts run 12–36 months | Commission for the full initial term **plus renewals and expansions**, or at least 24 months |
| Renewals / expansions | Hyperbolic excludes renewals [4]; DO affiliate pays the first transaction only [1] | Explicit inclusion |
| Deal registration and expiry | Defines whether the customer is "yours"; Hyperbolic gives 180 days to close [4]; DO excludes leads in an active sales process in the prior 60 days [1] | Written acceptance or rejection within a few business days; 6–12 months protection; extension while talks are active |
| Clawback | DO can deduct and even invoice you [1] | Limit to refunds/chargebacks/fraud, limited look-back, set-off only (no invoice) |
| Ban on charging the customer | DO affiliate forfeits commission if the customer pays you [1] | Must be absent or carved out for disclosed advisory fees — otherwise the combined model breaches the agreement |
| Agency / authority | Standard: independent contractor, no authority to bind [1][2] | Accept it. It protects you too (you are not the provider) |
| Exclusivity / non-compete | Public programmes are non-exclusive [1][2][8] | Never accept exclusivity; it destroys the value of a broker |
| Termination and post-termination commission | DO pays almost nothing after termination [1] | Commissions on registered deals survive termination, except for your material breach |
| Unilateral changes | DO: effective next business day [1]; Thunder may discontinue [5] | Changes must not reduce commission on already-registered deals |
| Payout threshold, timing, currency | Quarterly at Hyperbolic [4]; credits vs cash [3][5] | Cash, monthly or quarterly, low or no threshold, wire to US LLC |
| Reporting / audit rights | Absent from DO documents [1][2] | At minimum a statement per customer per period; audit right is a nice-to-have you will rarely get |
| Compliance reps | Export/OFAC compliance is standard [1][2] | Accept; keep them accurate. Make sure responsibility for customer KYC/export screening stays with the supplier as provider, in addition to your own screening |
| Liability cap / indemnity | Caps run in the supplier's favour [1][2] | Your liability capped at commissions received; no uncapped indemnity for customer behaviour |
| Marketing rules | Brand-keyword bidding bans, no "incentives" [1] | Check a commission pass-back to the buyer is not a banned "incentive" |
| Governing law / disputes | NY law and arbitration in the supplier's city [1][2] | You will not change this; just know the cost of enforcing is beyond your budget |

**Recommendation (Q17):** apply to self-serve programmes only as a learning step. For every real supplier ask for the full referral agreement before introducing anyone, and run it through the checklist. The three points to fight for are: (1) tail covering the full contract term including renewals, (2) written deal-registration confirmation with at least 6 months' protection, (3) commissions on registered deals surviving termination. Refuse exclusivity outright.

### Q18. Protection from being bypassed

**Blunt answer: with under $2,000 you cannot enforce anything in court, in any country.** A single lawyer's demand letter costs a few hundred dollars; litigation or arbitration costs tens of thousands (general knowledge, **unverified** figures). Every protection must therefore work without a lawsuit.

**How enforceable are NCNDA clauses?**
- In the US they are ordinary contract terms, not automatically invalid. A Delaware court enforced one for an intermediary and awarded damages based on lost opportunity (*Cura Financial Services v. Electronic Payment Exchange*, Del. Ch. 2001); a Georgia court struck one down as an unreasonable restrictive covenant (*Swartz Investments v. Vion Pharmaceuticals*, Ga. Ct. App. 2001) [19]. Both known to me only from third-party summaries — **[LAWYER] verify**.
- Things that reportedly make them fail: vague definition of the protected contacts, excessive duration, no carve-out for existing relationships, no consideration, and no provable loss [19]. The "ICC NCNDA" templates circulating online are widely associated with scam commodity deals; using one signals inexperience to a serious GPU cloud (my assessment).
- Internationally: a court judgment from one country is hard to enforce in another. An **arbitration award** is easier because of the New York Convention, to which Montenegro is a party [22] and the US also is. That only helps a party that can pay for arbitration. You cannot.
- Large suppliers will simply not sign your NCNDA. They will tell you to use their deal-registration process.

**What actually protects you (in order of real-world value):**
1. **Supplier's written deal-registration confirmation** ("Customer X registered to Partner Y until date Z") under a signed referral agreement. This is the supplier's own process, so their finance team honours it.
2. **Register before you reveal.** Give the supplier the workload profile first; give the buyer's name only in the registration email, and ask for a written accept/reject.
3. **Buyer engagement letter** in which the buyer acknowledges you introduced the named suppliers and agrees to tell the supplier you are the partner of record.
4. **A complete email trail** (dates, names, who introduced whom). Keep everything in writing.
5. **Stay in the deal.** Brokers get cut out when their only value was a name. Keep doing work the two parties want: comparisons, renewals, expansion sourcing, issue escalation.
6. **Work with suppliers who value channel reputation** and have a formal programme. Avoid one-off arrangements with unknown resellers.
7. **Several suppliers per buyer need**, so that losing one relationship does not lose the deal.
8. **Accept some leakage.** Treat a bypass as a cost of doing business, stop working with that party, and move on.

**Recommendation (Q18):** use a short mutual NDA with a narrow non-circumvention clause (outline in `/legal/nda-and-non-circumvention-outline.md`) with small suppliers and buyers, but rely on deal registration and usefulness. Never spend your budget on litigation threats.

### Q20. Your liability as a broker

| Scenario | Likely position if you are a pure introducer | Where you can still be liable |
|---|---|---|
| Supplier fails to deliver / hardware underperforms | The compute contract is between buyer and supplier; you are not a party and gave no warranty | You described the supplier inaccurately, passed on claims you did not check as if they were verified, promised a result, or signed anything "on behalf of" a party |
| Data leak at the supplier | Supplier's contract and data-processing terms govern | You held the buyer's credentials or data yourself. Do not: never take account access, API keys or datasets |
| Buyer misuses compute (illegal content, attacks) | Supplier's acceptable-use policy governs | You knew or ignored obvious warning signs |
| Buyer is a restricted party or end use is prohibited | **Your own direct exposure** — see below | Cannot be shifted by contract |
| Buyer does not pay the supplier | Not your debt | Clawback of your commission [1]; any guarantee you gave (never give one) |

**What helps:**
- **"Not the provider" positioning** in every document, proposal and email signature: you introduce and advise; the supplier contracts with and bills the buyer.
- **No-warranty and liability-cap clauses** in the buyer agreement (cap at fees you actually received on that deal, exclusion of indirect losses). US courts generally uphold such caps between businesses, but usually not for fraud, intentional misconduct and, in several states, gross negligence — **[LAWYER]**.
- **Accurate labelling of information:** "supplier states" versus "we verified".
- **The LLC** shields personal assets from business contract claims in general, but not from your own personal wrongdoing (e.g. a sanctions violation you personally committed) — **[LAWYER]**.
- **Tech E&O insurance** covers negligence claims by clients (bad advice, mistakes). US broker sites show roughly $65–110/month ($800–1,300/year) for $1M limits for small IT firms [18]. Caveats: those figures are for typical US-based consultants; availability and price for a non-resident-owned LLC doing brokerage are **unverified**; policies normally exclude fines, penalties and intentional acts, so insurance does not cover export or sanctions penalties.

**Where liability cannot be disclaimed:**
- **Export controls (EAR).** No person may "cause or aid, abet, counsel, command, induce, procure, or permit" a prohibited act, and no person may sell, transfer, finance or "otherwise service" an item with knowledge that a violation has occurred or is about to occur (15 CFR 764.2(b) and (e)) [20]. How this applies to brokering remote/cloud access is covered in the compliance research; it is your personal and company risk, not something a contract moves.
- **Sanctions (OFAC).** Penalties apply to anyone who violates, attempts, conspires or **causes** a violation; the IEEPA civil maximum shown in current regulations is the greater of $377,700 or twice the transaction value, per violation [21]. A US LLC is a US person.
- **Misrepresentation or fraud** by you.
- **Undisclosed commissions** — see Q21.
- **Your own data-protection duties** for the contact data you hold (GDPR for EU contacts).

**Recommendation (Q20):** stay a pure introducer; never hold money, credentials or data; put the liability cap and "not the provider" wording in the buyer agreement; run compliance screening on every buyer; postpone E&O until the first signed deal or until a counterparty asks for it, then get quotes.

### Q21. Licences and registrations

**Honest caveat:** you cannot prove a negative by search. I found no US federal or state licence for brokering cloud/GPU services, and none of the public partner programmes asks partners for one [1][2][3][4]. **[LAWYER]** should confirm in one short answer.

| Regime | Does it apply? | What would trigger it |
|---|---|---|
| Securities (SEC / state) | Not for introducing customers to a cloud service | Selling investment-type products: shares in GPU revenue, "GPU yield" tokens, pooled hardware investments; raising money for suppliers; finder's fees on investment or loan deals (the GPU-financing idea in section 5 needs separate advice) |
| Commodities / derivatives (CFTC, NFA) | Not for spot or reserved capacity contracts where the buyer actually uses the compute (**[LAWYER]** confirm that long reserved-capacity contracts are service contracts, not regulated derivatives) | **Compute futures.** An introducing broker is anyone who, for compensation or profit, solicits or accepts orders for futures (and similar products) without holding customer funds; acting as one without registration is unlawful [10][11]. Registration requires NFA membership [11]. Being paid to advise on futures trading can separately make you a commodity trading advisor. Status of the products: CME and Silicon Data announced H100 and B200 rental index futures (12 May 2026, launch planned 5 October 2026); the CFTC extended its review to 9 November 2026; I could not confirm that trading has started [12][13]. You may tell a buyer that hedging products exist and point them to a registered broker for free. Do not solicit, take orders, earn a fee per trade, or advise on trades. |
| Money transmission (FinCEN, state licences) | No, **if buyers pay suppliers directly** and suppliers pay you a commission | Receiving the buyer's money and passing it to the supplier. FinCEN's exemption for funds transmitted "integral to the sale of goods or the provision of services" is available to the party that itself provides the goods or services [14]; a broker who only moves money may not fit, and state rules are separate and stricter. Never offer escrow. This also restricts the future reseller model: as a reseller you would be the seller, which is a different analysis — **[LAWYER]** |
| State "doing business" | The LLC must stay in good standing in its formation state (registered agent, annual report/fee). Registration in other states ("foreign qualification") is normally triggered by a physical presence such as an office or employees, not by having customers there (general rule, **unverified per state**) | Hiring in, or opening an office in, another state |
| Commercial bribery / secret commissions | Applies to how you get paid | New York: giving a benefit to an employee, agent or fiduciary without the consent of their employer or principal, intending to influence their conduct, is a crime [15]. California has a similar law for amounts above $250 where the person acts corruptly and without the employer's knowledge or consent [16]. Two practical rules: (1) **never pay a kickback or gift to an individual at a buyer or supplier** — any pass-back goes to the company, on the invoice or contract; (2) if you act for the buyer and receive supplier money, **disclose it and get written consent**. Under general agency law an agent who takes a benefit from a third party without the principal's informed consent breaches the duty of loyalty and may have to give up the benefit and the fee (Restatement (Third) of Agency §§ 8.02, 8.06 — from secondary summaries, **[LAWYER]**) |
| FTC advertising / endorsement rules | Yes, for your marketing | If you publish recommendations, comparisons or links and are paid by the recommended supplier, the connection must be disclosed clearly and conspicuously (16 CFR Part 255; the 2023 revision treats affiliate links as a material connection) [17]. Supplier terms also require it [1]. Put a standing disclosure on your website and in proposals |
| Export controls / sanctions | Yes, always | No licence to be a broker, but direct obligations — see `/compliance/` |

**EU / Montenegro, briefly:**
- The EU Commercial Agents Directive defines a commercial agent as someone with continuing authority to negotiate the **sale or purchase of goods** [23]. Compute is a service, and a referral partner has no authority to negotiate or conclude. So the Directive's protections (e.g. termination indemnity) probably do not help you, and its duties probably do not bind you; some member states extend their national rules to services — **unverified, [LAWYER] if you sign under an EU law**.
- I found no Montenegrin licence for B2B IT-service intermediation (**unverified**). Montenegro's Law on Obligations is the place where agency and brokerage contracts would be regulated; I could not verify its content. The more important Montenegro question is whether working from Montenegro for a US LLC requires local registration or creates local tax presence — this belongs to the tax research and the accountant list.
- EU-based buyers: your service agreement can keep US law, but GDPR applies to the personal contact data you hold, and misleading B2B marketing is restricted in the EU as well.

**Recommendation (Q21):** proceed without a licence on the basis that you (1) never hold customer funds, (2) never touch futures or derivatives, (3) never sell anything investment-like, and (4) disclose every commission in writing. Pay a lawyer to confirm exactly these four boundaries (see `/legal/questions-for-lawyer.md`, questions 1–3).

## Contradictions with earlier notes

- "Compute futures (CME with Silicon Data, launched May 2026)": the partnership was **announced** in May 2026; launch was planned for 5 October 2026 and then held up by CFTC review. Actual start of trading is unconfirmed [12][13].
- "Crusoe and RunPod: affiliate programs": RunPod's is a small-ticket self-serve programme paying credits, with cash only after 25 paying referrals [3]. Crusoe's terms are not public [9].
- "Nebius: referral for deals of 64+ GPUs": still quoted in search results, but the page now presents a general partner programme with no public figures [6].

## Questions for a lawyer / accountant

See `/legal/questions-for-lawyer.md` (prioritised, with the three worth paying for first).

## Sources
All checked 2026-11-09.

1. DigitalOcean, Affiliate Program Agreement (last updated 1 Jan 2025) — https://www.digitalocean.com/legal/affiliate-program-agreement
2. DigitalOcean, Partner Terms and Conditions (May 2024) — https://www.digitalocean.com/legal/partner-terms-and-conditions-may-2024
3. RunPod docs, Referral programs — https://docs.runpod.io/accounts-billing/referrals
4. Hyperbolic, Introducing Hyperbolic Partner Program — https://www.hyperbolic.ai/blog/introducing-hyperbolic-partner-program
5. Thunder Compute docs, Referral program — https://www.thundercompute.com/docs/guides/referral-program
6. Nebius, referral / partner programme page — https://nebius.com/referral (64/512-GPU wording seen in search snippet only)
7. Ingenuity Cloud Services, ICS Partner Program — https://www.ingenuitycloudservices.com/partner-program/ (figures from search snippet; brochure PDF returned 404)
8. Cirrascale, Referral Programs — https://referral.cirrascale.com (search snippet only; host not reachable from this session)
9. Crusoe, Partners — https://crusoe.ai/partners (no terms published)
10. CFTC Staff Letter 26-25 (17 Sep 2026), background section stating the introducing-broker definition and registration requirement — https://www.cftc.gov/csl/26-25/download
11. National Futures Association, Introducing Broker (IB) Registration — https://www.nfa.futures.org/registration-membership/who-has-to-register/ib.html
12. CME Group press releases, 12 May 2026 and 11 Aug 2026 — https://www.cmegroup.com/media-room/press-releases/2026/8/11/cme_group_and_silicondatatolaunchcomputefuturesonoctober5tounloc.html
13. Finance Magnates, "CFTC Plans AI Compute Derivatives Consultation as CME Targets October 5" — https://www.financemagnates.com/institutional-forex/cftc-plans-ai-compute-derivatives-consultation-as-cme-targets-october-5/ ; RuntimeWire (21 Oct 2026) — https://runtimewire.com/article/silicon-data-cme-compute-futures-november-2026
14. FinCEN administrative rulings FIN-2014-R004 and FIN-2014-R005 (integral-to-sale exemption) — https://www.fincen.gov/sites/default/files/administrative_ruling/FIN-2014-R004.pdf ; https://www.fincen.gov/sites/default/files/administrative_ruling/FIN-2014-R005.pdf (read via search summary)
15. New York Penal Law § 180.00 — https://newyork.public.law/laws/n.y._penal_law_section_180.00
16. California Penal Code § 641.3 — https://california.public.law/codes/penal_code_section_641.3
17. FTC, Endorsement Guides FAQ — https://www.ftc.gov/system/files/documents/plain-language/pdf-0205-endorsement-guides-faqs_0.pdf ; Manatt summary of the 2023 revision — https://manatt.com/insights/newsletters/advertising-law/an-in-depth-look-at-the-ftcs-updates-2 (secondary sources; primary text is 16 CFR Part 255)
18. Insureon, technology business insurance cost — https://www.insureon.com/technology-business-insurance/cost ; TechInsurance — https://www.techinsurance.com/ask-us/business-insurance-costs/cost-of-errors-and-omissions-insurance/
19. Case summaries (third-party, unverified against the opinions): Cura Financial v. Electronic Payment Exchange — https://www.studicata.com/summaries/court-of-chancery-of-delaware/cura-fin-svcs-v-electronic-payment-2001-6wfk8i ; Swartz Investments v. Vion Pharmaceuticals — https://www.studicata.com/summaries/court-of-appeals-of-georgia/swartz-investments-llc-v-vion-pharmaceuticals-inc-2001-nqpsfp
20. BIS, EAR Part 764 (§ 764.2) — https://www.bis.gov/regulations/ear/764 (wording read from search results of older CFR editions; confirm current text)
21. OFAC Enforcement Guidelines, 31 CFR Part 501 Appendix A — https://www.ecfr.gov/current/title-31/subtitle-B/chapter-V/part-501/appendix-Appendix%20A%20to%20Part%20501 ; penalty figure as shown at 31 CFR § 560.701 via https://www.customsmobile.com/regulations/expand/title31_chapterV_part560_subpartG_section560.705 (search summary)
22. Aceris Law, Arbitration in Montenegro — https://www.acerislaw.com/arbitration-in-montenegro
23. Council Directive 86/653/EEC — https://www.legislation.gov.uk/eudr/1986/653?view=plain
24. Lambda, Partners — https://lambda.ai/partners (no terms published)
