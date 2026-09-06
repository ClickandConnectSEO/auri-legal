# STATE

**Last updated:** 2026-09-06 (revised, session 1)
**Phase:** 0 — market validation. No application code exists.
**Active branch:** `claude/six-figure-app-plan-x9hqbj`

## What this repo is today

Two static files, `privacy.html` and `terms.html`, written for **Auri AI**, an Amazon Alexa skill offering general communication assistance. No application, no package.json, no build tooling.

## What it is becoming

**Auri Care** — a family communication layer sold to small home care agencies, expanding into agency operations over three years. Full reasoning in `docs/business/SIX-FIGURE-PLAN.md`.

**Target: $100,000 MRR.** Revised mid-session from $100k ARR. 154 agencies at a $650 blended monthly rate. Realistic window is 42 months, in four staged phases.

The beachhead product and stage 1 are identical under either target. Only pricing, staffing and the module ladder changed.

## Hard invariants

1. **No code before 20 discovery calls are logged.** Building the wrong product well is the failure mode with the highest cost.
2. **Pricing is base + per caregiver, never flat.** Flat $179 needs 559 agencies for $100k MRR. Base $199 + $12/caregiver needs 154. This is the highest-leverage decision in the plan and it is free to make now.
3. **No paying customer before a BAA-covered stack is live.** Visit notes about named clients are PHI. The agency is the covered entity, Auri is the business associate.
4. **v1 scope is fixed at four features.** Caregiver logging, family view, agency console, weekly digest. Scheduling, EVV, payroll, billing and clinical charting stay out until stage 3.
5. **No PHI in logs, analytics, or error tracking.** Ever.
6. **Personal money funds stage 1 only.** Stages 2 through 4 are funded by revenue.
7. **Hire customer success at $20k MRR**, even though it will feel early. Founder-as-bottleneck is why most SaaS plateaus under $10k.
8. **The existing legal pages describe the Alexa skill, not Auri Care.** They are wrong for the new product. Tracked in `CLAIMS.md`.

## Next 3

1. **Run 20 discovery calls with home care agency owners** — unblocked, start now. Six questions, including caregiver headcount, which sets the per-caregiver rate. Done when: 20 completed calls recorded in `docs/business/DISCOVERY.md`. Est: L (4-6 weeks)
2. **Choose and provision the HIPAA infrastructure stack** — blocked on: call #20 confirming the wedge. Unblocks: all build work. Done when: a vendor BAA is signed and the decision is appended to `DECISIONS.md`. Est: M
3. **Build v1 and onboard 3 design partners** — do only after #1 and #2, because the feature set depends on discovery answers and the data model depends on the compliance stack. Done when: 3 agencies have live families receiving updates. Est: L
