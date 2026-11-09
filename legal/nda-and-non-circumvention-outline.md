# Mutual NDA with non-circumvention clause, and deal-registration email — OUTLINE FOR LAWYER REVIEW
_Last checked: 2026-11-09_

> **This is an outline for lawyer review, not a final contract and not legal advice.** Background and sources: `/research/legal-and-contracts.md` (Q18).

## Summary

- Use this with **smaller suppliers, data-centre operators, capacity holders and other intermediaries** that have no formal partner programme. Established GPU clouds will insist on their own NDA and deal-registration process; accept those.
- **Be realistic:** you cannot afford to enforce this document. Its value is (a) deterrence, (b) a clear written record of who introduced whom, (c) filtering out parties who refuse to sign anything.
- Keep it short (2–3 pages), mutual and narrow. Long "NCNDA" templates with 5-year terms and huge penalties look amateurish and are more likely to be unenforceable.
- The **deal-registration email** in Part B matters more than the NDA. Send it before you reveal a buyer's name, and get a written reply.
- Never use the NDA to hide your commission from a buyer. Commission disclosure is always permitted.

## Part A. Mutual NDA with non-circumvention — clause outline

| # | Clause | Outline content | Notes for lawyer review |
|---|---|---|---|
| 1 | Parties and date | Your US LLC; the counterparty's exact legal entity, registration number, address | Confirm signatory authority |
| 2 | Purpose | Evaluating and carrying out introductions between buyers of GPU compute capacity and suppliers of it | Narrow purpose supports enforceability |
| 3 | Confidential information | Non-public business information disclosed for the purpose: identities and requirements of introduced parties, pricing, capacity availability, contract terms | Mutual |
| 4 | Exclusions | Information already known, public, independently developed, or lawfully received from a third party | Standard |
| 5 | Obligations | Use only for the purpose; protect with reasonable care; share only with staff and advisers who need it and are bound by confidentiality | |
| 6 | Permitted disclosures | Required by law or regulator; **to authorities for export-control, sanctions or anti-money-laundering compliance; disclosure to a buyer of the existence and amount of any commission** | Essential carve-outs; never let an NDA block compliance reporting or commission disclosure |
| 7 | "Introduced Party" definition | A buyer or supplier that one party introduces to the other **by written notice (the deal-registration email) naming the legal entity**, and that the receiving party did not already have a documented relationship or active discussion with in the previous 12 months | Protection only for named, registered introductions — not "all contacts" |
| 8 | Acceptance or objection | The receiving party must object in writing within 5 business days if it already knows the Introduced Party, with reasonable evidence; otherwise the introduction is accepted | Creates the paper trail |
| 9 | Non-circumvention | For the protection period, the receiving party will not, directly or through affiliates or third parties, enter into a compute-capacity transaction with an Introduced Party **without the introducer's involvement or without paying the agreed commission/fee** | Framed as "pay the commission", not "never deal" — more reasonable, more likely to be upheld |
| 10 | Protection period | 12 months from each registration, extended while negotiations with that Introduced Party are active; ideal 24 months, fallback 6 | Excessive duration is a common reason clauses fail |
| 11 | Remedy | If circumvention occurs, the introducer is entitled to the commission it would have earned under the agreed rate (or a stated rate, e.g. X% of contract value, if no referral agreement exists yet) | Lawyer to advise on whether a fixed-rate remedy risks being treated as an unenforceable penalty |
| 12 | No obligation to deal | Neither party must enter into any transaction; no exclusivity | |
| 13 | No agency | Neither party is the other's agent or may bind it | Consistent with "not the provider" |
| 14 | Compliance | Each party complies with export-control, sanctions and anti-bribery laws; either may refuse any introduction on compliance grounds without liability | |
| 15 | Term | 2 years for making introductions; confidentiality survives 2–3 years after disclosure; clause 9 survives for each protection period | |
| 16 | Return / destruction | On request, except copies required by law or for compliance records | You must keep KYC records |
| 17 | Governing law and disputes | Ideal: your LLC's state law, courts of that state. Fallback: New York or Delaware law. Option for cross-border counterparties: arbitration (awards are easier to enforce internationally than court judgments) | Lawyer to recommend the cheapest workable forum |
| 18 | General | Entire agreement, written amendments only, electronic signatures, counterparts | |

**Positions**

| Point | Ideal | Fallback | Walk away |
|---|---|---|---|
| Non-circumvention | Clause 9 as written | Counterparty's own deal-registration confirmation in writing instead | Counterparty refuses both any NDA and any written registration |
| Period | 24 months | 6–12 months | Under 3 months |
| Disclosure carve-outs (clause 6) | As written | — | Counterparty requires commission to be secret from the buyer |

**What this document will not do:** stop a determined party from bypassing you; produce money without legal action you cannot fund; bind the counterparty's customers or affiliates who did not sign. Plan your process so that being bypassed once is survivable.

## Part B. Deal-registration email format

Send **before** disclosing the buyer's identity in any other way. One email per buyer per supplier. Keep the reply.

```
Subject: Deal registration – [Your LLC] – [Buyer legal name] – [date]

Hello [Partner manager name],

Under our [Referral Agreement dated … / NDA dated … / your partner programme],
I am registering the following opportunity:

1. Customer legal name:        [exact entity name]
2. Website / domain:           [domain]
3. Country (HQ and end use):   [country / countries]
4. Contact at customer:        [name, title] (shared with the customer's consent)
5. Requirement:                [GPU type, quantity, start date, term, region, workload type]
6. Estimated contract value:   [range]
7. How we are involved:        [introduced on (date); we will stay involved in …]
8. Compliance:                 [Our screening against US restricted-party lists was
                               completed on (date) with no match. We understand you
                               will run your own customer due diligence.]

Please confirm by reply:
(a) that this opportunity is registered to [Your LLC] as partner of record;
(b) the registration date and expiry date;
(c) the commission rate and duration that will apply; and
(d) if you cannot accept the registration, the reason (for example, existing
    customer or active opportunity).

Disclosure: we inform every customer in writing that we may receive a referral
commission from the supplier they choose.

Thank you,
[Name], [Your LLC]
```

**Usage rules**
1. No reply is not acceptance. Follow up once after 3 business days; if still nothing, do not make the introduction on a commission basis.
2. If the supplier answers "existing customer", ask for the date of the existing relationship and log it; do not argue.
3. Line 8 must be true. Only write it after you have actually done the screening described in `/compliance/`.
4. Share the buyer's contact details only with the buyer's consent (confidentiality and GDPR).
5. Save the confirmation as PDF in the deal folder and record the expiry date in the pipeline tracker; ask for an extension two weeks before expiry.

## Questions for a lawyer

See `/legal/questions-for-lawyer.md`, section "NDA and non-circumvention".
