---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-03"
created: "2026-10-03T00:05:43+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-03

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 2655 | 2468 | 34% | -0.85 | -1.09 … -0.61 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 455 | 398 | 42% | -0.01 | -3.28 … +3.26 | -3% | INCONCLUSIVE |
| MOMENTUM | 6h | 226 | 200 | 55% | -1.68 | -5.58 … +2.23 | -6% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 350 | 274 | 83% | -0.62 | -3.12 … +1.87 | -1% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 6 | 0 | — | — | — | — | INSUFFICIENT_DATA (30 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.41 · 798 | -1.09 · 1552 | -0.62 · 118 |
| MEAN_REVERSION | -2.82 · 38 | +0.15 · 343 | +3.05 · 17 |
| MOMENTUM | +2.88 · 16 | -2.14 · 175 | -0.73 · 9 |
| LONGSHOT_BIAS | -0.15 · 190 | — · 0 | -1.70 · 84 |
| CALIBRATION_EDGE | — · 0 | — · 0 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 730 | +2.24 | -0.00 … +4.48 | 54% | INCONCLUSIVE |
| MEAN_REVERSION | 326 | +0.92 | -3.73 … +5.56 | 40% | INCONCLUSIVE |
| MOMENTUM | 160 | -1.99 | -8.37 … +4.39 | 62% | INCONCLUSIVE |
| LONGSHOT_BIAS | 207 | -0.10 | -3.39 … +3.19 | 94% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 0 | — | — | — | INSUFFICIENT_DATA (30 more scored signals needed) |

## Market calibration — price 24h before resolution

4871 samples from 2446 resolved markets · Brier 0.0517 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 1230 | 1230 | 0.5% | 0.0% | 0.0% … 0.3% | -0.5pp | OVERPRICED |
| 0.02-0.05 | 314 | 314 | 3.2% | 1.6% | 0.7% … 3.7% | -1.6pp | CONSISTENT |
| 0.05-0.10 | 188 | 188 | 7.1% | 5.9% | 3.3% … 10.2% | -1.2pp | CONSISTENT |
| 0.10-0.20 | 229 | 229 | 14.1% | 4.4% | 2.4% … 7.8% | -9.8pp | OVERPRICED |
| 0.20-0.30 | 146 | 146 | 24.9% | 17.1% | 11.9% … 24.1% | -7.8pp | OVERPRICED |
| 0.30-0.40 | 153 | 153 | 34.9% | 32.7% | 25.8% … 40.5% | -2.2pp | CONSISTENT |
| 0.40-0.50 | 160 | 160 | 44.8% | 41.2% | 33.9% … 49.0% | -3.6pp | CONSISTENT |
| 0.50-0.60 | 195 | 175 | 53.9% | 57.4% | 50.4% … 64.2% | +3.5pp | CONSISTENT |
| 0.60-0.70 | 145 | 145 | 64.5% | 65.5% | 57.5% … 72.8% | +1.0pp | CONSISTENT |
| 0.70-0.80 | 157 | 157 | 74.6% | 82.8% | 76.1% … 87.9% | +8.2pp | UNDERPRICED |
| 0.80-0.90 | 218 | 218 | 85.5% | 95.0% | 91.2% … 97.2% | +9.4pp | UNDERPRICED |
| 0.90-0.95 | 194 | 194 | 92.6% | 94.3% | 90.1% … 96.8% | +1.7pp | CONSISTENT |
| 0.95-0.98 | 312 | 312 | 96.7% | 98.4% | 96.3% … 99.3% | +1.7pp | CONSISTENT |
| 0.98-1.00 | 1230 | 1230 | 99.5% | 100.0% | 99.7% … 100.0% | +0.5pp | UNDERPRICED |

**Long shots (< 10¢):** 1732 samples, priced 1.7%, won 0.9% → OVERPRICED

**Favourites (≥ 90¢):** 1736 samples, priced 98.2%, won 99.1% → UNDERPRICED

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
