# LEDGER

Append only. Newest at top.

---

## 2026-09-06 — Session 1b: target revised to $100k MRR

**Goal:** the user clarified they want six figures **monthly**, not annually. Rework the plan for a 12x revenue target.

**Shipped:**
- `docs/business/SIX-FIGURE-PLAN.md` rewritten (240 lines) around a $100k MRR target
- `docs/business/DISCOVERY.md` — added question 6, caregiver headcount, which sets the per-caregiver rate
- `STATE.md` invariants extended from 5 to 8
- Still no application code. Stage 1 is unchanged under either target.

**Found:**
- Home care software prices on a base fee plus per-caregiver or per-client unit. Mid-market runs $200-500 base plus $10-25 per caregiver. Flat pricing was below market convention and left money on the table.
- Switching to $199 base + $12/caregiver moves the customer count for $100k MRR from **559 to 154**. Same sales effort, one third the customers. Highest-leverage change available, and free because nothing is built.
- Only **5%** of micro SaaS companies exceed $100k MRR. 50% plateau at $1-10k. 30% never reach $1k.
- Median time to $1M ARR (~$83k MRR) is **2 years 9 months**, and that median is dominated by funded companies with sales teams.
- Agencies already pay $195-1,500/mo, so the higher blended price sits inside existing budget.

**Disproven / corrected:**
- The flat $149/$249/$399 tier structure from the first version of this plan. Superseded. It does not reach $100k MRR at any believable customer count.
- The implied assumption that this stays a solo build. At $100k MRR the business carries 4-6 people. Hiring is now written into the plan as a staged requirement, not an option.

**Left dirty:** nothing.

**Blocked on:** discovery calls. Nothing proceeds until the wedge and the caregiver-count distribution are known.

---
## 2026-09-06 — Session 1: niche selection and plan

**Goal:** pick a product niche with proven willingness to pay and write a plan to $100k ARR.

**Shipped:**
- `docs/business/SIX-FIGURE-PLAN.md` (206 lines) — full plan
- `docs/business/DISCOVERY.md` — call script and log template
- `docs/build-state/` bootstrapped, seven files
- No application code. Intentional.

**Found:**
- Repo was near-empty: `privacy.html` and `terms.html` for an Alexa skill named Auri AI. No app code in history.
- Consumer pricing was ruled out on arithmetic. $9.99/mo needs 834 subscribers against 8-10% monthly churn.
- Healthcare vertical SaaS churns 6-10% annually. Marketing tools churn 18-24%. Vertical retains 30-50% better than horizontal at equal contract value.
- Small home care agencies already spend $100-500/mo on software. The budget line exists.
- AI receptionist was evaluated and rejected: crowded at $49-199/mo with funded players, and per-minute voice cost eats margin.

**Disproven / rejected:**
- Growing the existing Alexa skill into the revenue product. Alexa skills have no viable subscription path at this scale and the user has no installed base.
- Credential expiry tracking as the v1 wedge. Ceiling near $79/mo needs 105 customers, and it reads as a feature. Held for year two as an upsell module to the same buyer.

**Left dirty:** nothing. All work committed.

**Blocked on:** discovery calls. Nothing else proceeds until the wedge is confirmed by real agency owners.
