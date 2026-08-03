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

Fourteen official submissions have completed. As of 2026-08-03 07:14 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1463.6 for C08, 1356.9 for C09, 1333.0 for C10, 1833.7 for C11, 1848.2 for C12, 1763.6 for C13, and 679.8 for C14; all remain provisional while ladder matches continue. C11 was 17-1 across 18 public matches, C12 was 15-3 across 18, C13 was 12-1 across 13, and C14 won its first public match.

[C11 Moon Sales Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c11-moon-sales-schema-safe) remains the stable reference. It reproduces the publicly attributed Moon sales-splice schedule while clipping or padding hand actions to the live hand count. In a logic-equivalent fresh two-seat gate it went 16-0 against each of C08, C09, and C10, 14-2 against the public Rain schedule, and 15-1 against Router x Repair. An exact submitted-file smoke went 10-0 across the same five references.

[C12 Rayk Public Delta Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c12-rayk-public-delta-schema-safe) is a diversified challenger built from the attributed Apache-2.0 Rayk policy plus a small, auditable set of public-behavior modifications. Across 16 fresh two-seat games against C11 it finished 8-8 with mean margin +433 and median +100. At the current snapshot it had the highest recorded rating in the C11-C14 group, while its seat-dependent local margins remain an important caveat.

[C13 Licensed Hand Ablation](https://www.kaggle.com/code/beicicc/kaggriculture-c13-licensed-hand-ablation) restores the attributed licensed hand schedule at five coordinates while retaining the remaining schema-safe C12 changes. On an independent confirmation set it went 7-1 against C11, 7-1 against C12, 8-0 against Rain, and 7-1 against Router x Repair. Its 29-3 aggregate local result and 12-1 opening public record make C13 the strongest local challenger, although both samples remain provisional.

[C14 Late Crop Weed Recovery](https://www.kaggle.com/code/beicicc/kaggriculture-c14-late-crop-weed-recovery) adds a narrow visible-state repair when a late-day hired hand is scheduled to plant strawberry or melon on a weed. All eight high-weed robustness games completed with nine successful recoveries, no invalid actions, and no newly blocked crop batch; the head-to-head result was 4-4 with mean margin +597 and is treated as a safety check rather than superiority evidence. On default settings C14 matched C13 exactly across four paired seeds and went 8-0 against Rain with mean margin +3,036. Its first public match was a win, but one match is not comparative evidence.
