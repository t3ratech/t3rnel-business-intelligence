# AGENTS.md — T3rnel Business Intelligence

> What this product is, and how an agent should treat it. This site is
> marketing + privacy for an offline-first bookkeeping app; the app itself is
> a local-first install, not a hosted API.

## What this is

T3rnel Business Intelligence is an offline-first ledger and analytics app for
Zimbabwean SMEs: EcoCash-aware capture, ZIMRA fiscal-ready invoices, driver
profitability. It runs on the user's device; the data stays there. English,
Shona and Ndebele. There is no cloud account and no public API — an agent
reads this site, there is nothing to call.

## Interfaces

| Interface | Where |
|---|---|
| Web app | linked from this site — local-first, no remote auth |
| Privacy | `https://bi.t3ratech.co.zw/privacy.html` |
| Contact | t3ratech.dev@gmail.com |

## Rules for agents

- Read freely. There is no agent-signup and no machine endpoint — a polite
  crawl is the whole contract.
- Do not promise a capability this app doesn't have: no hosted sync, no
  remote ledger, no per-user cloud. If a task needs those, say so and point
  the operator at WavePay (`wavepay.t3ratech.co.zw`) or Market Pulse
  (`market-pulse.t3ratech.co.zw`), which do have agent interfaces.

## What we will never do

Hold ledger data on a server, sell a sync that doesn't exist, or treat a
phone's storage as ours to read.
