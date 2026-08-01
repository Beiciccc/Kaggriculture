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

Five official submissions have completed. As of 2026-08-01 09:25 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1145.5 for C04, and 1275.0 for C05; all remain provisional while ladder matches continue.

The recommended public release is [C05 Mid Herd 10](https://www.kaggle.com/code/beicicc/kaggriculture-c05-mid-herd-10). Its documented v2 preserves the submitted executable logic while adding the strategy summary, paired validation evidence, source attribution, and limitations.
