# KYC and end-user due-diligence checklist
_Version 1 (draft for lawyer review) — 2026-11-09_

Run this on **every buyer before any introduction**, and the supplier part on every supplier before the first referral. Save everything in the deal folder. If a step cannot be completed, the deal does not proceed. Sources: see `research/sanctions-and-screening.md` and `research/export-controls.md`.

## Step 1 — Collect (from the buyer)
- [ ] Completed intake form (`buyers/intake-form.md`)
- [ ] Full legal name, registration number, country and date of incorporation
- [ ] Registered address and real operating address
- [ ] Company register extract (or a link to the official register entry)
- [ ] Website, and LinkedIn pages of the company and my contact
- [ ] Owners down to natural persons holding 25% or more, plus anyone who controls the company; country of **ultimate parent / headquarters**
- [ ] Directors' names
- [ ] Who the **end user** is (if different from the buyer) and their country
- [ ] What the workload is, in plain words (for example "fine-tuning an open-source language model for legal documents")
- [ ] Where the people using the GPUs will log in from
- [ ] Who will pay, from which bank and country
- [ ] Signed end-use statement: no military/intelligence/weapons use, no users or beneficiaries in restricted countries, no resale without telling me

## Step 2 — Verify (myself, from independent sources)
- [ ] Company exists in the official register (for example Serbia APR, Montenegro CRPS, UK Companies House, OpenCorporates)
- [ ] Incorporation date noted — formed after October 2022 or just before the deal is a flag
- [ ] Website and LinkedIn show a real business that plausibly needs GPUs; staff are real people
- [ ] Email domain matches the company
- [ ] Address is not a virtual office, residence or freight forwarder (map check)
- [ ] Ownership traced as far as public records allow; ultimate parent country confirmed
- [ ] News search: company name and owners + "sanctions", "export", "fraud", "China", "Russia"
- [ ] A video call held with a named person from the company

## Step 3 — Screen (free official tools)
Screen the **company, owners, directors, end user and payer**. Try spelling variants.
- [ ] US Consolidated Screening List — trade.gov/consolidated-screening-list (covers OFAC SDN plus BIS Entity List, Military End User, Unverified and Denied Persons lists)
- [ ] OFAC Sanctions List Search — sanctionssearch.ofac.treas.gov
- [ ] EU consolidated sanctions list — sanctionsmap.eu
- [ ] UK Sanctions List — search-uk-sanctions-list.service.gov.uk
- [ ] UN Security Council consolidated list
- [ ] Montenegro register of designated persons (access method still to be confirmed with a local lawyer)
- [ ] For each search: save a dated screenshot or PDF showing the name searched and the result
- [ ] Any possible match investigated and resolved **in writing** (different date of birth, address, etc.). An unresolved match means refuse.

> OpenSanctions is useful for a broader search, but it is not free for business use (about €0.10 per check via its API). Consider it once deal volume grows.

## Step 4 — Decide
- [ ] Checked against the refuse list in `compliance-policy.md` (Rule 2)
- [ ] Checked against `red-flags.md`; each flag noted with its resolution
- [ ] "Lawyer first" situations (Rule 3) escalated
- [ ] Decision recorded with date: **Proceed / Pause for information / Lawyer / Refuse**, with one sentence of reasoning
- [ ] `buyers/pipeline.csv` updated (`kyc_status`, `screening_date`)

## Step 5 — At contract and payment
- [ ] Re-screen buyer and payer on the day the contract is signed
- [ ] Buyer signs the service agreement with compliance representations (`legal/buyer-service-agreement-outline.md`)
- [ ] Supplier is told who the buyer and end user really are — nothing is withheld
- [ ] When I am paid: the payer's name and bank country match the screened entity

## Step 6 — Ongoing
- [ ] Monthly re-screen of every active buyer and supplier
- [ ] Re-run Steps 1–4 if ownership, end user, workload, user location or payer changes
- [ ] Keep the deal folder for 10 years

## Supplier version
- [ ] Legal entity, register extract, owners and ultimate parent country (Steps 1–3 as for a buyer)
- [ ] Data-centre locations confirmed, none in a refuse-list country
- [ ] How the supplier obtained its GPUs (NVIDIA partner status, named OEM or distributor)
- [ ] Supplier confirms it runs KYC on customers and does not serve restricted parties
- [ ] Full technical and commercial checks from `research/supplier-verification.md`

## What I do not do
- I do not accept "our lawyer says it is fine" in place of documents.
- I do not rely only on the supplier's KYC; I run my own.
- I do not coach a buyer on how to answer.
