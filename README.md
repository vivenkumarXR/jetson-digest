# jetson-digest

Public feed for the daily XR × Physical AI digest, curated by a local LLM running on a
Jetson Orin Nano — no cloud. This JSON powers the live digest module on
[vivenkumarxr.com](https://vivenkumarxr.com).

## Format

```json
{
  "updated": "2026-07-07T07:00:00+05:30",
  "telemetry": { "tokens_per_s": 14.2, "temp_c": 46.1 },
  "items": [
    { "title": "Article title", "url": "https://…", "source": "The Verge" }
  ]
}
```

- `updated` — ISO timestamp of the run (with timezone)
- `telemetry` — optional; if present, the website's 3D scene shows real Jetson stats
- `items` — the 3–5 items from today's digest, newest first

The website treats a feed older than 72h as "sleeping" and shows nothing stale.
