# INFRA NOTES

Append only. Environment landmines and how they were resolved.

---

## 2026-09-06 — session environment

- Remote Claude Code container. Outbound HTTPS goes through an agent proxy. CA bundle at `/root/.ccr/ca-bundle.crt`. Never disable TLS verification or unset `HTTPS_PROXY`.
- No `gh` CLI. GitHub work goes through `mcp__github__*` tools.
- Supabase and Cloudflare MCP servers are connected to this account. Relevant to the Phase 1 stack decision, but connection is not the same as a signed BAA. Verify the compliance tier before assuming either is usable for PHI.
- Repo had no `package.json`, no lockfile, no CI at session 1. Nothing to build or test yet.

## Known future landmine

Supabase HIPAA coverage requires the Team plan plus a HIPAA add-on, around $599/mo. The MCP connection being present does NOT mean the project is HIPAA-eligible. Confirm the plan tier before writing a single row of client data.
