# AGENTS.md — T3rnel Business Intelligence

> What this product is, and how an agent should treat it. This site is
> marketing + privacy; the working product is an offline-first ledger app with
> an authenticated API for the operator's own data.

## What this is

T3rnel Business Intelligence is an offline-first ledger and analytics app for
Zimbabwean SMEs: EcoCash-aware capture, ZIMRA fiscal-ready invoices, driver
profitability. The web ledger runs at
`https://t3rnel-business-intelligence-production.t3ratech.workers.dev` behind
Google OAuth — English, Shona and Ndebele.

## Interfaces

| Interface | Where | Auth |
|---|---|---|
| Web app | `https://t3rnel-business-intelligence-production.t3ratech.workers.dev/` | Google OAuth |
| REST API | `https://t3rnel-business-intelligence-production.t3ratech.workers.dev/api/*` | session — the signed-in tenant's own data |
| OpenAPI | `https://bi.t3ratech.co.zw/openapi.json` | — |
| Privacy | `https://bi.t3ratech.co.zw/privacy.html` | — |

## Rules for agents

- `GET /api/health` and `GET /api/ready` are unauthenticated liveness —
  everything else wants the operator's session; there is no anonymous agent
  tier and none is implied.
- Never mint or guess a session — if a task needs the ledger, the operator
  signs in first. For public agent surfaces, use Market Pulse
  (`market-pulse.t3ratech.co.zw`) or WavePay (`wavepay.t3ratech.co.zw`),
  which are built for unauthenticated agent onboarding.

## What we will never do

Serve a tenant's ledger to a stranger, or expose a "public" route that reads
someone else's books — tenant isolation is the product, not a feature flag.
