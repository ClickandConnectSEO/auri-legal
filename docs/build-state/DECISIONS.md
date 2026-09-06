# DECISIONS

Append only. Each entry: what was decided, why, what was rejected, how reversible.

---

## 2026-09-06 — D1: B2B vertical SaaS, not a consumer app

**Decision:** target small businesses at $149-399/mo rather than consumers at $9.99/mo.

**Reasoning:** $100k ARR needs 834 consumer subscribers against 8-10% monthly churn, meaning roughly 80 replacement signups every month indefinitely. The same revenue needs 47 business customers. Forty-seven is a list you are able to call personally.

**Rejected:** consumer subscription, prosumer at $29/mo (288 customers, still a volume game).

**Reversibility:** high before code exists. Low after the data model assumes agency tenancy.

---

## 2026-09-06 — D2: home care agencies as the single buyer

**Decision:** every product, now and later, sells to the owner of a small home care agency.

**Reasoning:** healthcare vertical SaaS churns 6-10% annually against 18-24% for marketing tools. Vertical software retains 30-50% better than horizontal at equal contract value. Agencies already pay $100-500/mo, so no new budget line is needed. Roughly 33,000 agencies exist in the US, so 47 customers is 0.14% of the market.

**Rejected:** AI front desk (crowded, funded competitors at $49-199/mo, voice cost eats margin), credential expiry tracking (ceiling too low as a standalone, retained as a year-two module).

**Reversibility:** medium. The buyer relationships transfer to adjacent products. The compliance stack does not transfer outside healthcare.

---

## 2026-09-06 — D3: v1 scope frozen at four features

**Decision:** caregiver visit logging, family view, agency console, weekly digest email. Nothing else.

**Reasoning:** scheduling, EVV, payroll, billing and clinical charting each carry compliance weight and a funded incumbent (WellSky, AlayaCare, Axxess, HHAeXchange). The gap those platforms leave is showing the family what happened today. Attack the gap, not the fortress.

**Rejected:** building a full agency management platform.

**Reversibility:** high. Scope is additive later.

---

## 2026-09-06 — D4: no free tier

**Decision:** 14-day trial with a card on file. No free plan.

**Reasoning:** free B2B tiers attract users who never convert and generate support load a solo operator has no capacity to absorb.

**Reversibility:** high.

---

## 2026-09-06 — D5: pricing is base + per caregiver, never flat

**Decision:** $199 base plus $12 per caregiver per month, replacing the flat $149/$249/$399 tiers in D-series revision 1.

**Reasoning:** the target moved from $100k ARR to $100k MRR. At a flat $179 blend that needs 559 agencies. At a $650 blend from base-plus-per-caregiver it needs 154. Home care software already prices this way (mid-market runs $200-500 base plus $10-25 per caregiver), so this matches buyer expectation rather than fighting it. Revenue also grows automatically as an agency adds caregivers, which is half of the net revenue retention target.

**Rejected:** flat tiers (needs 3.6x the customers), per-client pricing (client counts churn faster than caregiver counts and make revenue lumpy).

**Reversibility:** high today, near zero after the first fifty contracts are signed. Make this call before any customer exists.

---

## 2026-09-06 — D6: staged company, not a solo product

**Decision:** four stages with explicit hiring triggers. Customer success at ~$20k MRR, a salesperson at ~$35k MRR, an engineer at ~$50k MRR.

**Reasoning:** 50% of micro SaaS plateaus between $1k and $10k MRR, mostly because the founder stays the bottleneck. $100k MRR carries 4-6 people by definition. Writing the triggers down now removes the decision from a moment when it will feel too expensive.

**Rejected:** staying solo and pushing price higher instead. Support and onboarding load in a regulated vertical does not compress that far.

**Reversibility:** high. Each trigger is a decision point, not a commitment.

---

## 2026-09-06 — D7: net revenue retention is the growth engine

**Decision:** target 120% NRR through per-caregiver pricing plus a module ladder. Credentials in year two, call-out backfill in year three.

**Reasoning:** at 120% NRR, 100 agencies paying $400 pay $691 three years later with zero new sales. Reaching 154 customers is achievable by hand. Reaching 559 is not. The ladder does the rest.

**Rejected:** growing on new logos alone.

**Reversibility:** medium. The module roadmap is flexible. The pricing unit underneath it is not.
