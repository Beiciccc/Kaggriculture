# Experiment Log

This ledger records validated public versions and their official competition results. Ratings remain provisional while ladder matches are still running.

| Version | Date (UTC) | Local evaluation | Public code | Submission ID | Official status or rating | Notes |
|---|---|---|---|---|---|---|
| C01 | 2026-08-01 | 4-0-0 vs. public Fusion reference; `kaggle-environments==1.32.2`; max call 60.7 ms | [Kaggle Code v1](https://www.kaggle.com/code/beicicc/kaggriculture-c01-scenario-v7-reproduction) | `55154644` | `COMPLETE`; 1064.2 provisional | Reproduced Scenario-Aware v7 with source attribution; source SHA-256 `d5d704b93269` |
| C02 | 2026-08-01 | 10-0-2 development and 11-0-5 holdout vs. C01; mean holdout margin +2,686; max call 68.4 ms | [Kaggle Code v1](https://www.kaggle.com/code/beicicc/kaggriculture-c02-core-3-cow-1-sheep) | `55154872` | `COMPLETE`; 874.1 provisional | Single-variable core-herd change from 2 cows + 2 sheep to 3 cows + 1 sheep; source SHA-256 `e2e21fb1613c` |
| C03 | 2026-08-01 | 11-0-1 development and 11-0-5 holdout vs. C02; mean holdout margin +1,544; max call 50.9 ms | [Kaggle Code v1](https://www.kaggle.com/code/beicicc/kaggriculture-c03-target-herd-14) | `55155115` | `COMPLETE`; 600.0 provisional | Expanded the final herd target and matching pasture allocation from 12 to 14; source SHA-256 `99ed8978ea3a` |
