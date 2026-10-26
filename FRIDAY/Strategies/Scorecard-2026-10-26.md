---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-26"
created: "2026-10-26T23:39:34+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-26

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 4188 | 4038 | 23% | -0.61 | -0.71 … -0.50 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 309 | 256 | 44% | -0.27 | -2.19 … +1.65 | -2% | INCONCLUSIVE |
| MOMENTUM | 6h | 181 | 161 | 38% | -3.44 | -6.30 … -0.58 | -6% | NEGATIVE_AFTER_COSTS |
| LONGSHOT_BIAS | 24h | 309 | 216 | 57% | +0.10 | -1.45 … +1.66 | 0% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 13 | 6 | 83% | +6.15 | -20.30 … +32.60 | 8% | INSUFFICIENT_DATA (26 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.25 · 980 | -0.70 · 2936 | -1.25 · 122 |
| MEAN_REVERSION | -2.69 · 14 | -0.12 · 229 | -0.35 · 13 |
| MOMENTUM | +0.95 · 8 | -3.72 · 147 | -2.48 · 6 |
| LONGSHOT_BIAS | +0.09 · 166 | +4.00 · 2 | -0.02 · 48 |
| CALIBRATION_EDGE | — · 0 | +6.15 · 6 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 596 | +17.42 | +14.18 … +20.66 | 67% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 118 | +1.14 | -6.95 … +9.23 | 43% | INCONCLUSIVE |
| MOMENTUM | 68 | -1.15 | -12.55 … +10.25 | 62% | INCONCLUSIVE |
| LONGSHOT_BIAS | 81 | +2.77 | -1.33 … +6.87 | 96% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 4 | -3.97 | -40.79 … +32.84 | 75% | INSUFFICIENT_DATA (26 more scored signals needed) |

## Market calibration — price 24h before resolution

36092 samples from 18333 resolved markets · Brier 0.0665 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 9763 | 9763 | 0.5% | 0.4% | 0.3% … 0.5% | -0.1pp | CONSISTENT |
| 0.02-0.05 | 1896 | 1896 | 3.2% | 3.6% | 2.8% … 4.5% | +0.4pp | CONSISTENT |
| 0.05-0.10 | 1370 | 1370 | 7.2% | 8.5% | 7.2% … 10.1% | +1.4pp | UNDERPRICED |
| 0.10-0.20 | 1548 | 1548 | 14.4% | 16.1% | 14.3% … 18.0% | +1.7pp | CONSISTENT |
| 0.20-0.30 | 1062 | 1062 | 24.7% | 27.0% | 24.4% … 29.8% | +2.3pp | CONSISTENT |
| 0.30-0.40 | 960 | 960 | 34.9% | 33.4% | 30.5% … 36.5% | -1.4pp | CONSISTENT |
| 0.40-0.50 | 1318 | 1317 | 45.8% | 44.0% | 41.3% … 46.7% | -1.8pp | CONSISTENT |
| 0.50-0.60 | 1574 | 1433 | 53.3% | 55.0% | 52.5% … 57.4% | +1.6pp | CONSISTENT |
| 0.60-0.70 | 959 | 959 | 64.8% | 65.6% | 62.5% … 68.5% | +0.8pp | CONSISTENT |
| 0.70-0.80 | 1063 | 1063 | 75.0% | 72.9% | 70.2% … 75.5% | -2.1pp | CONSISTENT |
| 0.80-0.90 | 1517 | 1517 | 85.3% | 83.2% | 81.2% … 85.0% | -2.1pp | OVERPRICED |
| 0.90-0.95 | 1388 | 1388 | 92.7% | 91.8% | 90.2% … 93.1% | -0.9pp | CONSISTENT |
| 0.95-0.98 | 1895 | 1895 | 96.7% | 96.2% | 95.2% … 96.9% | -0.6pp | CONSISTENT |
| 0.98-1.00 | 9779 | 9779 | 99.5% | 99.6% | 99.5% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 13029 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 13062 samples, priced 98.4%, won 98.3% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
