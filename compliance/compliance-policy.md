# Compliance policy
_Version 1 (draft for lawyer review) — 2026-11-09_

This is the plain-language policy I follow on **every** deal. It is deliberately stricter than the law in several places, because a one-person brokerage cannot afford a borderline case. It is based on the research in `research/export-controls.md`, `research/enforcement-cases.md`, `research/sanctions-and-screening.md`, `research/eu-uk-local-rules.md` and `research/gdpr-and-data-residency.md`. It is not legal advice and must be reviewed by a US export/sanctions lawyer (see `legal/questions-for-lawyer.md`).

## 1. Why this applies to me
- My LLC is a **US person** for both export controls (EAR) and sanctions (OFAC), even though I live in Montenegro.
- Sanctions liability is **strict**: I can be fined without knowing a party was sanctioned. Simply introducing two parties can count as prohibited "facilitation".
- "Knowledge" under US export law includes **willful blindness**: being aware of a high probability and choosing not to ask. Not asking is not a defence.
- Penalties are personal: civil fines of roughly $375,000 per violation or twice the deal value; criminal penalties up to $1 million and 20 years for willful violations.
- Montenegro's Law on Restrictive Measures binds me personally as well, and Montenegro follows EU sanctions. The EU specifically bans providing GPU-as-a-service to Russian entities.

## 2. The rules

**Rule 1 — No screening, no introduction.** I do not introduce a buyer to a supplier, or share one party's details with the other, until the KYC checklist (`kyc-checklist.md`) is complete and saved.

**Rule 2 — Refuse list.** I refuse any deal where the buyer, end user, payer, supplier, or any owner or controller of them:
- appears on a US, EU, UK, UN or Montenegrin restricted-party list, or is 50% or more owned by listed persons;
- is located in, headquartered in, or ultimately owned or controlled from: **China, Hong Kong, Macau, Russia, Belarus, Iran, North Korea, Cuba, Syria, Venezuela, or the occupied regions of Ukraine** (Crimea, Donetsk, Luhansk);
- wants compute for military, intelligence, weapons, mass-surveillance or defence-research purposes (allied-government work goes to a lawyer first);
- will not say who owns them, who the end user is, where users are, or what the workload is.

> Note: Syria is no longer under a comprehensive US sanctions programme, and Belarus and Venezuela rules were partly eased in 2026. I still refuse them at this stage. Revisiting any of these needs a lawyer's written advice first.

**Rule 3 — Lawyer first.** I pause and get legal advice before going further when:
- a buyer is incorporated in a neutral country but has founders, investors or a parent linked to a refuse-list country;
- the buyer, end user or data centre is in a diversion-risk hub (for example Malaysia, Singapore, Thailand, Indonesia, Vietnam, UAE, Saudi Arabia, Turkey, Central Asia, the Caucasus);
- the buyer is a Serbian company with any Russian ownership, funding or customers (Serbia does not apply EU sanctions on Russia, so extra care is needed);
- the deal is unusually large for a company with no track record, especially one formed after October 2022;
- anyone asks about moving model weights to, or giving access to users in, a refuse-list country;
- I later learn that a past deal may have involved a restricted party.

**Rule 4 — Compute time only.** I never buy, hold, ship, store, relabel or re-invoice physical GPUs or servers. Every US criminal case found involved physical hardware and a middleman.

**Rule 5 — I never touch the buyer's money for the supplier.** The buyer contracts with and pays the supplier directly. I am paid my commission or fee separately. Holding or passing on funds could make me a money transmitter.

**Rule 6 — Clean payments only.** I accept bank transfer from an account in the name of the company I screened. No crypto, no cash, no third-party payers, no payments from a country unrelated to the customer.

**Rule 7 — Red flags.** I use `red-flags.md` on every deal. One unresolved red flag: pause and ask in writing. Two: refuse. I do not help a customer "fix" an answer.

**Rule 8 — No workarounds, ever.** I do not suggest, design or go along with any structure meant to hide an end user, owner, location or payer, or to get around export controls, sanctions or a supplier's KYC. If someone asks me to, the deal is over.

**Rule 9 — Vet suppliers too.** Every supplier passes the due-diligence checklist in `research/supplier-verification.md`, is screened like a buyer, and has no capacity in a refuse-list country. I prefer suppliers that run their own KYC on my buyers.

**Rule 10 — Honest about what I am.** I always tell the buyer in writing that I may earn a supplier commission, and that I am not the provider. I never promise data residency, sovereignty or supplier performance; I pass on the supplier's written commitments and say where they come from.

**Rule 11 — Records.** For every deal, accepted or refused, I keep a dated folder with: intake form, KYC documents, screening screenshots/PDFs, ownership notes, emails, contracts and the decision. I keep it **10 years** (the OFAC record-keeping period). KYC data is stored securely and used only for compliance.

**Rule 12 — Re-screen.** I re-screen all active buyers and suppliers monthly and whenever ownership, payer or end use changes.

**Rule 13 — Stay current.** I check for rule changes on the first working day of each month (BIS, OFAC, EU sanctions, the Remote Access Security Act, any new US AI chip rule) and update this policy. Next scheduled check: 2026-12-01.

**Rule 14 — When in doubt, stop.** If I suspect a past or current deal involved a violation, I stop work on it, change nothing in the records, and speak to a lawyer about voluntary self-disclosure before doing anything else.

## 3. What is generally fine (after screening)
- Buyers headquartered and owned in the US, EU/EEA, UK, Switzerland, Canada, Japan, Australia and similar allied countries, using capacity located in those countries.
- Western Balkans buyers with transparent local ownership, a real business and an ordinary commercial or research workload.
- Universities and startups I can verify from public records.
- Referral deals where the supplier contracts directly with the buyer and runs its own KYC.

## 4. Open points for the lawyer
The uncertain points behind this policy are listed in `legal/questions-for-lawyer.md` (section "Compliance questions"). The most important: whether a referral role counts as "support" under EAR §744.6, how deep ownership checks must go, and how to access the Montenegrin register of designated persons.
