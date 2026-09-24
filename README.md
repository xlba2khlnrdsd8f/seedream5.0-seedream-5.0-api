# Seedream 5.0 Pro API (seedream-5.0 / seedream5.0) — api guide with published pricing

> **1K-layer $0.0146; 1K $0.0293; 2K-layer $0.0293** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **seedream-5.0** — also written **seedream5.0** or **seedream 5.0**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `1K-layer` | $0.0146 |
| `1K` | $0.0293 |
| `2K-layer` | $0.0293 |
| `default` | $0.036 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $1.4625 |
| 1,000 | $14.625 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"seedream-5-0-pro","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
