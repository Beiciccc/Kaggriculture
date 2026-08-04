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

Nineteen official submissions have completed. The experiment ledger preserves the first recorded checkpoint for each version. As of 2026-08-04 03:46 UTC, C16 was 1569.2, C17 was 225.7, C18 had reached 1798.6, and C19 opened at 674.7 after one public win. All ratings remain provisional while ladder matches continue.

[C11 Moon Sales Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c11-moon-sales-schema-safe) remains the stable reference. It reproduces the publicly attributed Moon sales-splice schedule while clipping or padding hand actions to the live hand count. In a logic-equivalent fresh two-seat gate it went 16-0 against each of C08, C09, and C10, 14-2 against the public Rain schedule, and 15-1 against Router x Repair. An exact submitted-file smoke went 10-0 across the same five references.

[C12 Rayk Public Delta Schema Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c12-rayk-public-delta-schema-safe) is a diversified challenger built from the attributed Apache-2.0 Rayk policy plus a small, auditable set of public-behavior modifications. Across 16 fresh two-seat games against C11 it finished 8-8 with mean margin +433 and median +100. Its 15-3 public record remains provisional, while its seat-dependent local margins are an important caveat.

[C13 Licensed Hand Ablation](https://www.kaggle.com/code/beicicc/kaggriculture-c13-licensed-hand-ablation) restores the attributed licensed hand schedule at five coordinates while retaining the remaining schema-safe C12 changes. On an independent confirmation set it went 7-1 against C11, 7-1 against C12, 8-0 against Rain, and 7-1 against Router x Repair. Its 29-3 aggregate local result and 18-2 public record make C13 the strongest local challenger, although both samples remain provisional.

[C14 Late Crop Weed Recovery](https://www.kaggle.com/code/beicicc/kaggriculture-c14-late-crop-weed-recovery) adds a narrow visible-state repair when a late-day hired hand is scheduled to plant strawberry or melon on a weed. All eight high-weed robustness games completed with nine successful recoveries, no invalid actions, and no newly blocked crop batch; the head-to-head result was 4-4 with mean margin +597 and is treated as a safety check rather than superiority evidence. On default settings C14 matched C13 exactly across four paired seeds and went 8-0 against Rain with mean margin +3,036. Its 9-0 opening public record remains a small, provisional sample.

[C15 Post Demand Liquidation Timing](https://www.kaggle.com/code/beicicc/kaggriculture-c15-post-demand-liquidation-timing) preserves the planned step-680 market purchase while deferring observation-driven shed liquidation to step 681, after town demand has been applied. Across eight fresh two-seat seed pairs against C14, every paired margin change was positive: +6, +8, +2, +12, +6, +2, +7, and +10. Matched candidate/control checks against Rain and C12 were non-negative on every seed, all episodes completed without invalid actions, and terminal sellable inventory remained zero. No tested win/loss outcome changed, so C15 is treated as a conservative late-game score refinement rather than a broad strategic improvement. Validation episode 89677470 completed in an exact 102180-102180 self-play tie.

[C16 Swap Ends Market Order](https://www.kaggle.com/code/beicicc/kaggriculture-c15-post-demand-liquidation-timing) is published as Version 2 on the same Code page. It changes only the order of six existing market orders at step 649: the MELON sale moves first and the WHEAT sale moves last, while the order set, quantities, and execution turn remain unchanged. On independent eight-seed, two-seat confirmation sets, the paired margin changes totaled +8,792 against C15, +5,404 against Moon, and +22 against Rain, with no negative seed pair. A separate 12-seed Rain regression set also had no negative pair. Exact counterfactual evaluation on seven initial and 31 newly held-out public replays produced 34 positive and four zero margin changes, with no negative result. Every tested episode completed, the market-order cap was respected, and terminal sellable inventory remained zero. Validation episode 89829740 completed in a 102180-102180 tie.

C17 Kaito v18 Terminal Projection was not published as Kaggle Code because its official execution failed the online behavior gate. Kaito Fukami's attributed Apache-2.0 [public v18 source](https://www.kaggle.com/code/kaitofukami/40-53-top-10-future-holdout-v18-closed-loop?scriptVersionId=340030138) and the terminal projection passed 80 fresh local games with a 78-2 record, no invalid actions, and zero remaining sellable inventory. However, official validation episode 89842715 ended 3000-3000 and the first public episode ended 3000-58567. The raw-source loader had selected a later two-argument helper instead of the intended policy entrypoint: redefining an existing callable name did not move its insertion position, while the newly named helper became the last callable. C18 therefore adds a raw-file loader test that requires one uniquely selected entrypoint and verifies its first action before any release.

[C18 Online Entrypoint Safe](https://www.kaggle.com/code/beicicc/kaggriculture-c18-online-entrypoint-safe) is published as Version 3 of the rolling Code page. It changes no strategic action: a uniquely named one-argument entrypoint is added at the end of the raw source so Kaggle's loader selects the intended policy. Exact raw-file loading on 80 fresh games across five references finished 79-1, with no invalid actions, market-cap violations, action drift, or terminal sellable inventory. Three official failure observation streams, totaling 2,157 decisions, matched the named policy exactly after the fix. Official validation episode 89845822 finished 111283-110886, and the first public episode was won 172377-15685. The downloaded public Code source exactly matches submitted SHA-256 `603175d39f28` and retains the Apache-2.0 source attribution and modification notice.

[C19 Reproducibility Control](https://www.kaggle.com/code/beicicc/kaggriculture-c19-reproducibility-control) is an exact-byte repeat of C18, published as Version 4 of the rolling Code page. Before freezing the control, two proposed simplifications were rejected: disabling the closed-loop market reduced aggregate margin by 314 across 96 matched seed pairs, while a narrower same-multiset SELL permutation reduced aggregate margin by 229 across 64 fresh pairs. The submitted control therefore preserves the stronger verified policy unchanged. Its release matched C18 byte for byte, passed fresh module-state isolation, and reproduced actions, terminal states, rewards, and statuses on two new seeds in both seats. Official validation episode 89851756 matched the submitted source on all 719 actions per seat; the first public episode was won 195789-22237. The downloaded public Code source again matches SHA-256 `603175d39f28`.
