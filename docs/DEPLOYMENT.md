# Deployment Guide

## Local Compose

```bash
docker compose --env-file .env -f docker-compose.yml up --build
```

## Production Compose

```bash
docker compose --env-file .env -f docker-compose.prod.yml up --build -d
```

## GitHub Setup

1. Set Pages source to `GitHub Actions`.
2. Push semantic tags (`vX.Y.Z`) for release image pipeline.

## Health Checks

1. `GET /health`
2. `GET /ready`

## Environment Variables

Backend:

1. `APP_ENV`
2. `PROMPT_OPS_HOST`
3. `PROMPT_OPS_PORT`
4. `PROMPT_OPS_ALLOWED_HOSTS`
5. `PROMPT_OPS_CORS_ORIGINS`
6. `PROMPT_OPS_ENABLE_HSTS`
7. `PROMPT_OPS_MAX_PAYLOAD_BYTES`
8. `PROMPT_OPS_RATE_LIMIT_PER_MINUTE`
9. `PROMPT_OPS_DB_PATH`
10. `PROMPT_OPS_API_KEY`

Frontend:

1. `VITE_API_BASE_URL`
