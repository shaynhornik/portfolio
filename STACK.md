# Tech stack

What the systems in this repo are built with, and where. Numbers in parentheses are case studies.

## Languages

The languages I know and write by hand are **Python, Go and C**.

Most of the company code is written with Claude Code (see [HOW-I-BUILD](HOW-I-BUILD.md)). The systems are built with:

| Built with | Where |
|---|---|
| **Python** | Books rebuild and reconciliation toolkit with pandas and pdfplumber (04), marketing-ROI analysis, Boot.dev projects |
| **Go** | RSS aggregator with sqlc and goose, an HTTP server with a JSON API and JWT auth, a Pokédex CLI ([OPEN-SOURCE](OPEN-SOURCE.md)) |
| **TypeScript** | FYProof (17), every HGFI Tools web app and service (01 to 03, 06 to 11, 18), the Performance Center (12) |
| **Kotlin** | Native Android calling app with Jetpack Compose (06) |
| **Java** | Android visit recorder (09), Android emergency alarm app (07): plain Java, no third-party libraries |
| **SQL** | Postgres migrations, indexes, SQL functions over JSONB (02), row-level security (03), tested business reports (05) |
| **Bash** | Deploy pipelines with locks and safety checks, encrypted backups, secret-safe tooling (01) |

## Frontend

Next.js 14 and 16 (App Router, server components, route handlers, `instrumentation.ts` workers, one app serving three
sites by host name in 17) · React 18 and 19 · Tailwind 3 and 4 · a shared CSS design system across the suite (01) ·
Tiptap rich-text editor (10) · Leaflet (10) · Recharts (12).

## Backend and APIs

Next.js route handlers · Express · webhook-driven event engines with signature verification (06, 10) · in-process
background workers with resumable loops (03, 09) · a pg-boss job queue with a separate worker process (17) · Stripe
Checkout, entitlements, webhooks and reconciliation (17) · OAuth posting integrations with social platforms, including
atproto OAuth with DPoP (17) · REST API contract design with frozen versioned contracts for mobile clients (06).

## Data

PostgreSQL 16 and 17 (JSONB, row-level security, SQL functions, per-tool databases, a Postgres-backed job queue) ·
Prisma 5 and 7 with the `pg` driver adapter · SQLite (WAL) · pandas · change-cursor replication of a rate-limited SaaS
API (02) · idempotent upserts keyed on source ids · encryption at rest with AES-256-GCM (03, 08).

## AI and LLMs

Anthropic Claude API with Zod-validated structured output (03, 07, 09, 10) · a multi-provider gateway over Anthropic,
OpenAI, Gemini and OpenRouter with per-job routing, fallbacks, JSON Schema compatibility analysis and a cost ledger (08) ·
multimodal video checks against a sourced rulebook, with prompt-injection boundaries, an output filter,
provider-specific prompt caching and per-user spend caps (17) · BM25 retrieval over uploaded documents (07) ·
deterministic guardrails layered on LLM output (07) · golden-conversation and rubric evals as deploy gates (07, 09) ·
labeled eval sets with offline re-scoring and side-by-side comparisons (17) · Deepgram speech-to-text with diarization
(06, 09) · read-only LLM access to production data for non-programmers (05) · Claude Code and MCP
([HOW-I-BUILD](HOW-I-BUILD.md)).

## Mobile

Kotlin + Jetpack Compose · Jetpack core-telecom (self-managed calling) · foreground services and call-style
notifications · Telnyx Android Voice SDK, WebRTC, ICE, TURN · Firebase Cloud Messaging (including direct HTTP v1 with a
self-signed service-account JWT) · Android Keystore · OAuth PKCE sign-in via Custom Tabs · offline-first recording with
JobScheduler uploads (09) · Expo / React Native with an iOS share extension and a custom native module (17) · release
signing with publish guards.

## Telephony and messaging

Telnyx Call Control, WebRTC, SIP, TeXML and AI Assistants (06, 07) · 10DLC SMS campaigns with a consent ledger and
STOP/START handling (10) · Amazon SES with DKIM, suppression, pacing and SNS event webhooks (10) · Gmail API (07).

## Infrastructure and operations

Docker and Docker Compose · Caddy (automatic TLS, `forward_auth`, security headers, log redaction) · oauth2-proxy with
Google Workspace · nginx · systemd · PM2 · DigitalOcean Droplets, Spaces and Functions · Google Cloud · Tailscale ·
GPG-encrypted nightly backups with documented disaster recovery · nightly backups with automatic restore tests (17) ·
GitHub Actions CI that packs and smoke-tests a release per commit (17) · zero-downtime deploys with automatic rollback
(12, 17) · Bitwarden Secrets Manager · Trivy image scans and `npm audit` in deploy gates (03).

## Testing

Vitest · JUnit · Node test runner (each run on its own throwaway Postgres cluster in 17) · Playwright · end-to-end tests
that place real phone calls through headless browsers acting as phones (06) · provider adapters tested against recorded
real SSE streams (08) · fake Stripe, social-platform and storage servers (17) · CI checks for user copy and WCAG contrast
(17) · parity harnesses that diff old and new pay engines over real data before shipping (12).

## Integrations

QuickBooks Online · QuickBooks Time · Ramp · Plaid · Stripe · ServiceTitan · Housecall Pro · Telnyx · Deepgram · Amazon
SES and SNS · Anthropic · OpenAI · Google Gemini · OpenRouter · Google Workspace OAuth · Gmail · Google Sheets · Google
Search Console · Google Business Profile · Meta Graph · DataForSEO · Firebase Cloud Messaging · DigitalOcean Spaces ·
Resend.

## Media

ffmpeg and ffprobe (frame extraction, scene detection, cuts, blurs, muting, loudness normalization) · perceptual hashing
for frame de-duplication · child-safety hash matching that fails closed (17).
