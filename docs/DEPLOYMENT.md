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
