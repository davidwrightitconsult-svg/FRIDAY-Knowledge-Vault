---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-09-29"
created: "2026-09-29T00:04:54+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-09-29

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 387 | 347 | 39% | -0.29 | -0.85 … +0.28 | -2% | INCONCLUSIVE |
| MEAN_REVERSION | 6h | 94 | 80 | 45% | +2.30 | -6.14 … +10.75 | 3% | INCONCLUSIVE |
| MOMENTUM | 6h | 46 | 34 | 59% | -2.79 | -11.92 … +6.33 | -11% | INCONCLUSIVE |
| LONGSHOT_BIAS | 24h | 61 | 0 | — | — | — | — | INSUFFICIENT_DATA (30 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.33 · 133 | -0.19 · 192 | -0.81 · 22 |
| MEAN_REVERSION | -2.59 · 10 | +3.38 · 67 | -5.47 · 3 |
| MOMENTUM | +4.08 · 5 | -4.06 · 26 | -3.27 · 3 |
| LONGSHOT_BIAS | — · 0 | — · 0 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | Win rate |
|---|---|---|---|
| BOOK_IMBALANCE | 72 | -7.13 | 43% |
| MEAN_REVERSION | 56 | +4.37 | 43% |
| MOMENTUM | 18 | -2.97 | 61% |
| LONGSHOT_BIAS | 0 | — | — |

## Market calibration — price 24h before resolution

2713 samples from 1367 resolved markets · Brier 0.0417 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 661 | 661 | 0.5% | 0.0% | 0.0% … 0.6% | -0.5pp | CONSISTENT |
| 0.02-0.05 | 182 | 182 | 3.2% | 1.1% | 0.3% … 3.9% | -2.1pp | CONSISTENT |
| 0.05-0.10 | 113 | 113 | 7.1% | 1.8% | 0.5% … 6.2% | -5.3pp | OVERPRICED |
| 0.10-0.20 | 156 | 156 | 14.3% | 1.3% | 0.4% … 4.5% | -13.0pp | OVERPRICED |
| 0.20-0.30 | 86 | 86 | 24.9% | 12.8% | 7.3% … 21.5% | -12.1pp | OVERPRICED |
| 0.30-0.40 | 84 | 84 | 35.2% | 34.5% | 25.2% … 45.2% | -0.7pp | CONSISTENT |
| 0.40-0.50 | 77 | 77 | 44.0% | 29.9% | 20.8% … 40.8% | -14.1pp | OVERPRICED |
| 0.50-0.60 | 76 | 74 | 55.4% | 69.7% | 58.7% … 78.9% | +14.3pp | UNDERPRICED |
| 0.60-0.70 | 82 | 82 | 64.0% | 63.4% | 52.6% … 73.0% | -0.6pp | CONSISTENT |
| 0.70-0.80 | 91 | 91 | 74.6% | 87.9% | 79.6% … 93.1% | +13.3pp | UNDERPRICED |
| 0.80-0.90 | 153 | 153 | 85.5% | 98.0% | 94.4% … 99.3% | +12.6pp | UNDERPRICED |
| 0.90-0.95 | 114 | 114 | 92.8% | 98.2% | 93.8% … 99.5% | +5.5pp | UNDERPRICED |
| 0.95-0.98 | 177 | 177 | 96.7% | 98.9% | 96.0% … 99.7% | +2.2pp | CONSISTENT |
| 0.98-1.00 | 661 | 661 | 99.5% | 100.0% | 99.4% … 100.0% | +0.5pp | CONSISTENT |

**Long shots (< 10¢):** 956 samples, priced 1.8%, won 0.4% → OVERPRICED

**Favourites (≥ 90¢):** 952 samples, priced 98.1%, won 99.6% → UNDERPRICED

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
