# Tech stack

Everything I've shipped with, and where. Numbers in parentheses are case studies.

## Languages

| Language | Where |
|---|---|
| **TypeScript** | Every HGFI Tools web app and service (01–03, 06–11), the Performance Center (12), the RPG and DWV trainer (15), OpenClaw Remote (16) |
| **Python** | Books rebuild and reconciliation toolkit with pandas and pdfplumber (04), shaynhornik.com on FastAPI (14), marketing-ROI analysis, AI memory harvester (16), Boot.dev projects |
| **Kotlin** | Native Android calling app with Jetpack Compose (06), phone remote-control app (16) |
| **Java** | Android visit recorder (09), Android emergency alarm app (07): plain Java, no third-party libraries |
| **Go** | RSS aggregator with sqlc and goose, Pokédex CLI ([OPEN-SOURCE](OPEN-SOURCE.md)) |
| **SQL** | Hand-written Postgres migrations, indexes, SQL functions over JSONB (02), row-level security (03), 15 tested business reports (05) |
| **Bash** | Deploy pipelines with locks and safety checks, encrypted backups, secret-safe tooling (01) |
| **JavaScript** | Branded browser arcade with Canvas 2D and Web Audio (15), Three.js puzzle game (15), browser automation (16) |

## Frontend

Next.js 14 and 16 (App Router, server components, route handlers, `instrumentation.ts` workers) · React 18 and 19 ·
Tailwind 3 and 4 · a shared CSS design system across ten apps (01) · Tiptap rich-text editor (10) · Leaflet (10) ·
Recharts (12) · Three.js and WebXR (15) · Zustand, CodeMirror 6, PWA with Workbox (16) · Jinja2 + htmx with a
hand-written SVG chart library (14) · Shadow-DOM embeddable widget (13).

## Backend and APIs

Next.js route handlers (hundreds of them across the suite) · FastAPI (14) · Payload CMS 3 (13) · Fastify (15) ·
Express · webhook-driven event engines with signature verification (06, 10) · in-process background workers with
resumable loops (03, 09) · REST API contract design with frozen versioned contracts for mobile clients (06).

## Data

PostgreSQL 16 and 17 (JSONB, row-level security, SQL functions, per-tool databases) · Prisma 5 and 7 with the `pg`
driver adapter · SQLAlchemy 2 · SQLite (WAL) · pandas · change-cursor replication of a rate-limited SaaS API (02) ·
idempotent upserts keyed on source ids · encryption at rest with AES-256-GCM (03, 08).

## AI and LLMs

Anthropic Claude API with Zod-validated structured output (03, 07, 09, 10) · a multi-provider gateway over Anthropic,
OpenAI, Gemini and OpenRouter with per-job routing, fallbacks, JSON Schema compatibility analysis and a cost ledger (08)
· BM25 retrieval over uploaded documents (07) · deterministic guardrails layered on LLM output (07) · golden-conversation
and rubric evals as deploy gates (07, 09) · Deepgram speech-to-text with diarization (06, 09) · human-in-the-loop agents
with per-item approval (13) · read-only LLM access to production data for non-programmers (05) · Claude Code, multi-agent
workflows and MCP (15, 16, [HOW-I-BUILD](HOW-I-BUILD.md)).

## Mobile

Kotlin + Jetpack Compose · Jetpack core-telecom (self-managed calling) · foreground services and call-style
notifications · Telnyx Android Voice SDK, WebRTC, ICE, TURN · Firebase Cloud Messaging (including direct HTTP v1 with a
self-signed service-account JWT) · Android Keystore · OAuth PKCE sign-in via Custom Tabs · AccessibilityService (16) ·
offline-first recording with JobScheduler uploads (09) · Capacitor (13) · release signing with publish guards.

## Telephony and messaging

Telnyx Call Control, WebRTC, SIP, TeXML and AI Assistants (06, 07) · 10DLC SMS campaigns with a consent ledger and
STOP/START handling (10) · Amazon SES with DKIM, suppression, pacing and SNS event webhooks (10) · Gmail API (07).

## Infrastructure and operations

Docker and Docker Compose · Caddy (automatic TLS, `forward_auth`, security headers, log redaction) · oauth2-proxy with
Google Workspace · nginx · systemd · PM2 · DigitalOcean Droplets, Spaces and Functions · Google Cloud Compute Engine ·
Tailscale · GPG-encrypted nightly backups with documented disaster recovery · zero-downtime deploys with automatic
rollback (12) · Bitwarden Secrets Manager · Trivy image scans and `npm audit` in deploy gates (03).

## Testing

Vitest · JUnit · Node test runner · Playwright · end-to-end tests that place real phone calls through headless browsers
acting as phones (06) · provider adapters tested against recorded real SSE streams (08) · headless WebGL smoke tests
with SwiftShader (15) · parity harnesses that diff old and new pay engines over real data before shipping (12).

## Integrations

QuickBooks Online · QuickBooks Time · Ramp · Plaid · ServiceTitan (23 API areas) · Housecall Pro · Telnyx · Deepgram ·
Amazon SES and SNS · Anthropic · OpenAI · Google Gemini · OpenRouter · Google Workspace OAuth · Gmail · Google Sheets ·
Google Places · Google Search Console · Google Business Profile · Meta Graph · DataForSEO · Firebase Cloud Messaging ·
DigitalOcean Spaces · Garmin Connect · Android Health Connect · Duolingo · Boot.dev · Goodreads · Resend.

## Game and 3D

Three.js · WebXR · Unreal Engine 5.8 (Blueprints authored programmatically through an editor MCP bridge) · Godot 4 ·
Blender Python (`bpy`) procedural asset pipeline · Canvas 2D · Web Audio synthesis (15).
