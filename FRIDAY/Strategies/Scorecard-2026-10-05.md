---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-05"
created: "2026-10-05T00:12:56+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-05

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 3751 | 3541 | 33% | -0.76 | -0.94 … -0.58 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 535 | 469 | 42% | -0.41 | -3.18 … +2.35 | -4% | INCONCLUSIVE |
| MOMENTUM | 6h | 282 | 247 | 53% | -2.37 | -5.68 … +0.93 | -7% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 423 | 357 | 78% | -0.75 | -2.87 … +1.37 | -1% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 9 | 2 | 100% | +16.65 | +9.50 … +23.80 | 20% | INSUFFICIENT_DATA (28 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.36 · 1042 | -0.94 · 2338 | -0.68 · 161 |
| MEAN_REVERSION | -2.73 · 43 | -0.30 · 408 | +2.66 · 18 |
| MOMENTUM | +2.61 · 20 | -2.98 · 215 | +0.21 · 12 |
| LONGSHOT_BIAS | -0.19 · 246 | — · 0 | -1.98 · 111 |
| CALIBRATION_EDGE | — · 0 | +16.65 · 2 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 881 | +5.62 | +3.58 … +7.66 | 57% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 331 | +0.14 | -4.42 … +4.70 | 39% | INCONCLUSIVE |
| MOMENTUM | 166 | -1.42 | -7.59 … +4.76 | 63% | INCONCLUSIVE |
| LONGSHOT_BIAS | 246 | -0.28 | -3.34 … +2.79 | 94% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 2 | +16.65 | +9.50 … +23.80 | 100% | INSUFFICIENT_DATA (28 more scored signals needed) |

## Market calibration — price 24h before resolution

22758 samples from 11406 resolved markets · Brier 0.0687 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 5983 | 5983 | 0.5% | 0.4% | 0.3% … 0.6% | -0.1pp | CONSISTENT |
| 0.02-0.05 | 1197 | 1197 | 3.2% | 3.3% | 2.5% … 4.5% | +0.1pp | CONSISTENT |
| 0.05-0.10 | 874 | 874 | 7.2% | 8.3% | 6.7% … 10.4% | +1.1pp | CONSISTENT |
| 0.10-0.20 | 1035 | 1035 | 14.4% | 15.5% | 13.4% … 17.8% | +1.0pp | CONSISTENT |
| 0.20-0.30 | 684 | 684 | 24.8% | 26.6% | 23.4% … 30.0% | +1.8pp | CONSISTENT |
| 0.30-0.40 | 633 | 633 | 34.8% | 32.1% | 28.5% … 35.8% | -2.8pp | CONSISTENT |
| 0.40-0.50 | 880 | 879 | 45.8% | 44.4% | 41.2% … 47.7% | -1.4pp | CONSISTENT |
| 0.50-0.60 | 1065 | 962 | 53.3% | 54.5% | 51.5% … 57.4% | +1.2pp | CONSISTENT |
| 0.60-0.70 | 625 | 625 | 64.8% | 67.2% | 63.4% … 70.8% | +2.4pp | CONSISTENT |
| 0.70-0.80 | 692 | 692 | 74.9% | 73.7% | 70.3% … 76.8% | -1.2pp | CONSISTENT |
| 0.80-0.90 | 1010 | 1010 | 85.3% | 83.7% | 81.3% … 85.8% | -1.6pp | CONSISTENT |
| 0.90-0.95 | 884 | 884 | 92.6% | 91.7% | 89.7% … 93.4% | -0.8pp | CONSISTENT |
| 0.95-0.98 | 1188 | 1188 | 96.7% | 96.3% | 95.1% … 97.2% | -0.4pp | CONSISTENT |
| 0.98-1.00 | 6008 | 6008 | 99.5% | 99.6% | 99.4% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 8054 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 8080 samples, priced 98.3%, won 98.2% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
