# Questions for a lawyer
_Last checked: 2026-11-09_

> Running list. Sections 1–6 below come from the legal and contracts research (`/research/legal-and-contracts.md` and the outlines in `/legal/`). **Questions from other research areas (compliance, tax, entity) are to be merged in under their own headings at the end.** Nothing here is legal advice; the "current working assumption" column is what the research suggests, to be confirmed or corrected.

## Summary

- With under $2,000 total budget, legal spend must be small and targeted: **aim for one fixed-fee engagement of roughly 1–2 hours** with a US business lawyer, plus a separate short consultation with an export-control specialist (see compliance questions). Typical prices for such engagements were not verified; get two or three fixed quotes first.
- **The three questions worth paying for first are P1-1, P1-2 and P1-3**: (1) confirm no licence is needed and where the boundaries are, (2) review the buyer engagement letter, especially commission disclosure and the liability cap, (3) confirm that the combined fee model is lawful and how to disclose it.
- Everything marked P2 can wait until the first real supplier agreement is on the table; P3 can wait until there is revenue.
- Cheap routes: fixed-fee document review; a flat-fee marketplace lawyer; a law-school clinic or startup legal clinic; the supplier's own partner manager (for questions about their terms, free); bar-association referral services that offer low-cost first consultations. None of these were contacted or priced.
- Send the lawyer the outlines in `/legal/` and a one-page description of the business in advance, with the questions numbered as below, and ask for written answers. That keeps the meter low.

## How to read the priority column

| Priority | Meaning |
|---|---|
| **P1** | Ask before the first deal. Pay for these. |
| **P2** | Ask when a specific document or deal makes it relevant. |
| **P3** | Ask later, when there is revenue or a change of model. |

---

## 1. Licensing and regulatory boundaries (US)

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 1 | P1 | Does a US LLC that introduces buyers to GPU cloud providers for a referral commission and/or a disclosed buyer fee, never holding customer money, need any federal or state licence or registration (beyond keeping the LLC in good standing)? | Operating an unlicensed regulated business is the most basic risk | No licence found; not securities, commodities or money transmission within these boundaries | Fixed-fee 1-hour consult; ask for a short written confirmation |
| 2 | P1 | Where exactly are the lines I must not cross: (a) receiving buyer funds and paying suppliers, escrow or deposits (money transmission, federal and state); (b) anything investment-like (GPU revenue shares, financing introductions); (c) compute futures and other derivatives? | So I can write hard "never do" rules into the compliance policy | Never hold funds; never sell investment products; never solicit, accept orders for, or advise on futures | Same consult as #1 |
| 3 | P3 | If CME/ICE compute futures are trading: may I mention their existence and refer a buyer to a registered broker for free? Would any referral fee from a futures broker make me an introducing broker or an associated person? Does the NFA exemption for non-US persons with only non-US customers help a US LLC owned by a non-resident? | Section 5 of the plan asks whether a small intermediary has a role in futures | Mentioning is fine; any compensation linked to orders is not | Do not pay for this unless you actually want to pursue it |
| 4 | P2 | Are long reserved-capacity contracts (12–36 months, fixed price, sometimes transferable) ordinary service contracts, or could brokering resale of reserved capacity ever be treated as dealing in swaps or forwards? | Relevant to the "idle reserved capacity" opportunity | Service contracts where the buyer actually uses the compute | Add to the first consult only if time allows |
| 5 | P2 | Does my LLC need to register ("foreign-qualify") in any state other than its formation state, given that I work from Montenegro and have no US office or staff? | Avoid state penalties and loss of the right to sue | No, while there is no physical US presence | Ask the registered-agent company (free) and confirm with accountant |
| 6 | P3 | If I later resell capacity (buy and re-sell at a markup), what changes: money transmission analysis, sales tax, liability as provider, export-control status as provider? | Planning for model 4 | Much heavier; out of scope for now | Later |

## 2. Commission disclosure and conflicts of interest

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 7 | P1 | Is my commission-disclosure wording (see buyer agreement outline, clause 4) sufficient to avoid breach of fiduciary duty, commercial-bribery statutes (e.g. NY Penal Law § 180.00, Cal. Penal Code § 641.3) and deceptive-practice claims? Must I state the exact percentage per supplier, or is a range plus "on request" enough? | Undisclosed commissions can mean losing the fee and criminal exposure | Written disclosure of fact and rate, plus the buyer's written consent, before the buyer signs with a supplier | Part of the fixed-fee review of the buyer letter |
| 8 | P1 | Is the combined model lawful (supplier commission plus buyer-paid fee, or passing part of the commission to the buyer company) if fully disclosed to both sides? Any wording I must use toward the supplier? | This is revenue model 3 | Lawful with full disclosure, but may breach individual supplier terms | Same review; also read each supplier's terms yourself first |
| 9 | P2 | Am I legally the buyer's agent (with fiduciary duties) under Model A, where only the supplier pays me? Can the engagement letter limit those duties? | Determines how strict my duties are | Assume duties of honesty and disclosure apply in every model | Same review |
| 10 | P2 | What disclosure must appear on my website, comparison pages, LinkedIn posts and emails under the FTC Endorsement Guides when I am paid by suppliers I mention? | Marketing compliance | A clear standing disclosure near any recommendation | Read the FTC FAQ yourself (free); ask only if unsure |

## 3. Buyer service agreement

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 11 | P1 | Please review the engagement-letter outline: are the "not the provider", no-warranty and liability-cap clauses enforceable under the chosen state's law, and how must they be formatted (conspicuousness)? What can never be excluded (fraud, gross negligence, wilful misconduct)? | This is my main protection if a supplier fails | Cap at fees received is generally enforceable between businesses, with carve-outs | Fixed-fee document review — the single best use of legal budget |
| 12 | P1 | Which governing law and forum should my standard documents use, given a US LLC, a founder in Montenegro, and buyers in the US, EU and Balkans? | Affects enforceability and cost | LLC's formation state, or Delaware/New York | Same review |
| 13 | P2 | Can the buyer compliance representations (end user, end use, sanctions, payment source) be worded so they support, and do not weaken, my own export-control position? | They must match the compliance policy | They help evidence diligence but do not shift liability | Ask the export-control specialist (see compliance section) |
| 14 | P2 | For EU or Montenegrin buyers, do local mandatory rules override my US-law letter (e.g. limits on liability exclusions, consumer-type protections for micro-businesses)? | Avoid a void clause | B2B only; low risk | Montenegro/EU lawyer, only when the first such buyer appears |
| 15 | P3 | Is clause 12 (buyer acknowledges introduced suppliers for 12 months) reasonable and enforceable? | Bypass protection on the buyer side | Reasonable if narrow | With the review if time allows |

## 4. Supplier referral agreements

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 16 | P2 | Please review the first significant supplier referral agreement I am offered: tail, clawback, termination, unilateral change, bans on customer-paid fees, indemnities. Which points are worth pushing back on? | The supplier's paper controls my income | Use `/legal/referral-agreement-outline.md` Part B first | Do the checklist yourself; pay for review only when expected commission exceeds roughly ten times the lawyer's fee |
| 17 | P2 | If a supplier's terms say I lose commission when the customer pays me anything, does a separately invoiced advisory fee to the buyer breach that? | Protects the combined model | Likely yes unless carved out; ask the supplier in writing | Ask the supplier's partner manager (free), in writing |
| 18 | P2 | Do compliance clauses in supplier agreements make me responsible for the customer's export-control compliance? How should responsibility be split? | Avoid taking on the provider's duties | Each party is responsible for its own compliance; the supplier screens its own customers | With review #16, or the export-control specialist |
| 19 | P3 | Which IRS form should the LLC give to US suppliers paying commissions, and can they withhold tax? | Avoid 30% withholding surprises | Accountant question | Accountant |

## 5. NDA and non-circumvention

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 20 | P2 | Is the non-circumvention clause in my NDA outline (named introductions only, 12 months, remedy equal to lost commission) likely to be enforceable under the chosen law? Is a fixed-percentage remedy a penalty? | To avoid relying on a void clause | Narrow clauses are more enforceable; outcomes vary by state | Include in the fixed-fee review if the price allows; otherwise use as is, knowing it is mainly a deterrent |
| 21 | P3 | Court or arbitration clause for cross-border counterparties, given I cannot fund either? Is there a low-cost online arbitration option worth naming? | Enforceability across borders | Arbitration awards travel better; cost is the obstacle | Later |
| 22 | P3 | What is the cheapest effective step if I am bypassed (demand letter cost, small-claims options)? | Realistic enforcement plan | Probably a single demand letter, then write it off | Later |

## 6. Liability and insurance

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 23 | P2 | In which situations could I be personally liable despite the LLC (own torts, misrepresentation, export or sanctions violations, failure to keep the LLC separate from personal finances)? | Personal asset risk | The LLC does not protect against my own wrongdoing | First consult, 5 minutes |
| 24 | P2 | Can a non-resident-owned US LLC doing compute brokerage obtain tech E&O insurance, at what price, and what does it exclude (fines, export violations, intentional acts)? | Budget decision | US sites quote about $800–1,300 per year for small IT firms; applicability unverified | Free quotes from an insurance broker — not a lawyer question. Only when a deal requires it (asking for quotes means contacting third parties; decide first) |
| 25 | P3 | If a buyer suffers loss because a supplier I recommended failed, what claims could realistically be brought against me, and does my process (labelling verified versus unverified information) reduce them? | Process design | Negligent misrepresentation is the main theory | With review #11 |

## 7. Montenegro / EU (for a Montenegro lawyer or adviser)

| # | Pri | Question | Why it matters | Current working assumption | Cheap way to get it answered |
|---|---|---|---|---|---|
| 26 | P1 | Does doing this work physically from Montenegro for my US LLC require registering a business, branch or as an entrepreneur in Montenegro, or any local licence for intermediation? | Local legality; overlaps with tax | Unverified — depends on tax/permanent-establishment analysis | Combine with the accountant's tax consultation, in one meeting |
| 27 | P3 | Does Montenegro's Law on Obligations give a commercial agent or broker mandatory rights or duties (commission, termination compensation) that would apply to my contracts with local suppliers or buyers? | Contracting with Balkan parties | Unverified | Only when a local-law contract is proposed |
| 28 | P3 | If I sign a referral agreement governed by an EU member state's law, do commercial-agent protections (e.g. termination indemnity) apply to referral of services? | Could strengthen my position, or not apply at all | The EU Directive covers goods; national laws vary | Only when relevant |

---

## Suggested first engagement (to fit the budget)

1. **Before paying anyone:** finish your own checklist review of the documents; read the FTC FAQ; ask suppliers' partner managers the questions marked "free".
2. **One fixed-fee US business lawyer session** covering questions 1, 2, 7, 8, 11, 12 (and 9, 23 if time allows), with the buyer engagement-letter outline sent in advance.
3. **Export-control specialist**: see the compliance section below (to be merged). If money allows only one paid consultation in total, discuss with whoever maintains the compliance questions which is the higher risk; on the legal side alone, items 1, 7 and 11 come first.
4. **Montenegro adviser**: question 26 together with the tax questions.

---

## Questions from other research areas (to be merged)

_(Compliance / export control, tax and entity questions go here under their own headings.)_
