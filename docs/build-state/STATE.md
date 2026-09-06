# STATE

**Last updated:** 2026-09-06
**Phase:** 0 — market validation. No application code exists.
**Active branch:** `claude/six-figure-app-plan-x9hqbj`
**Branch tip at write time:** c5b5fe5

## What this repo is today

Two static files, `privacy.html` and `terms.html`, written for **Auri AI**, an Amazon Alexa skill offering general communication assistance. No application, no package.json, no build tooling.

## What it is becoming

**Auri Care** — a family communication layer sold to small home care agencies. Full reasoning in `docs/business/SIX-FIGURE-PLAN.md`.

Target: 47 paying agencies at a $179/mo blend = $8,400 MRR = $100k ARR. Realistic window 12-18 months.

## Hard invariants

1. **No code before 20 discovery calls are logged.** Building the wrong product well is the failure mode with the highest cost.
2. **No paying customer before a BAA-covered stack is live.** Visit notes about named clients are PHI. The agency is the covered entity, Auri is the business associate.
3. **v1 scope is fixed at four features.** Caregiver logging, family view, agency console, weekly digest. Scheduling, EVV, payroll, billing and clinical charting are out of scope and stay out.
4. **No PHI in logs, analytics, or error tracking.** Ever.
5. **The existing legal pages describe the Alexa skill, not Auri Care.** They are wrong for the new product and must be rewritten before launch. Tracked in `CLAIMS.md`.

## Next 3

1. **Run 20 discovery calls with home care agency owners** — unblocked, start now. Done when: 20 completed calls recorded in `docs/business/DISCOVERY.md` with the five standard answers each. Est: L (4-6 weeks)
2. **Choose and provision the HIPAA infrastructure stack** — blocked on: call #20 confirming the wedge. Unblocks: all build work. Done when: a vendor BAA is signed and the decision is appended to `DECISIONS.md`. Est: M
3. **Build v1 and onboard 3 design partners** — do only after #1 and #2, because the feature set depends on discovery answers and the data model depends on the compliance stack. Done when: 3 agencies have live families receiving updates. Est: L
