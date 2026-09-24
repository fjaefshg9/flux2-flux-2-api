# FLUX.2 Pro API (flux-2 / flux2) — api guide with published pricing

> **1MP $0.024; 2MP $0.036; 3MP $0.048** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **flux-2** — also written **flux2** or **flux 2**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `1MP` | $0.024 |
| `2MP` | $0.036 |
| `3MP` | $0.048 |
| `4MP` | $0.06 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $2.4 |
| 1,000 | $24 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"flux-2-pro","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
