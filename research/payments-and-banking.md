# Payments and banking: how to get paid (Q28)
_Last checked: 2026-11-09_

> Research only. Provider eligibility lists change without notice. Nothing was applied for or signed up to. Items not confirmed on the provider's own page are marked **(unverified)**.

## Summary

- **Get paid by bank transfer against an invoice.** Supplier commissions and buyer broker fees should arrive by wire, ACH or SEPA into an account in the LLC's name. That is all this business needs at the start.
- **Relay is the best-verified option.** Relay's own prohibited-countries list (updated 11 Aug 2026) does not include Montenegro (it does include Bosnia and Herzegovina) [1].
- **Mercury probably works, but I could not read its official list.** Mercury's help page blocked automated access. Two third-party copies of the list (one checked 23 Sep 2026) show 48 countries including Albania, Bosnia and Croatia, but not Montenegro [2][3]. One undated guide claims Montenegro is restricted [4]. Check Mercury's own "Prohibited countries" page yourself before applying.
- **Wise looks doubtful.** Wise's official list of countries where you must live to hold money does not include Montenegro [5]. Whether a US-registered LLC with a Montenegro-resident owner can still open Wise Business is **(unverified)**.
- **Stripe:** Montenegro is not a Stripe country [6], but a US LLC opens a *US* Stripe account, and Stripe asks non-US-resident representatives for an ID document instead of a US SSN/ITIN [7]. You do not need Stripe for the first six months.
- **Never hold or forward buyer money meant for a supplier.** Under FinCEN rules, accepting funds from one person and sending them to another is money transmission, with no minimum threshold, federal registration and state licences [8][9]. Buyers pay suppliers directly; you receive only your own fee or commission.
- **Do not accept crypto.** Do not accept payment from anyone other than the company you verified and contracted with.
- **Recommended setup:** one US business account (Relay or Mercury), invoices from simple invoicing software, wires/ACH/SEPA only, a personal Montenegrin bank account to receive owner distributions, and a payment log.

## Details

### Q28.1 — Which accounts can a non-resident-owned US LLC with a Montenegro-resident founder open?

| Provider | What it is | Montenegro-resident owner? | Evidence |
|---|---|---|---|
| **Relay** | US business banking via partner bank (Thread Bank) | **Not on the prohibited list** (31 countries; Bosnia and Herzegovina is listed, Montenegro and Serbia are not). List "can change without notice" | Official help page, updated 11 Aug 2026 [1] |
| **Mercury** | US business banking via partner banks | **Probably eligible (unverified).** Rule is based on country of residence. Third-party copies of the list do not include Montenegro; official page not readable today; one undated guide says restricted | [2][3][4]; official page [10] returned an access error |
| **Wise Business** | Multi-currency account with USD/EUR details (not a bank) | **Doubtful (unverified).** Montenegro is not on Wise's list of residence countries for holding money. How this applies to a US-registered LLC with a foreign owner is not stated | Official help page [5] |
| **Airwallex** | Multi-currency business account | **Unverified.** US-registered businesses are supported; the page read does not state owner-residence limits and says other criteria apply | Official help page [11] |
| **Payoneer** | Receiving accounts (USD/EUR), not a deposit bank | **Unverified.** Third-party lists show Montenegro as supported; Payoneer's own country page was not confirmed. Unclear whether you would register as the US LLC or as a Montenegrin resident | [12] |
| **Revolut Business** | EU/UK/US business account | **Probably not (unverified).** Search results indicate the applicant must live in a supported country (EEA, UK, Switzerland, US and a few others); Montenegro not seen. Official page not readable today | [13] |
| **Montenegrin bank** | Local EUR account | For you personally: yes. For the US LLC as a foreign company: possible but paperwork-heavy **(unverified)**. Montenegro has been in SEPA since 6 Oct 2025, so EUR transfers from the EU are cheap and fast | Central Bank of Montenegro [14] |

Honest caveats:
- Fintech "banks" de-risk quickly. Mercury off-boarded founders in a batch of countries in 2024 with short notice [15]. Western Balkan neighbours (Albania, Bosnia, Croatia) are already on Mercury's list. Plan for a second account as a backup once money flows.
- All of them will ask for: LLC formation documents, EIN letter, passport, proof of address, a description of the business, expected volumes, and a website. "GPU brokerage" involving export-controlled hardware and international counterparties will draw compliance questions. Describe it accurately: a referral/brokerage service that earns commissions and never handles customer funds.
- Do not use a nominee, a friend's address, or a false country of residence to get through onboarding. That is misrepresentation to a financial institution and will end in a frozen account.

### Q28.2 — Stripe

- Stripe's country list does not include Montenegro or Serbia [6]. That list is about where the *business* is established. A US LLC applies for a US Stripe account.
- Stripe's US verification rules: SSN/ITIN is collected from US-resident representatives and owners; non-US-resident representatives provide a national ID or verification document at onboarding [7].
- You will still need the EIN and a US bank account for payouts. Whether Stripe approves a specific Montenegro-resident representative is decided at review **(unverified)**.
- Do you need it? Not at first. Card payments cost a percentage of each payment, can be charged back months later, and make it harder to confirm who actually paid. For a few large B2B invoices, bank transfer is cheaper and cleaner. Consider Stripe invoicing later only for small buyer fees.

### Q28.3 — Rails and invoicing

| Flow | Typical payer | Rail | Notes |
|---|---|---|---|
| Supplier commission | US or EU cloud provider | ACH or domestic wire (US); SWIFT wire or SEPA (EU) | Supplier will ask for a W-8BEN (see `finance/tax-notes.md`) and bank details on letterhead. Expect net-30 to net-60 terms |
| Buyer-paid broker fee | Buyer company | Wire / ACH / SEPA against invoice | Invoice only your fee, never the compute cost |
| Owner distribution | LLC → you | International wire to your personal Montenegrin account | Reportable on Form 5472; declare in Montenegro |

Receiving EUR: a US account at Relay or Mercury receives SWIFT wires; a local EUR IBAN (cheaper for EU buyers) needs Wise, Airwallex or Payoneer if one of them accepts you **(unverified)**.

Invoice contents: LLC legal name, address and EIN; customer's legal name, address and VAT number (EU); a clear description ("brokerage fee for introduction to [supplier], order ref X"); amount and currency; bank details; for EU business customers the reverse-charge note; invoice number and date. Send bank details as a PDF and confirm them by a second channel — invoice-redirection fraud is common.

### Q28.4 — Payment-compliance implications

**1. Never touch the buyer's money for the supplier.**
FinCEN defines a money transmitter as a person who accepts funds from one person and transmits them to another person or location, or any other person engaged in the transfer of funds [9]. There is **no activity threshold** for money transmitters; a money services business must register with FinCEN (Form 107) within 180 days of being established and renew every two years [8]. Most US states also require their own money-transmitter licence, which costs far more than your whole budget **(state detail unverified)**; operating an unlicensed money transmitting business is a federal crime (18 U.S.C. §1960) [16].

The regulation has narrow exclusions — for example a payment processor working through a clearing system under an agreement with the seller, or someone who moves funds only as an integral part of selling their own goods or services [9]. A broker collecting a buyer's GPU payment and passing it to a supplier does not obviously fit either. Do not build a business on an exclusion without a US payments lawyer's written opinion.

Other reasons: your bank will close the account if it sees pass-through flows; you would carry the loss if a supplier fails to deliver; and holding the money makes you a party to the sale, which increases your export-control and sanctions responsibility.

Rule: **the buyer contracts with and pays the supplier directly. You invoice only your own commission or fee.** No escrow, no "pay us and we pay them", no netting your fee out of buyer funds.

**2. Do not accept crypto.**
- You cannot reliably tie a wallet to the company you verified, which breaks the "payer = KYC'd customer" rule.
- In a business touching export-controlled GPUs, a request to pay in crypto is a classic sign that someone wants to hide who or where they are. Treat the request as a reason for extra checks or refusal.
- US-facing fintech banks often restrict or close accounts with crypto-exchange flows **(unverified per provider)**.
- It adds tax and bookkeeping work in two countries.

**3. Third-party payer rule.**
Accept payment only from a bank account in the name of the company you verified and signed with, in a country consistent with what they told you. Refuse and return (to the same account) payments from: an unrelated company, an individual's personal account, a payment agent or exchange house, or a country that does not match the customer. A different payer than the customer is a standard red flag for sanctions evasion, diversion and money laundering. If a buyer says "our partner in another country will pay", stop and escalate to your compliance checklist.

**4. Match payer to the KYC file.** For each receipt record: invoice number, payer name on the bank statement, payer bank country, date, amount, and a tick that it matches the verified customer. If it does not match, do not perform further services until resolved.

**5. Screen before invoicing.** Sanctions/denied-party screening of the customer and its owners belongs in onboarding (see the compliance files). Never invoice an entity you have not screened. As a US LLC, you are a US person for OFAC purposes regardless of where you live.

**6. Record keeping.** Keep contracts, invoices, bank statements, W-8 forms, KYC files and screening results. IRS rules require books that support Form 5472 [17]; export and sanctions rules have their own multi-year retention periods (see compliance files). A simple rule: keep everything for at least seven years **(my conservative suggestion; confirm)**. Keep business and personal money strictly separate — one account for the LLC, and move money to yourself only as recorded owner distributions.

### Q28.5 — Methods to avoid

| Method | Why avoid |
|---|---|
| Holding / forwarding buyer funds, escrow | Money transmission: FinCEN registration, state licences, criminal exposure [8][9][16] |
| Crypto, stablecoins | Payer cannot be matched to KYC; evasion red flag; bank de-risking |
| Cash, money orders, Western Union-style transfers | No reliable payer identity |
| Payments from third parties or personal accounts | Sanctions / laundering red flag |
| PayPal, personal Wise/Revolut, your personal bank account for business income | Mixes personal and LLC funds; weak payer records; breaks the LLC's separation; complicates tax in both countries |
| Card payments for large invoices | Fees and chargeback risk; weaker payer verification |
| "Rent-an-account", nominee directors, false residence address | Misrepresentation to a bank; account seizure risk |
| Commission splits paid to unknown intermediaries | Bribery and diversion risk; also creates US "agent" tax questions |

### Recommended setup (cost: near zero)

1. **Read Mercury's and Relay's prohibited-country pages yourself**, then apply to Relay (best verified) and/or Mercury. Both advertise no monthly fee on basic plans **(unverified today)**.
2. **Backup:** once the first account is open, try one multi-currency provider (Airwallex or Payoneer) for EUR receiving details, if they accept you.
3. **Invoicing:** the bank's built-in invoicing or a free invoicing tool; numbered PDFs; bank transfer only.
4. **Contracts:** every agreement states that the buyer pays the supplier directly and that you never receive customer funds.
5. **Payment log:** a spreadsheet matching every receipt to an invoice and a verified customer.
6. **Distributions:** pay yourself by wire to your personal Montenegrin account, labelled as an owner distribution, and record each one for Form 5472.
7. **Postpone Stripe and all card acceptance** until there is a real need.

## Questions for a lawyer / accountant

1. (US payments lawyer, only if the model ever changes) If a supplier or buyer insists that I collect the full purchase price, does any FinCEN exclusion apply, and which state licences would be triggered?
2. (US accountant) Do supplier commissions paid by ACH into the LLC's US account change the "foreign-source income" analysis? (It should not — source follows where the work is done — but confirm.)
3. (Montenegrin accountant) How do I declare owner distributions received from the LLC into my Montenegrin account, and are there foreign-account reporting duties for a resident who controls a US bank account?
4. (Montenegrin accountant / bank) Can the US LLC open a non-resident company account at a Montenegrin bank, and would doing so strengthen the argument that the LLC is managed from Montenegro?

## Sources

1. Relay, Prohibited Countries (updated 11 Aug 2026) — https://relayfi.com/hc/en-us/articles/10239600121748-Prohibited-Countries/ — checked 2026-11-09
2. BizStartz, "Mercury Prohibited Countries: Full List" (list checked 23 Sep 2026; third-party) — https://bizstartz.com/mercury-prohibited-countries/ — checked 2026-11-09
3. My Latin Life on X, copy of Mercury's prohibited list (third-party) — https://x.com/MyLatinLife/status/2040057895824294196 — search result seen 2026-11-09
4. Subhan Law help guide, "U.S. Bank Account" (undated; claims Montenegro restricted at Relay/Mercury/Wise) — https://subhan-law.gitbook.io/help-guide/company-formation/u.s.-bank-account — search summary seen 2026-11-09
5. Wise, "Where do I need to live to hold money with Wise?" — https://wise.com/uk/help/articles/2813542/where-do-i-need-to-live-to-hold-money-with-wise — checked 2026-11-09
6. Stripe, Global availability — https://stripe.com/global — checked 2026-11-09
7. Stripe Support, 2024 updates to US verification requirements FAQ — https://support.stripe.com/questions/2024-updates-to-us-verification-requirements-faq — checked 2026-11-09
8. FinCEN, Money Services Business Definition — https://www.fincen.gov/money-services-business-definition — checked 2026-11-09
9. 31 CFR §1010.100(ff)(5), definition of money transmitter and exclusions — https://www.law.cornell.edu/cfr/text/31/1010.100 — checked 2026-11-09
10. Mercury, Prohibited countries (official; not readable by automated fetch) — https://support.mercury.com/hc/en-us/articles/28771710754580-Prohibited-countries — access error 2026-11-09
11. Airwallex Help, supported countries for business registration — https://help.airwallex.com/hc/en-gb/articles/4408591334937 — checked 2026-11-09
12. Smartcat help, Payoneer availability list (third-party) — https://help.smartcat.com/1674961-payoneer — search summary seen 2026-11-09
13. Revolut Business Help, eligible countries of residence (official; not readable by automated fetch) — https://help.revolut.com/en-SG/business/help/setting-up-an-account/is-my-business-eligible/what-country-of-residence-is-eligible-to-open-a-revolut-business-account — access error 2026-11-09
14. Central Bank of Montenegro, "Montenegro becomes an operational member of SEPA" (Oct 2025) — https://cbcg.me/en/public-relations/news/press-releases/montenegro-becomes-an-operational-member-of-sepa-first-transactions-from-tomorrow-faster-cheaper-and-safer-international-euro-payments — search summary seen 2026-11-09
15. TechCrunch, Mercury restricts founders in several countries (23 Jul 2024) — https://techcrunch.com/2024/07/23/mercury-bank-fintech-sanctions-ukraine-nigeria — search summary seen 2026-11-09
16. 18 U.S. Code §1960, prohibition of unlicensed money transmitting businesses — https://www.law.cornell.edu/uscode/text/18/1960 — statute cited from general knowledge; text not re-read 2026-11-09
17. IRS, Instructions for Form 5472 — https://www.irs.gov/instructions/i5472 — checked 2026-11-09
