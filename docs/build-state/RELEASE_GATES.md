# RELEASE GATES

Evidence or blank. Never mark a gate done by narrative.

## Phase 0 — validation (current)

- [ ] 20 discovery calls logged, six questions each — evidence: — blocked on: scheduling
- [ ] 8+ owners asked "when can I have it" — evidence: — blocked on: calls
- [ ] Caregiver headcount recorded for all 20, per-caregiver rate set from the spread — evidence: — blocked on: calls
- [ ] Base + per-caregiver price verbally accepted by 3+ owners — evidence: — blocked on: calls

## Phase 1 — compliance foundation

- [ ] Infrastructure vendor BAA signed — evidence: — blocked on: stack decision
- [ ] Healthcare technology lawyer review completed — evidence: — blocked on: budget release
- [ ] Agency-facing BAA template drafted — evidence: — blocked on: lawyer review
- [ ] Row-level tenant isolation enforced in Postgres, proven by a test that fails on cross-tenant read — evidence: — blocked on: schema
- [ ] Zero PHI in logs, analytics and error tracking, proven by a grep of a production log sample — evidence: — blocked on: build
- [ ] Audit log records every read of a client record — evidence: — blocked on: build
- [ ] Encryption at rest and in transit verified — evidence: — blocked on: build

## Phase 2 — product

- [ ] Caregiver visit log completes in under 30 seconds on a real phone, timed — evidence: — blocked on: build
- [ ] Family view works with no app install, tested on iOS Safari and Android Chrome — evidence: — blocked on: build
- [ ] Weekly digest delivers, with provider acceptance confirmed, not just a queued row — evidence: — blocked on: build
- [ ] Typecheck clean, test suite green, lint clean — evidence: — blocked on: build
- [ ] Build reproducible from a clean clone, every env var documented — evidence: — blocked on: build
- [ ] `privacy.html` and `terms.html` rewritten for Auri Care and matching real data flows — evidence: — blocked on: build
- [ ] Every row in `CLAIMS.md` is ✅ or has a scheduled fix — evidence: — blocked on: build
- [ ] No secrets or credentials in git history, `.gitignore` covers build artifacts — evidence: — blocked on: build

## Phase 3 — revenue

- [ ] Stripe live, trial-to-paid conversion working end to end — evidence: — blocked on: Phase 2
- [ ] 3 design partners with families actively receiving updates — evidence: — blocked on: Phase 2
- [ ] Usage metering counts active caregivers per agency exactly as the invoice does — evidence: — blocked on: Phase 2
- [ ] First signed contract at the full per-caregiver rate — evidence: — blocked on: all above

## Phase 4 — scale (stage 3, year 3)

- [ ] SOC 2 Type II report, required for multi-location and franchise buyers — evidence: — blocked on: revenue funding $25-40k
- [ ] Net revenue retention above 120%, measured over 12 months — evidence: — blocked on: module ladder shipping
