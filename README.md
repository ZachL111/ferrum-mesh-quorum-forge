# ferrum-mesh-quorum-forge

`ferrum-mesh-quorum-forge` is a compact SQL repository for distributed systems, centered on this goal: Implement an SQL distributed systems project for quorum incremental indexing, using append-only fixtures and checkpoint recovery checks.

## Why It Exists

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Ferrum Mesh Quorum Forge Review Notes

The first comparison I would make is `membership churn` against `quorum health` because it shows where the rule is most opinionated.

## Features

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/ferrum-mesh-quorum-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `membership churn` and `quorum health`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture Notes

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `quorum health`, `lease drift`, `replica lag`, and `membership churn`.

The SQL checks add a separate view over the domain review fixture.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Limitations And Roadmap

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.
