# Supplier outreach templates
_Last checked: 2026-11-09_

Drafts for the founder to edit and send personally. Nothing has been sent.

## Rules for every message

- Tell the truth: new, one-person brokerage; no track record yet. Do not claim customers, pipeline or volume you do not have.
- Never name a specific buyer to a supplier before (a) the buyer agrees and (b) the buyer has passed screening.
- Do not promise deal volume. Do not ask for exclusivity.
- Say plainly that you screen buyers (KYC, sanctions, export controls). Serious suppliers value this.
- Keep it under 150 words. One clear ask.
- Fill every `[bracket]`. Delete any sentence that is not true for you on the day you send it.

---

## 1. First contact — email

**Subject:** Referral partner enquiry — [Your LLC name]

Hi [Name],

I run [Your LLC name], a new, one-person GPU capacity brokerage (US LLC; I am based in Montenegro). I help AI startups and research teams in Europe, with a focus on South-East Europe, find capacity that fits their needs.

I am early: I have no closed deals yet, and I would rather say so than oversell. I do not resell or take payment for compute — the customer contracts with you directly. I screen every buyer (identity, ownership, end use, sanctions and export-control lists) before making an introduction.

Three questions:
1. Do you have a referral or partner programme, and can a small new partner join?
2. How do you register a referred deal so it is attributed correctly?
3. What is the smallest deal (GPUs / term) your sales team will handle?

Happy to do a 15-minute call if easier.

Thanks,
[Name]
[Your LLC name] · [website] · [LinkedIn]

---

## 2. First contact — LinkedIn connection note (max 300 characters)

Hi [Name] — I run a new one-person GPU brokerage serving AI teams in Europe / SE Europe. I'd like to learn whether [Supplier] works with referral partners and how deals are registered. No pitch — just two questions. Thanks, [Name]

**After they accept (message):**

Thanks for connecting. Short version: I introduce screened buyers (mostly 8–64 GPUs, 1–12 months, often needing EU hosting) and the customer contracts directly with the provider. I'm new and have no deal history yet. Does [Supplier] have a partner or referral programme, and who is the right person to ask about terms and deal registration?

---

## 3. Follow-up (5–7 working days later, once only; a second follow-up after two more weeks at most)

**Subject:** Re: Referral partner enquiry — [Your LLC name]

Hi [Name],

Following up on my note below. If partnerships are handled by someone else, I'd be grateful for the right contact.

In case it helps: I am not asking for exclusivity or special pricing — only to understand whether you accept referred customers from a small broker, and how to register them.

If it is not a fit right now, a one-line "no" is fine and I will not write again.

Thanks,
[Name]

---

## 4. Partner-programme application email

Use when the supplier has a public programme with an application address or form. Check their terms first and attach nothing you have not read.

**Subject:** Partner programme application — [Your LLC name]

Hi [Partner team / Name],

I would like to apply to the [Supplier] [referral / partner] programme.

**About the business**
- Legal entity: [Your LLC name], [State] LLC, formed [month/year]. EIN available on request.
- Owner and only employee: [Name], based in Montenegro.
- Website: [URL] · LinkedIn: [URL]
- Stage: new. No referred deals closed yet.

**What I do**
- Source GPU capacity for AI startups, research groups and SMEs, mainly in the EU and South-East Europe. I work in English and Serbian / Croatian / Bosnian / Montenegrin.
- Typical request: [8–64] GPUs, [1–12] months, often with EU data-location requirements.
- I do not resell, hold customer funds or operate infrastructure. The customer signs with you.

**How I work**
- Every buyer completes an intake and KYC / end-use form and is screened against sanctions and export restricted-party lists before I introduce them. I decline buyers I cannot verify.
- I tell every buyer in writing that I may receive a commission from the provider.

**Questions**
1. Commission rate, whether it is one-time or recurring, and payout timing.
2. Minimum deal size and term that qualify.
3. Deal registration: how, and how long does a registration stay valid?
4. Any restrictions I should know about (e.g. charging the buyer a separate fee, working with other providers, territories)?
5. Can you share the partner agreement for review before I apply formally?

I can provide company formation documents and identification as part of your onboarding.

Thank you,
[Name]
[Email] · [Phone]

---

## 5. Capacity request for a specific, screened need (no buyer name yet)

**Subject:** Capacity request — [N]× [GPU type], [region], from [date]

Hi [Name],

I have a screened buyer request and would like an indicative quote. I will share the buyer's identity once they confirm they want to proceed with [Supplier] and you confirm the deal is registered to me.

- GPUs: [N]× [type] ([alternatives acceptable: …])
- Term: [duration], start [date] (flexibility: […])
- Location: [EU / country]
- Setup: [bare metal / VM / K8s / Slurm], networking [InfiniBand / Ethernet], storage [amount, type]
- Workload: [training / fine-tuning / inference], [one neutral line]
- Buyer type: [e.g. EU-registered AI startup, VC-funded], end user is the buyer itself
- Payment: [prepay monthly / invoice]

Could you send: price per GPU-hour, what is included (storage, egress, support), contract minimums, availability date, and how long the quote is valid?

Thanks,
[Name]

---

## Notes

- Keep every supplier reply in `/suppliers/suppliers.csv` (contact, terms, status).
- Read any agreement for exclusivity, clawbacks, bans on charging the buyer, and agency wording before accepting — see `/legal/`. Ask a lawyer before signing.
