# Daily (daily-co)

Daily provides WebRTC video and audio infrastructure for developers — REST APIs for rooms, recordings, transcripts, meetings, dial-out and Daily Bots / Pipecat Cloud (voice AI agents), plus client SDKs for Web, iOS, Android, React Native and Flutter.

**APIs.json:** [apis.yml](apis.yml)

## Type
- **x-type:** company

## APIs
- **Daily REST API** — `https://api.daily.co/v1` — manage domains, rooms, meeting tokens, recordings, transcripts, meetings, participants, presence, batch ops, dial-in/dial-out, webhooks, live streaming. Bearer-token auth. [Docs](https://docs.daily.co/reference/rest-api).
- **Pipecat Cloud (Daily Bots)** — `https://api.pipecat.daily.co/` — REST + SDKs for deploying voice AI agents built with the open-source Pipecat framework. [Docs](https://docs.pipecat.daily.co/).

## Tags
Realtime, WebRTC, Video, Audio, SDK, Voice AI, Recording, Transcription

## Common Properties
- [Website](https://www.daily.co/)
- [Documentation](https://docs.daily.co/)
- [Pricing](https://www.daily.co/pricing/)
- [GitHub](https://github.com/daily-co)
- [Status Page](https://status.daily.co/)
- [Plans](plans/daily-co-plans-pricing.yml) — reconciled
- [Rate Limits](rate-limits/daily-co-rate-limits.yml) — reconciled
- [FinOps](finops/daily-co-finops.yml) — reconciled, FOCUS-aligned

## Rate Limits (reconciled)
- Standard endpoints: 20 req/sec (~100 per 5s window)
- Listings & deletions: ~2 req/sec
- Recording / live-streaming starts: ~1 req/sec
- Throttled responses return HTTP 429 with `Retry-After`.

## Plans (reconciled)
- **Video SDK Free** — 10,000 participant-minutes/month included.
- **Video SDK Pay-As-You-Go** — usage-based participant-minute billing.
- **Pipecat Cloud** — usage-based per agent-minute.
- **WebRTC Infrastructure** — usage-based, volume discounts.
- **Enterprise** — custom contracts via sales.

## OpenAPI
Daily generates SDKs from an internal OpenAPI definition but does not publish a downloadable spec at a stable URL as of 2026-05-08; pipeline did not retrieve a spec into `openapi/`.

## Timestamps
- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## Maintainers
- **Kin Lane** — kin@apievangelist.com
