---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-02"
created: "2026-10-02T00:07:39+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-02

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 1962 | 1818 | 35% | -0.96 | -1.26 … -0.67 | -4% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 363 | 317 | 41% | -0.41 | -4.16 … +3.35 | -5% | INCONCLUSIVE |
| MOMENTUM | 6h | 178 | 152 | 59% | -0.37 | -4.72 … +3.97 | -5% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 281 | 207 | 83% | -0.82 | -3.75 … +2.12 | -1% | INCONCLUSIVE |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.48 · 597 | -1.25 · 1137 | -0.48 · 84 |
| MEAN_REVERSION | -2.64 · 34 | -0.27 · 271 | +2.83 · 12 |
| MOMENTUM | +2.87 · 15 | -0.94 · 129 | +2.68 · 8 |
| LONGSHOT_BIAS | -0.01 · 143 | — · 0 | -2.63 · 64 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | Win rate |
|---|---|---|---|
| BOOK_IMBALANCE | 628 | +1.86 | 54% |
| MEAN_REVERSION | 252 | +0.77 | 40% |
| MOMENTUM | 120 | +0.46 | 65% |
| LONGSHOT_BIAS | 162 | -0.66 | 93% |

## Market calibration — price 24h before resolution

2787 samples from 1404 resolved markets · Brier 0.0421 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 676 | 676 | 0.5% | 0.0% | 0.0% … 0.6% | -0.5pp | CONSISTENT |
| 0.02-0.05 | 187 | 187 | 3.2% | 1.6% | 0.5% … 4.6% | -1.6pp | CONSISTENT |
| 0.05-0.10 | 117 | 117 | 7.1% | 1.7% | 0.5% … 6.0% | -5.4pp | OVERPRICED |
| 0.10-0.20 | 161 | 161 | 14.2% | 1.2% | 0.3% … 4.4% | -13.0pp | OVERPRICED |
| 0.20-0.30 | 90 | 90 | 24.9% | 12.2% | 7.0% … 20.6% | -12.7pp | OVERPRICED |
| 0.30-0.40 | 87 | 87 | 35.2% | 34.5% | 25.3% … 44.9% | -0.7pp | CONSISTENT |
| 0.40-0.50 | 78 | 78 | 43.9% | 29.5% | 20.5% … 40.4% | -14.4pp | OVERPRICED |
| 0.50-0.60 | 77 | 75 | 55.4% | 70.1% | 59.2% … 79.2% | +14.7pp | UNDERPRICED |
| 0.60-0.70 | 85 | 85 | 64.1% | 63.5% | 52.9% … 73.0% | -0.6pp | CONSISTENT |
| 0.70-0.80 | 95 | 95 | 74.6% | 88.4% | 80.5% … 93.4% | +13.9pp | UNDERPRICED |
| 0.80-0.90 | 157 | 157 | 85.5% | 98.1% | 94.5% … 99.4% | +12.6pp | UNDERPRICED |
| 0.90-0.95 | 119 | 119 | 92.7% | 98.3% | 94.1% … 99.5% | +5.6pp | UNDERPRICED |
| 0.95-0.98 | 182 | 182 | 96.7% | 98.4% | 95.3% … 99.4% | +1.7pp | CONSISTENT |
| 0.98-1.00 | 676 | 676 | 99.5% | 100.0% | 99.4% … 100.0% | +0.5pp | CONSISTENT |

**Long shots (< 10¢):** 980 samples, priced 1.8%, won 0.5% → OVERPRICED

**Favourites (≥ 90¢):** 977 samples, priced 98.1%, won 99.5% → UNDERPRICED

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
