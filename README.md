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

Thirteen official submissions have completed. As of 2026-08-03 06:23 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1463.6 for C08, 1356.9 for C09, 1333.0 for C10, 1833.7 for C11, 1057.3 for C12, and 600.0 for C13; all remain provisional while ladder matches continue. C11 had completed 18 public ladder matches at this snapshot, C12 had completed four, and C13 had completed validation but no public matches.

The current rating-backed recommendation is [C11 Moon Sales Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c11-moon-sales-schema-safe). It reproduces the publicly attributed Moon sales-splice schedule while clipping or padding hand actions to the live hand count. In a logic-equivalent fresh two-seat gate it went 16-0 against each of C08, C09, and C10, 14-2 against the public Rain schedule, and 15-1 against Router x Repair. An exact submitted-file smoke went 10-0 across the same five references.

[C12 Rayk Public Delta Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c12-rayk-public-delta-schema-safe) is a diversified challenger built from the attributed Apache-2.0 Rayk policy plus a small, auditable set of public-behavior modifications. Across 16 fresh two-seat games against C11 it finished 8-8 with mean margin +433 and median +100. This parity result and its seat-dependent margins make C12 useful as a contrasting ladder probe, but not yet a replacement for C11.

[C13 Licensed Hand Ablation](https://www.kaggle.com/code/beicicc/kaggriculture-c13-licensed-hand-ablation) restores the attributed licensed hand schedule at five coordinates while retaining the remaining schema-safe C12 changes. On an independent confirmation set it went 7-1 against C11, 7-1 against C12, 8-0 against Rain, and 7-1 against Router x Repair. The 29-3 aggregate result makes C13 the strongest local challenger, but its initial 600.0 rating is not yet comparative evidence.
