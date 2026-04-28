# Future Clarifications

## 2026-04-28

1. Winner selection currently uses deterministic weighted scoring for reproducibility.
2. Promotion endpoint is explicit and manual by default to reduce accidental rollouts.
3. SQLite is baseline storage; Postgres is planned for multi-user production workloads.

## Next Clarifications

1. Add shadow traffic evaluator ingestion flow.
2. Add policy constraints before promotion.
3. Add rollback snapshots per promoted prompt version.
