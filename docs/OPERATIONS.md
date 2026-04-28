# Operations Guide

## Daily Checks

1. API health and readiness endpoints are green.
2. Prompt and experiment create flows succeed.
3. Latest evaluation and promotion actions are persisted.

## Recovery Steps

1. Restart backend service.
2. Verify DB file path permissions.
3. Re-run known evaluation payload.

## Smoke Commands

```bash
cd backend
pytest -q

cd ../frontend
npm run build
```
