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

Eleven official submissions have completed. As of 2026-08-03 05:14 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1463.6 for C08, 1356.9 for C09, 1333.0 for C10, and 600.0 for C11; all remain provisional while ladder matches continue. C11 had no public ladder matches at this snapshot, so its 600.0 value is an initialization rather than comparative evidence.

The current rating-backed recommendation remains [C08 Schema-Safe 89308208](https://www.kaggle.com/code/beicicc/kaggriculture-c08-schema-safe-89308208). [C11 Moon Sales Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c11-moon-sales-schema-safe) is the strongest local candidate: it reproduces the publicly attributed Moon sales-splice schedule while clipping or padding hand actions to the live hand count. In a logic-equivalent fresh two-seat gate it went 16-0 against each of C08, C09, and C10, 14-2 against the public Rain schedule, and 15-1 against Router x Repair. An exact submitted-file smoke went 10-0 across the same five references. C11 remains provisional until it accumulates meaningful public ladder matches.
