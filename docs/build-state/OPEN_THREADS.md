# OPEN THREADS

**Last updated:** 2026-09-06 (revised for the $100k MRR target)

## Active

| Thread | Next action | Blocker |
|---|---|---|
| Market validation | Book and run 20 calls with home care agency owners, six questions each | None. Unblocked. |
| Per-caregiver rate | Set the $/caregiver figure from the headcount spread across the 20 calls | Blocked on call #20 |
| HIPAA stack choice | Compare AWS-with-BAA against Supabase Team + HIPAA add-on on real cost | Blocked on discovery confirming the product handles PHI as expected |
| Legal review | Book 2 hours with a healthcare technology lawyer, budget $800-1,500 | Do before the first paying agency, not before |
| Legal pages are wrong | `privacy.html` and `terms.html` describe an Alexa skill, not a web SaaS handling PHI | Rewrite required before launch. See `CLAIMS.md`. |
| Caregiver adoption risk | Design the 30-second logging flow and time it on a real device | Blocked on build phase |

## Deferred — will get worse

**Multi-tenant data isolation.** Cheap now, expensive later. The moment agency data is written without row-level isolation enforced in the database, retrofitting it becomes a full migration under compliance pressure. Decide the tenancy model in the first schema commit and enforce it in Postgres RLS, not application code.

**The Auri AI / Auri Care name collision.** Two products under one name, one an Alexa skill with published legal pages, one a HIPAA-regulated SaaS. Decide now whether Auri Care is a separate brand or a rename.

**Usage metering.** Pricing is per caregiver, so the system must count active caregivers per agency per billing period from day one, and count it the same way the invoice does. Bolting metering onto a live billing system after a hundred agencies are on it is a revenue-integrity problem, not a feature.

**SOC 2 Type II.** Not needed for owner-operator agencies. Required to sell multi-location and franchise groups in stage 3. Budget $25-40k in year three. Evidence collection is far cheaper if audit logging and access control are built correctly in v1.

**Founder as bottleneck.** The named reason half of micro SaaS plateaus under $10k MRR. The hiring trigger is $20k MRR for customer success. It will feel too early. Hire anyway.
