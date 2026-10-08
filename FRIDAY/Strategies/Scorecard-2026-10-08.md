---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-08"
created: "2026-10-08T00:13:11+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-08

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 4105 | 3947 | 25% | -0.68 | -0.80 … -0.55 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 355 | 301 | 42% | +0.00 | -2.42 … +2.42 | -2% | INCONCLUSIVE |
| MOMENTUM | 6h | 211 | 188 | 41% | -3.61 | -6.82 … -0.40 | -7% | NEGATIVE_AFTER_COSTS |
| LONGSHOT_BIAS | 24h | 317 | 233 | 62% | -0.39 | -2.34 … +1.55 | -0% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 12 | 6 | 83% | +6.15 | -20.30 … +32.60 | 8% | INSUFFICIENT_DATA (26 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.26 · 990 | -0.80 · 2838 | -1.28 · 119 |
| MEAN_REVERSION | -2.85 · 23 | +0.23 · 265 | +0.29 · 13 |
| MOMENTUM | +0.95 · 8 | -3.86 · 174 | -2.48 · 6 |
| LONGSHOT_BIAS | -0.30 · 176 | -1.00 · 1 | -0.66 · 56 |
| CALIBRATION_EDGE | — · 0 | +6.15 · 6 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 709 | +17.09 | +14.27 … +19.92 | 68% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 163 | +0.94 | -6.05 … +7.93 | 40% | INCONCLUSIVE |
| MOMENTUM | 84 | -1.82 | -11.95 … +8.30 | 61% | INCONCLUSIVE |
| LONGSHOT_BIAS | 106 | +1.47 | -2.55 … +5.49 | 95% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 4 | -3.97 | -40.79 … +32.84 | 75% | INSUFFICIENT_DATA (26 more scored signals needed) |

## Market calibration — price 24h before resolution

33627 samples from 16893 resolved markets · Brier 0.0656 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 9111 | 9111 | 0.5% | 0.4% | 0.3% … 0.6% | -0.1pp | CONSISTENT |
| 0.02-0.05 | 1801 | 1801 | 3.2% | 3.5% | 2.8% … 4.5% | +0.4pp | CONSISTENT |
| 0.05-0.10 | 1277 | 1277 | 7.1% | 8.3% | 6.9% … 9.9% | +1.2pp | CONSISTENT |
| 0.10-0.20 | 1431 | 1431 | 14.4% | 15.7% | 13.9% … 17.7% | +1.3pp | CONSISTENT |
| 0.20-0.30 | 989 | 989 | 24.7% | 26.6% | 23.9% … 29.4% | +1.9pp | CONSISTENT |
| 0.30-0.40 | 882 | 882 | 34.9% | 33.2% | 30.2% … 36.4% | -1.7pp | CONSISTENT |
| 0.40-0.50 | 1207 | 1206 | 45.7% | 44.1% | 41.3% … 46.9% | -1.6pp | CONSISTENT |
| 0.50-0.60 | 1443 | 1309 | 53.3% | 54.9% | 52.3% … 57.4% | +1.5pp | CONSISTENT |
| 0.60-0.70 | 879 | 879 | 64.8% | 66.1% | 62.9% … 69.2% | +1.3pp | CONSISTENT |
| 0.70-0.80 | 992 | 992 | 75.0% | 73.4% | 70.5% … 76.0% | -1.6pp | CONSISTENT |
| 0.80-0.90 | 1407 | 1407 | 85.3% | 83.6% | 81.6% … 85.4% | -1.7pp | CONSISTENT |
| 0.90-0.95 | 1281 | 1281 | 92.7% | 91.7% | 90.1% … 93.1% | -0.9pp | CONSISTENT |
| 0.95-0.98 | 1796 | 1796 | 96.7% | 96.2% | 95.2% … 97.0% | -0.6pp | CONSISTENT |
| 0.98-1.00 | 9131 | 9131 | 99.5% | 99.6% | 99.4% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 12189 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 12208 samples, priced 98.4%, won 98.3% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
