# API Reference

## Health

1. `GET /health`
2. `GET /ready`

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
