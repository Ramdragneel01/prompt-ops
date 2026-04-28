# prompt-ops Architecture

## Overview

prompt-ops treats prompts as deployable assets and runs controlled baseline/challenger experiments before promotion.

## Runtime Topology

1. Backend API service
   - Prompt version registry
   - Experiment orchestration and scoring
   - Promotion workflow and audit trail
2. Frontend dashboard
   - Prompt registration form and catalog
   - Experiment setup and evaluation controls
   - Promotion recommendation visibility
3. SQLite persistence
   - Local and small-team baseline store
   - Portable test and dev data path

## Key Flows

1. Register prompt version.
2. Create experiment with baseline and challenger prompt IDs.
3. Submit evaluation items for both variants.
4. Compute weighted quality/safety/latency score.
5. Mark winner and optionally promote.

## Security and Reliability

1. Trusted host validation.
2. Request payload size limit.
3. Optional HSTS for HTTPS deployments.
4. Input validation and type constraints.
5. Health and readiness endpoints.

## Scale Path

1. Swap SQLite with Postgres.
2. Add background worker for high-volume evaluation batches.
3. Add policy-gated auto-promotion and rollback pipelines.
