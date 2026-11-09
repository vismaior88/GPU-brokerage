# Business model, niche and operations (Q1, Q2, Q30–33)
_Last checked: 2026-11-09_

This file is the analyst's synthesis of the other research files. It contains judgement, not new facts; the facts and their sources are in the files named in each section.

## Summary
- **Model:** start as a **referral partner** paid by disclosed supplier commission, with free basic sourcing for buyers. Add one paid, clearly separate service (a fixed-fee "sourcing sprint"). No reselling and no compute futures.
- **Niche:** mid-size deals (**8–128 GPUs, 3–12 months**) for **European and Western Balkans buyers who want EU-hosted capacity**, served in English and Serbian.
- **Honest view of the edge:** today there is none. Competitors are well funded and mostly free to buyers. The edge has to be built: a verified map of EU/SEE suppliers, real vetting, contract comparison, a named person who answers, and visible compliance.
- **Biggest risks:** (1) no cash for 4–6 months on a budget under $2,000; (2) Montenegrin tax exposure on the LLC's income; (3) a single bad deal on the compliance side; (4) suppliers that are sold out not needing a broker.
- **Stop/pivot test:** if by day 90 there are fewer than 2 signed supplier agreements and fewer than 5 qualified buyer conversations, or by month 6 no deal is in contract, pivot to paid advisory and the newsletter, or stop.

## Q1 — Which revenue model, and in what order?
| Model | Capital | Risk | Realistic now? | Verdict |
|---|---|---|---|---|
| 1. Referral partner | None | Low: depends on supplier paying; commission tails are short | Yes, with 3–5 suppliers that accept a new one-person LLC | **Start here** |
| 2. Buyer-paid fee | None | Low, but hard to sell because competitors are free to the buyer | Only as a separate fixed-fee service | **Add as a "sourcing sprint"** |
| 3. Combined | None | Legal: some supplier terms forfeit commission if the buyer pays you too; undisclosed commissions can be unlawful | Only with written disclosure, buyer consent and a check of each supplier's terms | **Case by case** |
| 4. Reseller | High | High: customer non-payment, price drops, and you become the contracting party for export-control purposes | No | **Not before steady income and legal advice** |

Sequence: referral only (months 0–6) → referral plus paid sprint once a buyer asks for more work than a commission justifies → consider selective combined deals → reselling only if there is 12+ months of steady commission income, a lawyer's sign-off and capital that can be lost. See `finance/unit-economics.md` and `research/legal-and-contracts.md`.

## Q2 — Which niche?
| Option | Assessment |
|---|---|
| **EU-hosted / sovereign** | **Choose.** Data residency is the reason buyers gave most often in the one buyer study found; EU suppliers with thin sales teams are the ones most likely to pay a broker. |
| **Balkans / SEE** | **Choose as the entry point for buyers**, not for supply. Language and location are a real advantage. Supply is thin (one commercial GPU service found in Belgrade), and free public compute competes for the smallest buyers. |
| Middle East, Asia hubs | **Avoid.** These are the diversion-risk regions in enforcement cases. Too much compliance risk for a new broker. |
| LatAm, India, Africa | Later. No network, no language advantage. |
| **8–128 GPUs** | **Choose.** Large clusters go direct or to funded brokers; under 8 GPUs goes self-serve on marketplaces. Nebius's referral program starts at 64 GPUs. |
| Hopper vs Blackwell | Both. Sell what verified suppliers actually have. Blackwell prices are less transparent, so a comparison is worth more there. |
| Workload | Reserved training/fine-tuning and steady inference (3–12 months). Short bursts pay almost nothing. |
| Customer type | Funded AI startups, AI agencies/consultancies and research groups with budget. Enterprises take too long for a first deal. |

## Q3–Q5 — see `research/market-and-competitors.md`
In one line: buyers will not use a new broker for price. They may use one for a verified shortlist of EU options, a side-by-side comparison of contract terms, help with test access and acceptance, and someone accountable by name.

## Q30 — Minimal tools and processes for month one (all free unless stated)
| Need | Tool | Cost |
|---|---|---|
| Trackers / CRM | `suppliers/suppliers.csv` and `buyers/pipeline.csv` in this project; a free CRM tier later if volume demands | $0 |
| Screening | US Consolidated Screening List, OFAC search, EU and UK lists; saved PDFs per deal | $0 |
| Compliance | `compliance/` policy, checklist, red flags; one deal folder per buyer | $0 |
| Contracts | Outlines in `legal/`; use suppliers' own partner agreements, reviewed against the checklist | $0 until lawyer review |
| Price data | Free tiers of Ornn, Silicon Data, GetDeploying, GPUPerHour; a weekly snapshot in this project | $0 |
| Intake | `buyers/intake-form.md` as an online form | $0 |
| Presence | Domain, business email, one-page website, complete LinkedIn profile | ~$50–100 |
| Bank | US business account for the LLC (eligibility for a Montenegro resident must be confirmed with each provider) | $0 |
| Tax | Form 5472 filing service; Montenegrin tax consultation | ~$300–750 plus consultation |

Weekly routine: Monday price snapshot and pipeline review; daily outreach block; Friday update of trackers, decision log and open questions.

## Q31 — Weekly metrics
1. New conversations held: buyers and suppliers (target 5+ per week in the first 90 days)
2. Qualified buyers (completed intake form and passed KYC)
3. Quotes sent, and time from intake to quote (target under 48 hours)
4. Supplier agreements signed / in negotiation
5. Deals in contract; deals closed; deals lost with the reason
6. Deals refused on compliance grounds (a healthy number is not zero)
7. Commission booked versus cash received
8. Cash spent against the $2,000 budget
9. Hours worked

## Q32 — Path to the first paid deal, and when to stop
1. **Weeks 1–2:** tax and banking basics; web presence; apply to 3–5 partner programs.
2. **Weeks 2–6:** 15–20 free discovery conversations in the Belgrade/Zagreb/Ljubljana AI community and with EU startups, to learn what buyers actually struggle with. No selling.
3. **Weeks 4–10:** first qualified buyer; quote from 2–3 vetted suppliers; test access; contract between buyer and supplier.
4. **Months 3–6:** first commission invoice. Cash arrives 1–3 months after the buyer starts paying.

Stop or pivot signals:
- Day 45: no supplier will sign a referral agreement with a new one-person LLC → the model does not work as planned; switch to paid advisory.
- Day 90: fewer than 2 supplier agreements **and** fewer than 5 qualified buyer conversations.
- Month 6: no deal in contract, or the budget is spent with no commission booked.
- Any time: the Montenegrin tax or legal advice makes the structure unworkable, or a rule change (for example the Remote Access Security Act) puts brokers under licensing.

## Q33 — When to move to reselling or own software
- **Reselling:** not before 12 months of steady commissions, a lawyer's advice on the change in legal role, and capital at risk that can be lost. Probably never the right first expansion.
- **Software:** start with content, not code. A free weekly price note for the region builds the audience. Consider a paid tracker or verification service only when buyers ask for it repeatedly.
- **Better first expansions:** paid sourcing sprints and colocation referrals (published terms exist). See `research/opportunities.md`.

## Sources
This file draws on: `research/market-and-competitors.md`, `research/pricing-and-indexes.md`, `research/supplier-programs.md`, `research/demand-side.md`, `research/legal-and-contracts.md`, `research/opportunities.md`, `research/export-controls.md`, `finance/tax-notes.md` and `finance/unit-economics.md`. External sources are listed in those files.
