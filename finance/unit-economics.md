# Unit economics and pricing (Q14, Q16)
_Last checked: 2026-11-09_

## Summary
- Realistic cash commission from suppliers is **5–10% of what the customer pays**, usually for a limited period (often 6–12 months). Self-serve "affiliate" programs pay 1–3%, mostly in credits, and are not a business. See `research/supplier-programs.md`.
- A commission is only money when (a) the customer actually pays the supplier and (b) the supplier pays you, typically 30–90 days later. Plan for **no cash before month 4–6**.
- One 8-GPU deal is pocket money (about $900–$1,400/month). **One 32-GPU, 12-month deal is a living** (about $3,500–$5,600/month). The business works on a few mid-size deals, not many tiny ones.
- A buyer-paid fee is hard to charge because most competitors are free to the buyer, and some supplier programs forfeit your commission if the buyer also pays you. Use paid work only for a clearly separate service (a fixed-fee "sourcing sprint").
- The numbers below are **illustrations, not forecasts**. The inputs that matter most (deal size, how long the customer stays, whether the supplier pays for the full term) are unknown until real agreements are signed.

## Assumptions
| Input | Value | Basis |
|---|---|---|
| Hours per GPU-month | 730 | 24 × 365 / 12 |
| H100 reserved price | $3.00 / GPU-hour | Rounded, conservative against Ornn's $3.37 spot reading of 8 Nov 2026 and a second-hand $2.65–2.80 one-year contract figure. See `research/pricing-and-indexes.md`. |
| B200 reserved price | $7.50 / GPU-hour | Between Silicon Data ($6.84) and GetDeploying median ($8.55); Ornn shows $9.94. Indexes disagree widely. |
| Commission | 5% (low), 8% (mid), 10% (high) | Published cash programs. Unverified for most suppliers. |
| Utilisation | 100% of a reserved contract | Reserved deals bill whether used or not. On-demand deals will be far lower. |

## What one deal pays (per month, while the commission lasts)
| Deal | Customer spend / month | 3% | 5% | 8% | 10% |
|---|---|---|---|---|---|
| 8 × H100 | $17,520 | $526 | $876 | $1,402 | $1,752 |
| 32 × H100 | $70,080 | $2,102 | $3,504 | $5,606 | $7,008 |
| 64 × H100 | $140,160 | $4,205 | $7,008 | $11,213 | $14,016 |
| 8 × B200 | $43,800 | – | $2,190 | $3,504 | – |
| 32 × B200 | $175,200 | – | $8,760 | $14,016 | – |

## Portfolio scenarios (H100 at $3.00/hr)
| Active deals | Mix | Customer spend / month | Income / month at 5% | at 8% | Income / year at 5% | at 8% |
|---|---|---|---|---|---|---|
| 1 | one 8-GPU deal | $17,520 | $876 | $1,402 | $10,512 | $16,819 |
| 1 | one 32-GPU deal | $70,080 | $3,504 | $5,606 | $42,048 | $67,277 |
| 5 | three 8-GPU + two 32-GPU | $192,720 | $9,636 | $15,418 | $115,632 | $185,011 |
| 20 | twelve 8-GPU, six 32-GPU, two 64-GPU | $911,040 | $45,552 | $72,883 | $546,624 | $874,598 |

**Read these with scepticism.** The yearly figures assume every deal runs 12 months, the commission is paid for the whole term, and no customer leaves or stops paying. Twenty simultaneous active deals for one person is a year-three outcome at best, and it would need help with compliance and account management. A sensible first-year target is **2–4 closed deals**.

## Haircuts to apply to any forecast
1. **Commission tail.** Several programs pay for 6 months only (RunPod, Hyperbolic). Halve the yearly figure for those.
2. **Short and on-demand deals.** A 4-week burst of 8 GPUs at 8% pays about $1,300 once.
3. **Clawbacks.** If the customer gets a refund or does not pay, the supplier takes the commission back.
4. **Payout delay.** Customer invoice → customer pays (30 days) → supplier pays you (30–60 days more).
5. **Deals that die.** Assume most qualified leads do not close. Until there is real data, plan on 1 in 10.
6. **Tax.** Montenegro taxes the income (see `finance/tax-notes.md`); US filing costs about $300–750 a year.

## Costs (first 6 months, budget under $2,000)
| Item | Estimate | Note |
|---|---|---|
| US Form 5472 filing service | $300–750 | Mandatory; $25,000 penalty for missing it. |
| One Montenegrin tax consultation (written) | unverified, ask for a fixed quote | Highest-value spend. |
| One fixed-fee US lawyer session | unverified, ask for a fixed quote | Covers commission disclosure, §744.6 "support", liability cap. |
| Domain, email, simple website | ~$50–100 | |
| Screening tools, CRM, price data | $0 | Free tiers are enough to start. |
| DSC Europe one-day pass (optional) | €350 + VAT + travel | Would use roughly a quarter of the budget. |
| E&O insurance | $800–1,300 / year | Defer until there is revenue. |

The budget covers the compliance and tax basics and one or two professional consultations. It does not cover several conferences, paid data, or insurance.

## Buyer-paid fee: what is realistic
- **Free basic sourcing**, paid by disclosed supplier commission. This is the market norm.
- **Paid "sourcing sprint"**: fixed fee (for example $500–$1,500) for a written comparison of 3–5 vetted offers, contract-term comparison and a test-access plan. Charge it only where the supplier agreement allows, and always disclose any commission. Pricing here is my suggestion, not a market-verified figure.
- **Success fee on top of the supplier price** (for example 2–3% of contract value): possible for buyers who want a supplier that pays no commission. Needs a signed buyer agreement.

## How price moves affect each model (Q16)
| Model | Prices rising (now) | Prices falling |
|---|---|---|
| Referral % | Commission per deal goes up, but sold-out suppliers need partners less and may cut or close programs. | Commission per deal shrinks, but suppliers with idle capacity pay more and welcome brokers. |
| Buyer fee (fixed) | Buyers value help finding scarce capacity; the fee is easier to justify. | Capacity is easy to find; the fee is hard to justify. |
| Reseller | Margin if capacity was locked in early. | **Dangerous**: you hold a commitment above market price and customers walk. Not for this budget. |

A broker paid by percentage is naturally hedged: it earns in both markets, just from different sides. That is another reason to stay out of reselling.

## Sources
See `research/pricing-and-indexes.md`, `research/supplier-programs.md`, `research/legal-and-contracts.md` and `finance/tax-notes.md` for the underlying sources. The arithmetic in this file is my own.
