# OPEN THREADS

**Last updated:** 2026-09-06

## Active

| Thread | Next action | Blocker |
|---|---|---|
| Market validation | Book and run 20 calls with home care agency owners | None. Unblocked. |
| HIPAA stack choice | Compare AWS-with-BAA against Supabase Team + HIPAA add-on on real cost | Waiting on discovery to confirm the product handles PHI as expected |
| Legal review | Book 2 hours with a healthcare technology lawyer, budget $800-1,500 | Do before the first paying agency, not before |
| Legal pages are wrong | `privacy.html` and `terms.html` describe an Alexa skill, not a web SaaS handling PHI | Rewrite required before launch. See `CLAIMS.md`. |
| Caregiver adoption risk | Design the 30-second logging flow and time it on a real device | Blocked on build phase |

## Deferred — will get worse

**Multi-tenant data isolation.** Cheap now, expensive later. The moment agency data is written without row-level isolation enforced in the database, retrofitting it becomes a full migration under compliance pressure. Decide the tenancy model in the first schema commit, and enforce it in Postgres RLS rather than application code.

**The Auri AI / Auri Care name collision.** Two products under one name, one an Alexa skill with published legal pages, one a HIPAA-regulated SaaS. Decide now whether Auri Care is a separate brand or a rename. Untangling published legal documents after launch costs real money.
