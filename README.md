# Veo 3.1 API (veo-3.1 / veo3.1) — gateway guide with published pricing

> **default $0.07; extend $0.07; 4K $0.57** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://apimart.ai/pricing)** · **[Get an API key](https://apimart.ai/keys)**

Everything here refers to **veo-3.1** — also written **veo3.1** or **veo 3.1**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `default` | $0.07 |
| `extend` | $0.07 |
| `4K` | $0.57 |
| `EXTEND-4K` | $0.57 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $7 |
| 1,000 | $70 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"veo3.1-lite","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
