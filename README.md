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

Nine official submissions have completed. As of 2026-08-02 01:38 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1198.4 for C08, and 600.0 for C09; all remain provisional while ladder matches continue.

The current recommended public release is [C08 Schema-Safe 89308208](https://www.kaggle.com/code/beicicc/kaggriculture-c08-schema-safe-89308208). [C09 Dynamic Shed](https://www.kaggle.com/code/beicicc/kaggriculture-c09-dynamic-shed) extends C08 with state-aware final-day shed liquidation; paired tests improved or tied C08 on every evaluated seed, while cross-play against C06 remained weaker. C09 is exploratory because its step-696 replacement does not cap the combined market-order list when many product types coexist.
