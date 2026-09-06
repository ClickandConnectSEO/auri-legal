# Auri Care — the plan to $100k ARR

Written 2026-09-06. Owner: Auri. Build partner: Claude Code.

---

## 1. The target, in plain numbers

$100,000 ARR = **$8,333 MRR**.

How you reach it depends entirely on price:

| Model | Price | Paying customers needed | Realistic? |
|---|---|---|---|
| Consumer app | $9.99/mo | 834 | No. Consumer churn runs 8-10% monthly. You would need ~80 new subs every month forever. |
| Prosumer | $29/mo | 288 | Hard. Still a volume game. |
| **Small-business vertical SaaS** | **$179/mo blended** | **47** | **Yes.** |
| Mid-market vertical | $499/mo | 17 | Yes, but the sales cycle is 3-6 months each. |

**Decision: build B2B vertical software, not a consumer app.**

Forty-seven customers is a number you are able to name, track on one page, and call personally. Eight hundred anonymous subscribers is a marketing machine you have no budget to run.

---

## 2. Three niches evaluated

All three share **one buyer**: the owner of a small home care agency. Picking one buyer and staying there is the whole strategy. You learn the market once and sell it three products over five years.

### Niche 1 — Family communication layer for home care agencies ✅ RECOMMENDED

Caregivers finish a visit. Families hear nothing until someone phones the office. Agencies win private-pay clients on trust, and right now trust is a voicemail.

- Price: $149-$399/mo
- Customers to six figures: **47**
- Build weight: light. No billing, no payroll, no EVV.
- Competition: the big platforms (WellSky, AlayaCare, Axxess, HHAeXchange) own scheduling and compliance. Family updates are an afterthought bolted onto all of them.

### Niche 2 — Credential and compliance expiry tracking ❌ Not first

Expired CNA certificates are a genuine, expensive pain. But the ceiling is around $79/mo, which needs 105 customers, and it reads as a feature rather than a product.

**Keep it.** Ship it as a paid module in year two. Same buyer, near-zero acquisition cost, straight lift to net revenue retention.

### Niche 3 — AI front desk for home care intake ❌ Not first

One missed inquiry is worth $40,000 in lifetime billings, so the value is real. But the field is crowded with funded players at $49-$199/mo (My AI Front Desk, Dialzara, NextPhone, Trillet), and per-minute voice costs eat the margin. A solo founder has no edge here.

---

## 3. Why home care wins on the data

- Healthcare vertical SaaS shows **6-10% annual churn**. Marketing tools show 18-24%. Sticky beats cheap.
- Vertical SaaS retains **30-50% better** than horizontal software at the same contract value.
- Small agencies **already pay $100-$500/mo** for software. You are not creating a budget line. You are competing for one.
- There are roughly 33,000 home care agencies in the US. Forty-seven of them is **0.14% of the market**.

---

## 4. The product

**Auri turns every visit into a family update.**

### v1 — four things, nothing else

1. **Caregiver web app.** End of visit, under 30 seconds. Tap what happened: meals, medication prompted, mood, activity. Optional photo. Optional voice note, transcribed.
2. **Family view.** One link. No app install, no password to forget. Today's update, a timeline, photos.
3. **Agency console.** Add clients, invite families, review flagged updates before they send, agency logo on everything.
4. **Weekly digest email** to the family. This is the retention hook, not a nice-to-have.

### What v1 deliberately does NOT do

Scheduling. EVV. Payroll. Billing. Clinical charting. Medication administration records.

Every one of those brings compliance weight and a funded incumbent. Stay out.

### The sales line

Sell revenue, not savings.

> One extra private-pay client at 20 hours a week and $35 an hour is $36,400 a year. Auri costs $1,788 a year.

That ratio closes deals. "Saves your coordinator time" does not.

---

## 5. Pricing

| Tier | Price | Limit |
|---|---|---|
| Starter | $149/mo | up to 25 active clients |
| Growth | $249/mo | up to 75 active clients |
| Agency | $399/mo | unlimited |

Annual billing at 2 months free. Blended target: **$179/mo**.

No free tier. Free tiers on B2B tools attract people who never buy and generate support load you have no time for. Offer a 14-day trial with a card on file.

---

## 6. The biggest risk, named honestly

**Caregiver adoption.** Turnover in this workforce is high. Many caregivers are rushed and some are low-tech. If they do not log the visit, the family view sits empty and the agency cancels.

Mitigations built into v1:
- Thirty seconds, hard ceiling. Time it and prove it.
- No app store download. A web app opened from an SMS link.
- Voice note fallback for anyone who will not tap through a form.
- The agency owner mandates it as part of the visit. Sell to the owner, and make the owner's onboarding script part of the product.

**Kill criterion:** if design-partner caregivers are not logging visits three times a week by day 30, the product does not work. Fix it or stop.

---

## 7. HIPAA — a real gate, not a footnote

A visit note about a named person's health, held on behalf of a care agency, is protected health information. The agency is the covered entity. Auri is a business associate. This is non-negotiable.

**Requirements before the first paying agency:**
- Signed Business Associate Agreement with every agency
- Signed BAA with every infrastructure vendor you use
- Encryption in transit and at rest
- Audit logging on every read of a client record
- Role-based access, enforced in the database, not the UI
- Zero PHI in application logs or analytics
- A published subprocessor list

**Two cost paths:**

| Path | Cost | Trade-off |
|---|---|---|
| AWS with BAA | BAA is free to sign, pay only for usage (~$60-120/mo at this scale) | More setup work |
| Supabase Team + HIPAA add-on | ~$599+/mo | Faster to build, eats most of the budget |

**Recommendation:** design-partner phase on the cheap stack with a written agreement and no real client names. Move to a BAA-covered stack before the first dollar of revenue.

**Action:** pay a healthcare technology lawyer for a two-hour review before the first paying agency signs. Budget $800-1,500. This is the cheapest insurance in the plan.

---

## 8. Getting the first 47 customers

Home care is regional and referral-driven. Do not start with ads.

1. **Twenty discovery calls first. No code.** Find owners on LinkedIn with the title "Owner, Home Care Agency". Ask what happens after a visit ends and how families find out.
2. **Three free design partners.** Local. In your metro. Drive to them.
3. **One case study with a number in it.** "Agency X closed three more private-pay clients in 60 days." Everything after this is easier.
4. **HCAOA state chapters.** Meetings and sponsorships. This is where owners gather.
5. **Franchise networks.** Home Instead, Right at Home, Comfort Keepers, Visiting Angels. Start in franchisee Facebook groups, then approach the franchisor once you have five happy franchisees.
6. **Referral fee.** Home care owners talk to each other constantly. Pay one month of revenue for a closed referral.

---

## 9. Timeline

Anyone promising six figures in 90 days is selling a course.

| Window | Milestone | MRR |
|---|---|---|
| Month 0-1 | 20 discovery calls. No code written. | $0 |
| Month 2-3 | v1 shipped. 3 design partners live. | $0 |
| Month 4-6 | First 10 paying agencies. | ~$1,800 |
| Month 7-12 | 30 agencies. First case study working. | ~$5,400 |
| Month 13-18 | 47+ agencies. | **$8,400+** |

**Realistic window to $100k ARR: 12-18 months.**

---

## 10. Where the money goes

Budget: $500-$2,000/mo.

| Item | Monthly |
|---|---|
| Hosting, database, storage (BAA-covered) | $60-120 |
| Email and SMS delivery | $40 |
| Stripe fees | 2.9% of revenue |
| Domain, monitoring, error tracking | $40 |
| HCAOA chapter membership and events | $100 avg |
| Legal and compliance reserve | $200 |
| Travel to local agencies | $100 |
| **Total** | **~$550-700** |

Everything above that goes to reserve. Do not buy ads until one channel is proven manually.

---

## 11. Kill criteria

Written now, while it is easy to be honest.

- Fewer than 8 of 20 discovery calls ask "when can I have it" → the wedge is wrong. Change it.
- Design-partner caregivers not logging 3x weekly by day 30 → adoption is fatal. Fix or stop.
- No signed $149/mo contract by month 5 → the price or the buyer is wrong.
- Month 12 under $3,000 MRR → the channel does not work. Rethink acquisition, not the product.

---

## 12. The next three moves

1. **Twenty discovery calls.** Unblocked. Start today. Done when 20 owners have answered the same five questions and the answers are written into `docs/business/DISCOVERY.md`.
2. **HIPAA infrastructure decision.** Blocked on call #20. Done when a stack is chosen and a vendor BAA is signed.
3. **Build v1.** Do only after #1 and #2. Done when 3 design partners have live families receiving updates.

**Do not write code until step 1 is finished.** The most expensive thing you would build is the wrong product, beautifully.
