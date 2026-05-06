# Review Journal

This journal records the domain cases that matter before widening the public API.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 139, lane `watch`
- `stress`: `lease drift`, score 184, lane `ship`
- `edge`: `replica lag`, score 164, lane `ship`
- `recovery`: `membership churn`, score 224, lane `ship`
- `stale`: `quorum health`, score 138, lane `watch`

## Note

This file is intentionally plain so the fixture remains the source of truth.
