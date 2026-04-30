# Operations Guide

## Daily Checks

1. API health and readiness endpoints are green.
2. Probe aliases (`/healthz`, `/readyz`) return expected status.
3. Prompt and experiment create flows succeed.
4. Latest evaluation and promotion actions are persisted.
5. `429` response rate remains within expected baseline.

## Recovery Steps

1. Restart backend service.
2. Verify DB file path permissions.
3. Re-run known evaluation payload.
4. Tune `PROMPT_OPS_RATE_LIMIT_PER_MINUTE` if legitimate traffic is throttled.

## Smoke Commands

```bash
cd backend
pytest -q

cd ../frontend
npm run build
```
