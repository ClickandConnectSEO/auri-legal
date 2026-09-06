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
