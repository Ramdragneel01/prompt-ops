# API Reference

## Health

1. `GET /health`
2. `GET /ready`
3. `GET /healthz`
4. `GET /readyz`

## Prompt Registry

1. `POST /api/v1/prompts`
2. `GET /api/v1/prompts`

## Experiments

1. `POST /api/v1/experiments`
2. `GET /api/v1/experiments`
3. `GET /api/v1/experiments/{experiment_id}`
4. `POST /api/v1/experiments/{experiment_id}/evaluate`
5. `POST /api/v1/experiments/{experiment_id}/promote`

## Example Prompt Create

```json
{
  "name": "support_refund_prompt",
  "version": "v3",
  "content": "You are a support assistant. Follow the refund policy and cite policy section ids.",
  "variables": ["customer_tier", "region"],
  "tags": ["support", "refund"]
}
```

## Example Experiment Evaluate

```json
{
  "items": [
    {
      "variant": "baseline",
      "quality_score": 0.81,
      "latency_ms": 820,
      "safety_pass": true
    },
    {
      "variant": "challenger",
      "quality_score": 0.86,
      "latency_ms": 790,
      "safety_pass": true
    }
  ]
}
```

## Error Contract

All API errors return a normalized payload:

```json
{
  "error": {
    "code": "rate_limited",
    "message": "rate_limited",
    "request_id": "f6aafcd2-25f2-4f5e-b0f6-c7446199758f"
  }
}
```

Common status codes:

1. `400` bad request.
2. `401` unauthorized when API key is configured.
3. `404` missing resource.
4. `413` payload too large.
5. `422` validation error.
6. `429` rate limited (includes `Retry-After: 60`).
