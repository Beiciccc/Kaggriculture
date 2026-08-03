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

Twelve official submissions have completed. As of 2026-08-03 06:09 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1463.6 for C08, 1356.9 for C09, 1333.0 for C10, 1748.7 for C11, and 683.4 for C12; all remain provisional while ladder matches continue. C11 had completed 14 public ladder matches at this snapshot, while C12 had completed one.

The current rating-backed recommendation is [C11 Moon Sales Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c11-moon-sales-schema-safe). It reproduces the publicly attributed Moon sales-splice schedule while clipping or padding hand actions to the live hand count. In a logic-equivalent fresh two-seat gate it went 16-0 against each of C08, C09, and C10, 14-2 against the public Rain schedule, and 15-1 against Router x Repair. An exact submitted-file smoke went 10-0 across the same five references.

[C12 Rayk Public Delta Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c12-rayk-public-delta-schema-safe) is a diversified challenger built from the attributed Apache-2.0 Rayk policy plus a small, auditable set of public-behavior modifications. Across 16 fresh two-seat games against C11 it finished 8-8 with mean margin +433 and median +100. This parity result and its seat-dependent margins make C12 useful as a contrasting ladder probe, but not yet a replacement for C11.
