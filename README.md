# Kaggriculture

Public project repository for the [Kaggriculture](https://www.kaggle.com/competitions/kaggriculture/overview) farming simulation competition.

The project studies robust policies for long-horizon farm management under dynamic prices, limited actions, and head-to-head evaluation. Public versions are documented with reproducible local evaluation summaries and their official competition results.

## Competition setting

- A season lasts 30 in-game days and 720 turns.
- Policies manage crops, animals, labor, land, inventory, and market orders.
- Ranking is based on head-to-head wins, losses, and ties rather than final coin margin.
- Public ratings can change as additional matches are played.

## Repository contents

- `experiments/experiment_log.md`: public experiment and submission record.
- `data/README.md`: data provenance and redistribution notes.
- Links to validated competition-associated public Kaggle Code versions will be recorded after publication.

## Current status

Eight official submissions have completed. As of 2026-08-02 01:10 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1064.5 for C07, and 600.0 for C08; all remain provisional while ladder matches continue.

The current recommended public release is [C06 Scenario Fertilizer](https://www.kaggle.com/code/beicicc/kaggriculture-c06-scenario-fertilizer). [C07 Public V12 Tape](https://www.kaggle.com/code/beicicc/kaggriculture-c07-public-v12-tape) and [C08 Schema-Safe 89308208](https://www.kaggle.com/code/beicicc/kaggriculture-c08-schema-safe-89308208) document two credited public replay reproductions; C08 adds protection against replay-to-state hand-count drift.
