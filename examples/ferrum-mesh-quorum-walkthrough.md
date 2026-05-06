# Ferrum Mesh Quorum Forge Walkthrough

I use this file as a small checklist before changing the SQL implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 139 | watch |
| stress | lease drift | 184 | ship |
| edge | replica lag | 164 | ship |
| recovery | membership churn | 224 | ship |
| stale | quorum health | 138 | watch |

Start with `recovery` and `stale`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The next useful expansion would be a malformed fixture around lease drift and membership churn.
