# Contributing

## Setup

1. Install Python 3.12+ and Node.js 20+.
2. Copy `.env.example` to `.env`.
3. Install backend and frontend dependencies.
4. Run tests and builds before opening a pull request.

## Validation

```bash
cd backend
pytest -q

cd ../frontend
npm run build
```

## Pull Request Requirements

1. Keep changes scoped to one behavior set.
2. Update docs for API or deployment changes.
3. Capture non-obvious trade-offs in docs/FUTURE-CLARIFICATIONS.md.
