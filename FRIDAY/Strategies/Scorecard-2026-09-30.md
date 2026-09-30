---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-09-30"
created: "2026-09-30T00:05:33+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-09-30

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 840 | 765 | 38% | -0.77 | -1.19 … -0.35 | -4% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 186 | 157 | 41% | +0.69 | -5.20 … +6.58 | 3% | INCONCLUSIVE |
| MOMENTUM | 6h | 93 | 81 | 62% | -1.15 | -7.48 … +5.18 | -7% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 146 | 61 | 87% | -0.40 | -5.25 … +4.46 | -0% | INCONCLUSIVE |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.37 · 295 | -1.08 · 425 | -0.43 · 45 |
| MEAN_REVERSION | -2.20 · 17 | +0.65 · 133 | +8.51 · 7 |
| MOMENTUM | +2.18 · 11 | -1.74 · 66 | -0.45 · 4 |
| LONGSHOT_BIAS | +1.76 · 49 | — · 0 | -9.22 · 12 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | Win rate |
|---|---|---|---|
| BOOK_IMBALANCE | 215 | +0.36 | 45% |
| MEAN_REVERSION | 116 | +1.91 | 41% |
| MOMENTUM | 45 | +1.22 | 64% |
| LONGSHOT_BIAS | 38 | +0.56 | 95% |

## Market calibration — price 24h before resolution

2747 samples from 1384 resolved markets · Brier 0.0417 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 667 | 667 | 0.5% | 0.0% | 0.0% … 0.6% | -0.5pp | CONSISTENT |
| 0.02-0.05 | 184 | 184 | 3.2% | 1.1% | 0.3% … 3.9% | -2.1pp | CONSISTENT |
| 0.05-0.10 | 115 | 115 | 7.1% | 1.7% | 0.5% … 6.1% | -5.3pp | OVERPRICED |
| 0.10-0.20 | 156 | 156 | 14.3% | 1.3% | 0.4% … 4.5% | -13.0pp | OVERPRICED |
| 0.20-0.30 | 90 | 90 | 24.9% | 12.2% | 7.0% … 20.6% | -12.7pp | OVERPRICED |
| 0.30-0.40 | 86 | 86 | 35.2% | 33.7% | 24.6% … 44.2% | -1.5pp | CONSISTENT |
| 0.40-0.50 | 78 | 78 | 43.9% | 29.5% | 20.5% … 40.4% | -14.4pp | OVERPRICED |
| 0.50-0.60 | 77 | 75 | 55.4% | 70.1% | 59.2% … 79.2% | +14.7pp | UNDERPRICED |
| 0.60-0.70 | 84 | 84 | 64.1% | 64.3% | 53.6% … 73.7% | +0.2pp | CONSISTENT |
| 0.70-0.80 | 95 | 95 | 74.6% | 88.4% | 80.5% … 93.4% | +13.9pp | UNDERPRICED |
| 0.80-0.90 | 153 | 153 | 85.5% | 98.0% | 94.4% … 99.3% | +12.6pp | UNDERPRICED |
| 0.90-0.95 | 116 | 116 | 92.8% | 98.3% | 93.9% … 99.5% | +5.5pp | UNDERPRICED |
| 0.95-0.98 | 179 | 179 | 96.7% | 98.9% | 96.0% … 99.7% | +2.2pp | CONSISTENT |
| 0.98-1.00 | 667 | 667 | 99.5% | 100.0% | 99.4% … 100.0% | +0.5pp | CONSISTENT |

**Long shots (< 10¢):** 966 samples, priced 1.8%, won 0.4% → OVERPRICED

**Favourites (≥ 90¢):** 962 samples, priced 98.1%, won 99.6% → UNDERPRICED

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
