# CLAIMS

Every promise the product makes, mapped to what the code does.

**Last updated:** 2026-09-06

| Claim (verbatim from UI/docs) | File | What the code actually does | Status | Evidence |
|---|---|---|---|---|
| "Auri AI does not collect, store, or share any personal information." | `privacy.html` | Nothing. Static page. Describes an Alexa skill, not the planned SaaS. | ⚠️ WILL BECOME FALSE | `privacy.html:9`. Auri Care stores PHI by design. This page must be rewritten before any Auri Care launch. |
| "All requests processed by the skill are handled securely through Amazon Alexa and are not saved by the developer." | `privacy.html` | Nothing. Refers to the Alexa skill only. | ⚠️ SCOPE MISMATCH | `privacy.html:9`. Accurate for the Alexa skill. Wrong for the new product. |
| "Auri AI provides general communication assistance only. It does not provide medical, legal, therapeutic, or professional advice." | `terms.html` | Nothing. Static page. | ⚠️ SCOPE MISMATCH | `terms.html:9`. Auri Care handles care records. Terms need a full rewrite. |

## Rules for this file

- A success state must never appear for something merely queued or generated. Model delivery honestly: `prepared → sent → receipt confirmed → viewed by family`.
- A family-facing "update sent" badge must mean the email or SMS provider accepted it, not that a row was written.
- Audit this file before any agency demo, any BAA signing, and any legal review.
