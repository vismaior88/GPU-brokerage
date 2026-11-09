# Buyer intake form (Q12)
_Last checked: 2026-11-09_

## Summary

- Purpose: collect everything needed to (a) get supplier quotes within 48 hours and (b) run KYC / end-use screening **before** any supplier is named.
- Paste into Google Forms or Tally. Field types are in brackets. `*` = required.
- Two parts: **Part A** (5 minutes, enough for an indicative price range) and **Part B** (needed before a firm quote or introduction). Keeping Part A short raises completion.
- Rule: **no firm quote and no supplier introduction until Part B is complete and screening is passed.** If a buyer will not name the end user or end use, the deal stops. See `/compliance/kyc-checklist.md` and `/compliance/red-flags.md`.
- The KYC questions here are a practical draft. The compliance files are the authority; have a qualified lawyer confirm the list.

## Form intro text (paste at the top)

> Thanks for your interest. I am an independent broker: I find GPU capacity from cloud providers and data centres that fits your needs. I do not own or operate the hardware; your contract for compute is with the provider.
> **Disclosure:** I may be paid a referral commission by the provider. If I charge you any fee, I will tell you the amount in writing before you commit.
> Because advanced GPUs are subject to export-control and sanctions rules, I ask every customer the same identity and end-use questions. I cannot quote without them.
> Your answers are used only to source and screen this request and are shared with a provider only after you agree.

## Part A — Quick request (indicative range)

**A1. Contact**
1. Full name * [short text]
2. Work email * [email] — _free webmail addresses will need extra verification_
3. Role / title * [short text]
4. Company / organisation name * [short text]
5. Company website * [URL]
6. Country where the company is registered * [dropdown: country list]
7. LinkedIn profile (optional) [URL]

**A2. Workload**
8. What will you run? * [multiple choice] Training from scratch / Fine-tuning / Inference (production) / Batch inference or data processing / Research experiments / Rendering or simulation / Other
9. Describe the workload in 1–3 sentences (model type and size, framework) * [long text]
10. What does the product or project do, and for which industry? * [long text]

**A3. Capacity**
11. GPU type * [checkboxes] H100 / H200 / B200 / GB200 / L40S / A100 / RTX-class / AMD / Not sure — advise me / Other
12. Would you accept an alternative GPU if cheaper or available sooner? * [Yes / No / Depends]
13. Number of GPUs * [number] — or range, min–max
14. Start date * [date] and how flexible? [Fixed / ± 1 week / ± 1 month]
15. Duration * [multiple choice] Under 1 week / 1–4 weeks / 1–3 months / 3–6 months / 6–12 months / 12+ months / Not sure
16. Commitment type * [multiple choice] On-demand (pay as you go) / Reserved (commit for the term) / Either
17. Usage pattern [multiple choice] 24/7 / Bursts / Not sure

**A4. Location**
18. Where must the hardware be located? * [checkboxes] EU / EEA only / A specific country: ____ / UK / US / No requirement
19. Reason for the location requirement [checkboxes] GDPR / personal data / Customer contract / Sector regulation (health, finance, public) / Latency / Preference / None

**A5. Budget**
20. Budget * [multiple choice] Target price per GPU-hour: ____ / Total budget: ____ / Monthly budget: ____ / No budget set yet
21. Currency [USD / EUR / other]
22. What are you using today, and roughly what do you pay? [long text] — _helps me avoid offering something worse_
23. Do you have cloud credits or a public compute allocation (e.g. EuroHPC AI Factories, a national platform)? When do they end? [long text]

## Part B — Details for a firm quote and screening

**B1. Technical**
24. Deployment type * [multiple choice] Bare metal / Virtual machines / Managed Kubernetes / Slurm cluster / No preference
25. Do the GPUs need to work as one cluster (multi-node training)? * [Yes / No / Not sure]
26. Networking between nodes [multiple choice] InfiniBand required / High-speed Ethernet (RoCE) fine / Not needed / Not sure
27. Storage: how much, and what kind? [short text] e.g. "20 TB NVMe, shared file system"
28. Data volume to move in/out, and from where? [short text] — _egress fees matter_
29. CPU / RAM / other requirements [short text]
30. Support and SLA needs [checkboxes] Best effort is fine / Uptime SLA required / 24/7 support / Named engineer
31. Security / compliance requirements [checkboxes] ISO 27001 / SOC 2 / GDPR data processing agreement / Single-tenant (no sharing) / Sector-specific: ____ / None
32. Will personal data or other sensitive data be processed? * [Yes / No] If yes, what kind? [short text]
33. Do you need test access or a benchmark before committing? [Yes / No]

**B2. Commercial**
34. Who signs the contract and who approves the spend? * [short text]
35. Decision date * [date]
36. Payment terms you can accept * [checkboxes] Prepayment (monthly) / Prepayment (full term) / Invoice net 15 / Invoice net 30 / Card
37. Payment method * [multiple choice] Bank transfer from a company account in the company's name / Company card / Other: ____ — _I do not arrange deals paid in cash, crypto, or by unrelated third parties_
38. Which providers have you already contacted or received quotes from? * [long text] — _so I do not duplicate or conflict with an existing conversation_
39. Is anyone else (another broker or reseller) sourcing this request? [Yes / No]

**B3. Identity and ownership (KYC)**
40. Full legal entity name * [short text]
41. Registration number and register (e.g. APR, Companies House) * [short text]
42. Registered address * [long text]
43. Operating address, if different [long text]
44. Year founded * [number]
45. Parent company and ultimate parent, with countries * [long text] — write "none" if independent
46. Beneficial owners holding 25% or more: full name, nationality, country of residence, % * [long text]
47. Directors / managers: full names * [long text]
48. Is the company, any owner or any director owned or controlled by a government, or by a person or company headquartered in China (incl. Hong Kong, Macau), Russia, Belarus, Iran, North Korea, Cuba or Syria? * [Yes / No] If yes, explain [long text]
49. Is the company, any owner, director or the end user on any sanctions or export restricted-party list (e.g. OFAC SDN, BIS Entity List, EU or UK sanctions lists)? * [Yes / No / Not sure]
50. How is the company funded? [multiple choice] Revenue / Venture capital (name main investors) / Grants / Parent company / Other

**B4. End user and end use**
51. Who will actually use the compute? * [multiple choice] Our company only / Our customer(s) / A parent or affiliate / Other
52. If not your company only: full legal name, country and website of each end user * [long text]
53. From which countries will people log in to and operate the compute? * [long text]
54. What is the end use? Be specific: what will be trained or run, for what product or purpose? * [long text]
55. Will the compute be used, directly or indirectly, for any military, intelligence, weapons, surveillance or nuclear purpose, or for any military or government end user? * [Yes / No] If yes, explain [long text]
56. Will you resell, sublease or give access to any third party? * [Yes / No] If yes, to whom? [long text]
57. Will model weights, outputs or access be provided to any party in the countries listed in question 48? * [Yes / No]

**B5. Declarations** [checkboxes, all required]
58. ☐ The information above is true and complete, and I will tell you if it changes.
59. ☐ I understand you are a broker, not the compute provider, and that you may receive a commission from the provider.
60. ☐ I understand that you and the provider may carry out sanctions and export-control screening and may decline the request without giving a reason.
61. ☐ I agree that you may share this information with providers you propose for this request, after I confirm each provider.
62. ☐ I am authorised to submit this request for the company named above.

Name, title, date * [short text]

## How to use the answers (internal notes, do not paste into the form)

- **Quote speed:** Part A is enough to give an indicative range from price indexes within 24–48 hours. Label it "indicative, not an offer, capacity not held".
- **Minimum for a supplier request:** Q8–19, 24–27, 30–31, 35–36.
- **Stop and escalate** (see `/compliance/red-flags.md`): "Yes" or "Not sure" on Q48, Q49, Q55, Q57; blank or vague Q52–54; payment by third party or crypto; webmail address with no verifiable company; great urgency with no interest in price; location or login countries that do not match the company's story.
- **Verify, do not just collect:** check the company register, website, LinkedIn, and screen the entity, owners, directors and end users against restricted-party lists (process in the compliance files). Record the date in `pipeline.csv` → `screening_date`.
- **Re-screen** before any contract is signed and if the end user or ownership changes.
- **Privacy:** the form collects personal data (names, nationality of owners). Store it securely, keep it only as long as needed, and add a short privacy notice. Confirm GDPR requirements with a lawyer.
- Log every submission in `/buyers/pipeline.csv`.
