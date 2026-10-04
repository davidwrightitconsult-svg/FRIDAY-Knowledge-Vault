---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-04"
created: "2026-10-04T00:12:01+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-04

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 3196 | 3018 | 34% | -0.81 | -1.00 … -0.61 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 496 | 442 | 42% | -0.06 | -3.01 … +2.90 | -3% | INCONCLUSIVE |
| MOMENTUM | 6h | 252 | 227 | 54% | -1.56 | -5.00 … +1.89 | -6% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 380 | 337 | 81% | -0.76 | -3.00 … +1.48 | -1% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 9 | 2 | 100% | +16.65 | +9.50 … +23.80 | 20% | INSUFFICIENT_DATA (28 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.38 · 941 | -1.02 · 1937 | -0.72 · 140 |
| MEAN_REVERSION | -2.87 · 40 | +0.11 · 384 | +2.66 · 18 |
| MOMENTUM | +2.74 · 19 | -2.03 · 197 | -0.41 · 11 |
| LONGSHOT_BIAS | -0.12 · 229 | — · 0 | -2.13 · 108 |
| CALIBRATION_EDGE | — · 0 | +16.65 · 2 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 880 | +5.62 | +3.58 … +7.66 | 57% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 331 | +0.84 | -3.75 … +5.44 | 40% | INCONCLUSIVE |
| MOMENTUM | 165 | -1.47 | -7.68 … +4.74 | 63% | INCONCLUSIVE |
| LONGSHOT_BIAS | 246 | -0.29 | -3.35 … +2.78 | 94% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 2 | +16.65 | +9.50 … +23.80 | 100% | INSUFFICIENT_DATA (28 more scored signals needed) |

## Market calibration — price 24h before resolution

18753 samples from 9399 resolved markets · Brier 0.0694 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 4817 | 4817 | 0.5% | 0.5% | 0.3% … 0.7% | +0.0pp | CONSISTENT |
| 0.02-0.05 | 1011 | 1011 | 3.2% | 3.9% | 2.8% … 5.2% | +0.6pp | CONSISTENT |
| 0.05-0.10 | 761 | 761 | 7.2% | 8.7% | 6.9% … 10.9% | +1.5pp | CONSISTENT |
| 0.10-0.20 | 865 | 865 | 14.4% | 14.0% | 11.8% … 16.5% | -0.4pp | CONSISTENT |
| 0.20-0.30 | 579 | 579 | 24.8% | 24.9% | 21.5% … 28.5% | +0.0pp | CONSISTENT |
| 0.30-0.40 | 546 | 546 | 34.9% | 31.5% | 27.8% … 35.5% | -3.4pp | CONSISTENT |
| 0.40-0.50 | 719 | 718 | 45.6% | 43.2% | 39.7% … 46.9% | -2.4pp | CONSISTENT |
| 0.50-0.60 | 875 | 788 | 53.4% | 55.5% | 52.2% … 58.8% | +2.2pp | CONSISTENT |
| 0.60-0.70 | 540 | 540 | 64.7% | 67.4% | 63.3% … 71.2% | +2.7pp | CONSISTENT |
| 0.70-0.80 | 587 | 587 | 74.8% | 75.3% | 71.7% … 78.6% | +0.5pp | CONSISTENT |
| 0.80-0.90 | 841 | 841 | 85.3% | 85.4% | 82.8% … 87.6% | +0.1pp | CONSISTENT |
| 0.90-0.95 | 775 | 775 | 92.6% | 91.5% | 89.3% … 93.2% | -1.1pp | CONSISTENT |
| 0.95-0.98 | 1001 | 1001 | 96.7% | 95.9% | 94.5% … 97.0% | -0.8pp | CONSISTENT |
| 0.98-1.00 | 4836 | 4836 | 99.5% | 99.5% | 99.3% … 99.7% | +0.0pp | CONSISTENT |

**Long shots (< 10¢):** 6589 samples, priced 1.7%, won 2.0% → CONSISTENT

**Favourites (≥ 90¢):** 6612 samples, priced 98.3%, won 98.0% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
