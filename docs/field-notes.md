# Field Notes

The useful part of this repository is the small rule set around quorum health and replica lag.

The domain cases cover `quorum health`, `lease drift`, `replica lag`, and `membership churn`. They sit beside the smaller starter fixture so the project has both a compact scoring check and a domain-flavored review check.

`recovery` is the strongest case at 224 on `membership churn`. `stale` is the cautious anchor at 138 on `quorum health`.

The point is not to make the repository bigger. The point is to make the important judgment testable.
