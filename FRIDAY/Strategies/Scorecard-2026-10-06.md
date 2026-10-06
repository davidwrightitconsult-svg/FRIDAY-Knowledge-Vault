---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-06"
created: "2026-10-06T00:14:09+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-06

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 3892 | 3696 | 30% | -0.81 | -0.97 … -0.65 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 464 | 405 | 40% | -0.84 | -3.46 … +1.79 | -4% | INCONCLUSIVE |
| MOMENTUM | 6h | 252 | 223 | 48% | -2.85 | -6.03 … +0.34 | -8% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 380 | 328 | 75% | -0.55 | -2.68 … +1.58 | -1% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 12 | 3 | 100% | +14.70 | +9.07 … +20.33 | 18% | INSUFFICIENT_DATA (27 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.35 · 1008 | -0.99 · 2540 | -0.89 · 148 |
| MEAN_REVERSION | -3.24 · 35 | -0.82 · 352 | +3.59 · 18 |
| MOMENTUM | +2.21 · 15 | -3.42 · 199 | +1.37 · 9 |
| LONGSHOT_BIAS | -0.54 · 222 | — · 0 | -0.58 · 106 |
| CALIBRATION_EDGE | — · 0 | +14.70 · 3 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 997 | +14.74 | +12.53 … +16.95 | 67% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 285 | -0.87 | -5.90 … +4.16 | 38% | INCONCLUSIVE |
| MOMENTUM | 144 | -1.23 | -8.05 … +5.59 | 62% | INCONCLUSIVE |
| LONGSHOT_BIAS | 220 | +0.35 | -2.75 … +3.45 | 94% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 3 | +14.70 | +9.07 … +20.33 | 100% | INSUFFICIENT_DATA (27 more scored signals needed) |

## Market calibration — price 24h before resolution

26905 samples from 13484 resolved markets · Brier 0.067 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 7250 | 7250 | 0.5% | 0.4% | 0.3% … 0.6% | -0.1pp | CONSISTENT |
| 0.02-0.05 | 1387 | 1387 | 3.2% | 3.6% | 2.8% … 4.7% | +0.4pp | CONSISTENT |
| 0.05-0.10 | 1025 | 1025 | 7.2% | 8.0% | 6.5% … 9.8% | +0.8pp | CONSISTENT |
| 0.10-0.20 | 1176 | 1176 | 14.4% | 15.9% | 13.9% … 18.1% | +1.5pp | CONSISTENT |
| 0.20-0.30 | 806 | 806 | 24.7% | 27.3% | 24.3% … 30.5% | +2.5pp | CONSISTENT |
| 0.30-0.40 | 715 | 715 | 34.8% | 33.0% | 29.7% … 36.5% | -1.8pp | CONSISTENT |
| 0.40-0.50 | 984 | 983 | 45.8% | 44.8% | 41.7% … 47.9% | -0.9pp | CONSISTENT |
| 0.50-0.60 | 1198 | 1080 | 53.3% | 54.1% | 51.3% … 56.9% | +0.8pp | CONSISTENT |
| 0.60-0.70 | 709 | 709 | 64.8% | 66.3% | 62.7% … 69.7% | +1.5pp | CONSISTENT |
| 0.70-0.80 | 815 | 815 | 74.9% | 73.0% | 69.9% … 75.9% | -1.9pp | CONSISTENT |
| 0.80-0.90 | 1147 | 1147 | 85.3% | 83.3% | 81.0% … 85.3% | -2.0pp | CONSISTENT |
| 0.90-0.95 | 1035 | 1035 | 92.6% | 92.1% | 90.3% … 93.6% | -0.5pp | CONSISTENT |
| 0.95-0.98 | 1378 | 1378 | 96.7% | 96.1% | 94.9% … 97.0% | -0.6pp | CONSISTENT |
| 0.98-1.00 | 7280 | 7280 | 99.5% | 99.6% | 99.4% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 9662 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 9693 samples, priced 98.4%, won 98.3% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
