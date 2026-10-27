---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-27"
created: "2026-10-27T00:09:12+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-27

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 4187 | 4037 | 23% | -0.61 | -0.71 … -0.50 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 309 | 256 | 44% | -0.27 | -2.19 … +1.65 | -2% | INCONCLUSIVE |
| MOMENTUM | 6h | 181 | 161 | 38% | -3.44 | -6.30 … -0.58 | -6% | NEGATIVE_AFTER_COSTS |
| LONGSHOT_BIAS | 24h | 310 | 216 | 57% | +0.10 | -1.45 … +1.66 | 0% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 13 | 6 | 83% | +6.15 | -20.30 … +32.60 | 8% | INSUFFICIENT_DATA (26 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.25 · 979 | -0.70 · 2936 | -1.25 · 122 |
| MEAN_REVERSION | -2.69 · 14 | -0.12 · 229 | -0.35 · 13 |
| MOMENTUM | +0.95 · 8 | -3.72 · 147 | -2.48 · 6 |
| LONGSHOT_BIAS | +0.09 · 166 | +4.00 · 2 | -0.02 · 48 |
| CALIBRATION_EDGE | — · 0 | +6.15 · 6 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 594 | +17.52 | +14.27 … +20.77 | 67% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 118 | +1.14 | -6.95 … +9.23 | 43% | INCONCLUSIVE |
| MOMENTUM | 68 | -1.15 | -12.55 … +10.25 | 62% | INCONCLUSIVE |
| LONGSHOT_BIAS | 81 | +2.77 | -1.33 … +6.87 | 96% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 4 | -3.97 | -40.79 … +32.84 | 75% | INSUFFICIENT_DATA (26 more scored signals needed) |

## Market calibration — price 24h before resolution

36615 samples from 18595 resolved markets · Brier 0.0673 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 9846 | 9846 | 0.5% | 0.4% | 0.3% … 0.5% | -0.1pp | CONSISTENT |
| 0.02-0.05 | 1924 | 1924 | 3.2% | 3.7% | 2.9% … 4.6% | +0.5pp | CONSISTENT |
| 0.05-0.10 | 1392 | 1392 | 7.2% | 8.6% | 7.2% … 10.1% | +1.4pp | UNDERPRICED |
| 0.10-0.20 | 1584 | 1584 | 14.4% | 16.2% | 14.5% … 18.1% | +1.8pp | UNDERPRICED |
| 0.20-0.30 | 1093 | 1093 | 24.7% | 27.1% | 24.5% … 29.8% | +2.4pp | CONSISTENT |
| 0.30-0.40 | 988 | 988 | 34.9% | 33.3% | 30.4% … 36.3% | -1.6pp | CONSISTENT |
| 0.40-0.50 | 1347 | 1346 | 45.7% | 43.9% | 41.2% … 46.5% | -1.9pp | CONSISTENT |
| 0.50-0.60 | 1609 | 1464 | 53.3% | 55.1% | 52.6% … 57.5% | +1.7pp | CONSISTENT |
| 0.60-0.70 | 989 | 989 | 64.8% | 65.7% | 62.7% … 68.6% | +1.0pp | CONSISTENT |
| 0.70-0.80 | 1092 | 1092 | 75.0% | 72.8% | 70.1% … 75.4% | -2.2pp | CONSISTENT |
| 0.80-0.90 | 1554 | 1554 | 85.3% | 83.1% | 81.1% … 84.9% | -2.2pp | OVERPRICED |
| 0.90-0.95 | 1410 | 1410 | 92.7% | 91.8% | 90.2% … 93.1% | -0.9pp | CONSISTENT |
| 0.95-0.98 | 1924 | 1924 | 96.7% | 96.0% | 95.1% … 96.8% | -0.7pp | CONSISTENT |
| 0.98-1.00 | 9863 | 9863 | 99.5% | 99.6% | 99.5% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 13162 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 13197 samples, priced 98.4%, won 98.3% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
