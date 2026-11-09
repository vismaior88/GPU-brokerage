# Pricing, price indexes and how price moves affect revenue (Q15, Q16)
_Last checked: 2026-11-09_

## Summary

- **Prices are rising, and the founder's three claims are broadly right.** On Ornn's index (settled 8 Nov 2026): H100 SXM **$3.37**/GPU-hr (+18.2% in a month), H200 **$6.82** (+20.1%), B200 **$9.94** (+33.1%) [1]. The "$3.10 H100" figure is consistent with early November and is already out of date; "B200 +31% in a month" matches (+33% now).
- **"Up ~20% year on year" depends on the index.** GetDeploying's broad on-demand index shows **+9%** YoY across 22 GPU models, but **+25%** for the H100 [2]. Contract-price measures show more: SemiAnalysis's 1-year H100 contract index rose ~38% from Oct 2025 to Mar 2026 [3]. Say "H100 up roughly 25% YoY on list prices", not "GPUs up 20%".
- **Indexes disagree a lot, especially on Blackwell.** On the same weekend, B200 was $9.94 on Ornn [1], $6.84 on Silicon Data [4] and $8.55 (GPU-cloud list median) on GetDeploying [2]. Never quote a single index as "the market price". Quote a range and name the sources.
- **Free data is enough to start.** Ornn (latest value + 3 months of daily history, free API), Silicon Data (headline value + 30-day table), GetDeploying (weekly index, per-provider prices) and GPUPerHour (live in-stock prices) cost nothing [1][2][4][5]. Do not pay for data in the first six months.
- **Index prices are for small on-demand rentals.** Reserved and multi-month deals are negotiated; typical published discounts are about 26% (1-year) and 48% (3-year) below on-demand [2]. A real quote always comes from the supplier.
- **Compute futures are not live in the US yet.** CME's H100 and B200 futures (Silicon Data indexes) missed the 5 Oct 2026 target; the CFTC review was extended to 9 Nov 2026 and no launch is confirmed [6][7]. ICE/Ornn has no date [8]. The founder's note "launched May 2026" is wrong: May was the announcement.
- **Rising prices help percentage-based income per deal but make deals harder to source.** Referral % and %-based buyer fees grow with price; a reseller holding fixed-price capacity gains in a rising market and can be wiped out in a falling one. This supports staying out of reselling.

## Details

### Q15a. Current price levels (November 2026)

All figures are US dollars per GPU per hour.

| GPU | Ornn spot index, 8 Nov [1] | Silicon Data neo-cloud index, 9 Nov [4] | GetDeploying list median, GPU clouds / hyperscalers, wk of 9 Nov [2] | Other |
|---|---|---|---|---|
| H100 (SXM) | $3.37 (+18.2% 1-mo) | $3.01 | $5.33 / $7.89 (overall median $3.73, 44 providers) | GPUPerHour in-stock: low $2.59, median $3.11 [5]. Uvik list median (7 Oct): $4.20 [3] |
| H200 | $6.82 (+20.1% 1-mo) | $3.48 | $5.85 / $10.85 | Uvik (7 Oct): $5.70 [3] |
| B200 | $9.94 (+33.1% 1-mo) | $6.84 (+15.3% 7-day) | $8.55 / $14.24 | Uvik (7 Oct): $8.19 [3] |
| B300 | not in free set | $7.68 (+15.1% 7-day) | n/a | Uvik (7 Oct): $9.50 [3] |
| A100 | $1.03 (+9.6% 1-mo) | $1.59 | $2.70 / $3.67 | Uvik A100 80GB (7 Oct): $2.75 [3] |
| RTX PRO 6000 | $1.54 (+6.2% 1-mo) | n/a | $2.15 / $4.50 | |
| MI300X (AMD) | n/a | $2.77 | n/a | Uvik (7 Oct): $3.45 [3] |
| L40S | n/a | n/a | n/a | Uvik (7 Oct): $1.62 [3] |

**Why the numbers differ.** Each source measures something different: Ornn describes its index as based on traded spot prices; Silicon Data standardises observations from neo-clouds and marketplaces; GetDeploying and Uvik take medians of public list prices; GPUPerHour shows the cheapest listing actually in stock. The large Ornn vs Silicon Data gap on H200 and B200 is not explained by either publisher and should be treated as real uncertainty about the "true" price.

**On-demand vs reserved.**
- GetDeploying: 1-year reservations average ~26% below on-demand, 3-year ~48% below, spot ~43% below [2].
- H100 1-year contract price (SemiAnalysis survey index): $1.70 in Oct 2025 to $2.35 in Mar 2026 [3]. Later readings of about $2.65–$2.80 have been reported second-hand **(unverified)** [9].
- Hyperscaler 3-year H100 commitments: about $2.97 (AWS) to $5.40 (Azure) [3].

**Trend.**
- Past month: sharp rise in Hopper and Blackwell on Ornn (+18% to +33%) [1]; Silicon Data H100 moved from $2.83 (11 Oct) to $3.01 (9 Nov), about +6% [4]. GetDeploying's broad list-price index was flat over four weeks, with H100 +7% [2]. List prices lag spot.
- Supplier list-price increases: Nebius raised H100 from $3.85 to $4.50 (+17%) and H200 from $4.50 to $5.40 (+20%) on 1 Oct 2026; AWS raised Capacity Block prices ~15–20% in 2026 [3][10].
- B200: about $8.01 on Ornn on 24 Sep 2026, up 79% in three months [11]; $9.94 on 8 Nov [1].
- Year on year: +9% across 22 models, H100 +25% (GetDeploying) [2].

**Verification of the founder's claims**

| Claim | Verdict | Evidence |
|---|---|---|
| Cloud GPU prices up ~20% YoY on one index | **Partly confirmed.** No index found showing exactly 20% overall. H100 is +25% YoY, the broad index +9% | [2] |
| B200 rental +31% in one month | **Confirmed (approximately).** Ornn shows +33.1% over one month as of 8 Nov | [1] |
| H100 SXM ~ $3.10 on Ornn | **Confirmed as a recent reading, now stale.** Reported $3.03 on 25 Oct **(secondary source)**; $3.37 on 8 Nov after a +8.7% one-day move | [1] |
| CME futures "launched May 2026" | **Incorrect.** Announced May 2026, targeted 5 Oct, not confirmed live | [6][7] |

### Q15b. Price indexes and data sources

| Source | What it measures | Free | Paid | Best use for a broker |
|---|---|---|---|---|
| **Ornn Compute Price Index** (data.ornn.com) [1] | Daily settled spot price for H100, H200, B200, A100, RTX PRO 6000; also token prices | Latest value, 3 months of daily history, API without key | Full history, hourly data, CSV, forward curves, data-centre map | Headline "market today" number and one-month trend. Bloomberg tickers exist for H100 and B200 |
| **Silicon Data** (silicondata.com) [4] | Daily index for H100, H200, B200, B300, A100, MI300X; basis for CME futures | Headline values and 30-day table on the web page | Portal, full history, API (7-day trial mentioned; price not shown) | Second reference point; shows how wide the range is |
| **GetDeploying GPU Price Index** [2] | Weekly median of public on-demand list prices, 94 providers, 103 models; per-provider price pages | Index page and weekly dataset | Daily and per-provider series via API (price not stated) | Finding which providers list a GPU and at what list price; YoY trend |
| **GPUPerHour** [5] | Live cheapest in-stock on-demand offers, 27 providers for H100 | Yes, free to cite with attribution | none seen | Checking what is actually available right now |
| **SemiAnalysis H100 1-year contract index** [3][9] | Monthly survey of negotiated contract prices | Headline figures appear in public posts | Full data is a paid product **(price unverified)** | The only reference for reserved-deal pricing |
| **Uvik GPU Price Index** [3] | Monthly median list prices, 19 providers | Yes | none | Cross-check; shows min–max range |
| Supplier price pages | Actual list prices | Yes | none | The basis of any real quote |

Caution: many "GPU price guides" in search results are written by vendors (Spheron, GMI, Thunder Compute, RunPod). They are useful for their own prices and unreliable about competitors.

**How to quote fast and credibly (recommended routine)**

1. **Weekly, 30 minutes:** record Ornn and Silicon Data values for H100, H200, B200, and GetDeploying medians, in a simple sheet. After a month this is a private price history the founder can chart in client notes.
2. **On a buyer enquiry, within 24 hours:** send an *indicative range*, not a quote. Example wording: "Indicative only: H100 on-demand is currently about $3.00–$3.40 per GPU-hour on spot indexes (Ornn, Silicon Data, 9 Nov) and $3.70–$5.30 at list. For a 6-month reservation of 32 GPUs expect a negotiated price below list; I will confirm with written supplier offers."
3. **Always convert to a monthly total.** One GPU-month is about 730 hours. 32 H100s at $3.20 is roughly $74,750 per month. Buyers budget in monthly totals, and it makes the commission arithmetic clear.
4. **State what the price excludes:** storage, networking/egress, support tier, taxes, minimum term, prepayment.
5. **Within 2–5 days:** replace the range with two or three written supplier offers side by side, with the index values shown for reference and the date.
6. **Put a validity date on everything.** With moves of 8% in a day on Ornn [1], an indicative range older than a week is misleading.
7. **Never present an index as a price the buyer can get.** Indexes describe small on-demand rentals; a specific cluster in a specific location may cost more, or be unavailable.

### Compute futures: status in brief

- **CME + Silicon Data:** two cash-settled contracts on the H100 and B200 rental indexes, 730 GPU-hours each. Target launch 5 Oct 2026 was missed. The CFTC extended its review to 9 Nov 2026 and sought public comment; CME's notice says the date is to be announced. No confirmed launch found as of today [6][7][12].
- **ICE + Ornn:** announced May 2026; futures based on the Ornn index; no launch date [8].
- **Architect (AX):** already lists perpetual futures on GPU rental prices on a Bermuda-regulated venue, using Ornn data [8]. **Liquid Compute** has applied for a US exchange [12].
- **BGC, ADM Investor Services and others** are preparing to broker these products once approved [13].
- **Relevance to the founder:** none operationally in year one. Dealing in or advising on futures is regulated activity; do not offer it. The useful by-product is that the underlying indexes are public and give buyers a neutral reference.

### Q16. How rising or falling prices affect each revenue model

| | Prices rising (now) | Prices falling |
|---|---|---|
| **Referral % of supplier revenue** | Commission per deal grows with price. But suppliers are sold out, so fewer need a referral partner, programmes may be cut or restricted to large deals, and small customers get deprioritised. Recurring commissions on existing fixed-price contracts do not rise | Commission per deal shrinks, but suppliers have idle capacity and are more willing to pay for customers and to serve small deals. Volume is easier. Customers may renegotiate or leave fixed contracts, cutting recurring commission; clawback clauses matter |
| **Buyer-paid fee** (% of contract or flat) | Buyers value help finding scarce capacity, so a fee is easier to justify. A %-fee rises with price; a flat fee does not. Risk: the founder cannot find capacity and earns nothing for the work, unless part of the fee is a retainer | Capacity is easy to find and prices are public, so buyers question the fee. Value shifts to negotiating renewals downward; a fee tied to savings achieved works better here |
| **Combined (disclosed)** | Works: supplier commission where available, buyer fee where the supplier pays nothing (more common in a tight market) | Works: lean on supplier commission; rebate part to the buyer |
| **Reseller** (rent and re-rent at a markup) | Fixed-price capacity bought earlier gains value, which looks attractive. Requires capital, prepayment and credit risk on the buyer | Dangerous: committed at a high price while the market falls, customers leave or default. This is how small resellers fail. Prices fell for most of 2024–2025 before the current rise, so a reversal is plausible |

Points that hold in both directions:

- **Volatility itself is the opportunity and the risk.** Fast-moving, inconsistent prices make an informed adviser more useful, and make every quote expire quickly.
- **Contract length decides exposure.** A referral commission paid monthly on a 12-month fixed-price contract is insulated from price moves for a year. Prefer suppliers that pay recurring commission on reserved contracts.
- **The current rise may not last.** Ornn's own forward estimates (not traded prices) hold the B200 near today's level for about a year and then fall faster than other GPUs [11]. Plan on today's prices for no more than 6–12 months.

**Recommendation for Q16.** Build income on percentage-based supplier commission from reserved (3–12 month) contracts, add a small flat or retainer-type buyer fee only for searches where no supplier commission exists, and do not resell. In the current rising market, expect fewer but larger commissions per deal and longer search times; track "time to find capacity" as closely as price.

## Questions for a lawyer / accountant

- If the founder shares price indications, forward views or hedging suggestions with clients, at what point could that be treated as regulated commodity or derivatives advice in the US (CFTC rules) or the EU? The working assumption is to give no advice on futures at all.
- Are there licence terms on redistributing Ornn, Silicon Data or GetDeploying figures in client documents or public newsletters? (Check each site's terms; GPUPerHour states free to cite with attribution.)

## Sources

1. Ornn data portal, index values settled 8 Nov 2026 — https://data.ornn.com (checked 2026-11-09)
2. GetDeploying, "GPU Price Trends / GPU Price Index", week of 9 Nov 2026 — https://getdeploying.com/gpu-price-index (checked 2026-11-09)
3. Uvik Software, "GPU Price Index" (data of 7 Oct 2026, updated 2 Nov 2026; also cites SemiAnalysis contract index and Nebius/AWS changes) — https://uvik.net/blog/gpu-price-index/ (checked 2026-11-09)
4. Silicon Data, H100 index page (SDH100RT) with other index values — https://www.silicondata.com/products/silicon-index/h100 (checked 2026-11-09)
5. GPUPerHour, H100 rental page — https://gpuperhour.com/rent/h100 (checked 2026-11-09)
6. Finance Magnates, "CFTC Plans AI Compute Derivatives Consultation as CME Targets October 5" — https://www.financemagnates.com/institutional-forex/cftc-plans-ai-compute-derivatives-consultation-as-cme-targets-october-5/ (checked 2026-11-09, via search summary)
7. Ironbeam status note on CME compute futures (dated 6 Oct 2026) — https://www.ironbeam.com/?p=11169 ; Cointelegraph — https://cointelegraph.com/news/cftc-ai-compute-futures-cme-october-launch (checked 2026-11-09, via search summary)
8. Yahoo Finance, "ICE and Ornn to launch GPU compute futures contracts" — https://finance.yahoo.com/markets/options/articles/ice-ornn-launch-gpu-compute-142609556.html ; The Next Web — https://thenextweb.com/news/ice-nyse-compute-futures-market-gpu-ai (checked 2026-11-09, via search summary)
9. SemiAnalysis, "The Great GPU Shortage – Rental Capacity – Launching our H100 1 Year Rental Price Index" — https://newsletter.semianalysis.com/p/the-great-gpu-shortage-rental-capacity ; secondary report of later figures — https://fourweekmba.com/ai-patels-data-puts-nvidia-h100-rent-up-65-in-a-year-at-2-80/ (checked 2026-11-09, via search summary)
10. AI Weekly, "AWS Raises EC2 GPU Capacity Block Prices 20% From July 1" — https://aiweekly.co/alerts/aws-raises-ec2-gpu-capacity-block-prices-20-from-july-1 (checked 2026-11-09, via search summary)
11. Data Gravity (Chris Zeoli), "The GPU depreciation curve is broken" (25 Sep 2026) — https://www.datagravity.dev/p/the-gpu-depreciation-curve-is-broken (checked 2026-11-09)
12. Newcomer, "Compute crunch: startups aim to financialize" (2 Nov 2026, paywalled preview) — https://www.newcomer.co/p/compute-crunch-startups-aim-to-financialize (checked 2026-11-09)
13. Crypto Briefing, "Commodity brokers gear up to trade AI compute futures as CFTC review continues" — https://cryptobriefing.com/commodity-brokers-prepare-ai-compute-futures/ (checked 2026-11-09, via search summary)
