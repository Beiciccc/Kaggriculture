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

Ten official submissions have completed. As of 2026-08-02 01:56 UTC, the latest recorded public ratings were 1064.2 for C01, 1147.4 for C02, 1115.2 for C03, 1067.2 for C04, 1155.4 for C05, 1252.9 for C06, 1326.8 for C07, 1372.9 for C08, 1027.6 for C09, and 600.0 for C10; all remain provisional while ladder matches continue. C10 had no public ladder matches at this snapshot, so its 600.0 value is an initialization rather than comparative evidence.

The current recommended public release is [C08 Schema-Safe 89308208](https://www.kaggle.com/code/beicicc/kaggriculture-c08-schema-safe-89308208). [C09 Dynamic Shed](https://www.kaggle.com/code/beicicc/kaggriculture-c09-dynamic-shed) extends C08 with state-aware final-day shed liquidation; paired tests improved or tied C08 on every evaluated seed, while cross-play against C06 remained weaker. C09 is exploratory because its step-696 replacement does not cap the combined market-order list when many product types coexist. [C10 Conservative Probe Router](https://www.kaggle.com/code/beicicc/kaggriculture-c10-conservative-probe-router) adds a targeted visible-state probe to a public replay router: it preserves the base step-4 action, then uses the opponent's public balance at step 7 to distinguish the tested C07- and C08-type openings. Fresh two-seat tests were positive against C07, C08, and C09, but the rule is deliberately narrow and C10 remains exploratory pending meaningful ladder evidence.
