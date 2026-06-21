# FallSeed Claims Firm

> **A Progressive Web App (PWA) seed for UK Claims firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-claims/

## What this is

`fallseed-claims` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Claims wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

PI / Claims management · personal injury · CMR (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallclaim`](https://sjgant80-hub.github.io/fallclaim/) | Case register · liability / quantum / damages tracker · limitation diary · CFA / DBA records · CRU log · costs schedule · 12-pt compliance |
| onboard | [`fallclaimonboard`](https://sjgant80-hub.github.io/fallclaimonboard/) | Intake · CDD / KYC · cause-of-action gate · limitation check · CFA / DBA selection · success-fee disclosure · pre-action protocol kickoff |
| paper | [`fallclaimpaper`](https://sjgant80-hub.github.io/fallclaimpaper/) | CFA / DBA · Letter of Claim · Part 36 offers · Schedule of Loss · settlement deed · client care · cancellation rights (CMCOB) |
| practice | [`fallclaimpractice`](https://sjgant80-hub.github.io/fallclaimpractice/) | Workflow · KPI tracker · CMCOB attestations · vulnerable-customer review · file reviews · complaints log · ATE renewals |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-claims-v2`) on your device
- **BroadcastChannel mesh** — `fall-claim` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1091**, spine-clean mod 127. Mesh channel **`fall-claim`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
