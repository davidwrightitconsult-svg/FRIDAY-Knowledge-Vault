---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-01"
created: "2026-10-01T00:06:49+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-01

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 1354 | 1251 | 36% | -0.90 | -1.23 … -0.56 | -4% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 258 | 238 | 42% | -0.27 | -4.90 … +4.36 | -1% | INCONCLUSIVE |
| MOMENTUM | 6h | 127 | 117 | 61% | +0.31 | -4.73 … +5.34 | -5% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 211 | 139 | 84% | -1.11 | -4.79 … +2.57 | -1% | INCONCLUSIVE |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.54 · 450 | -1.17 · 729 | -0.32 · 72 |
| MEAN_REVERSION | -2.47 · 23 | -0.22 · 205 | +3.66 · 10 |
| MOMENTUM | +2.25 · 12 | -0.06 · 98 | +2.06 · 7 |
| LONGSHOT_BIAS | +1.60 · 96 | — · 0 | -7.17 · 43 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | Win rate |
|---|---|---|---|
| BOOK_IMBALANCE | 305 | +2.02 | 45% |
| MEAN_REVERSION | 167 | +0.63 | 40% |
| MOMENTUM | 64 | +3.57 | 69% |
| LONGSHOT_BIAS | 97 | -1.00 | 93% |

## Market calibration — price 24h before resolution

2759 samples from 1390 resolved markets · Brier 0.0422 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 668 | 668 | 0.5% | 0.0% | 0.0% … 0.6% | -0.5pp | CONSISTENT |
| 0.02-0.05 | 185 | 185 | 3.2% | 1.6% | 0.5% … 4.7% | -1.6pp | CONSISTENT |
| 0.05-0.10 | 116 | 116 | 7.1% | 1.7% | 0.5% … 6.1% | -5.4pp | OVERPRICED |
| 0.10-0.20 | 159 | 159 | 14.3% | 1.3% | 0.4% … 4.5% | -13.0pp | OVERPRICED |
| 0.20-0.30 | 90 | 90 | 24.9% | 12.2% | 7.0% … 20.6% | -12.7pp | OVERPRICED |
| 0.30-0.40 | 86 | 86 | 35.2% | 33.7% | 24.6% … 44.2% | -1.5pp | CONSISTENT |
| 0.40-0.50 | 78 | 78 | 43.9% | 29.5% | 20.5% … 40.4% | -14.4pp | OVERPRICED |
| 0.50-0.60 | 77 | 75 | 55.4% | 70.1% | 59.2% … 79.2% | +14.7pp | UNDERPRICED |
| 0.60-0.70 | 84 | 84 | 64.1% | 64.3% | 53.6% … 73.7% | +0.2pp | CONSISTENT |
| 0.70-0.80 | 95 | 95 | 74.6% | 88.4% | 80.5% … 93.4% | +13.9pp | UNDERPRICED |
| 0.80-0.90 | 156 | 156 | 85.5% | 98.1% | 94.5% … 99.3% | +12.6pp | UNDERPRICED |
| 0.90-0.95 | 117 | 117 | 92.7% | 98.3% | 94.0% … 99.5% | +5.6pp | UNDERPRICED |
| 0.95-0.98 | 180 | 180 | 96.7% | 98.3% | 95.2% … 99.4% | +1.6pp | CONSISTENT |
| 0.98-1.00 | 668 | 668 | 99.5% | 100.0% | 99.4% … 100.0% | +0.5pp | CONSISTENT |

**Long shots (< 10¢):** 969 samples, priced 1.8%, won 0.5% → OVERPRICED

**Favourites (≥ 90¢):** 965 samples, priced 98.1%, won 99.5% → UNDERPRICED

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
