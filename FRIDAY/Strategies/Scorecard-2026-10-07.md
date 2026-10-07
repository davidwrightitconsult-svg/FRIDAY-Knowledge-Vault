---
type: "strategy-scorecard"
title: "Strategy scorecard 2026-10-07"
created: "2026-10-07T00:06:46+00:00"
source: "QUANT"
tags: ["friday/strategies", "friday/scorecard"]
execution_authorized: false
---

# Strategy scorecard — 2026-10-07

> [!note] Measured, not validated. Net = after crossing the spread at entry and exit.
> A PROMISING verdict still needs out-of-sample validation (Phases 8-9). Execution is locked.

Window: last 30 days · minimum sample 30

| Strategy | Horizon | Signals | Scored | Hit rate | Avg net (¢) | 95% CI (¢) | Avg return on cost | Verdict |
|---|---|---|---|---|---|---|---|---|
| BOOK_IMBALANCE | 1h | 4018 | 3842 | 28% | -0.73 | -0.86 … -0.59 | -3% | NEGATIVE_AFTER_COSTS |
| MEAN_REVERSION | 6h | 401 | 340 | 41% | -0.29 | -2.85 … +2.28 | -3% | INCONCLUSIVE |
| MOMENTUM | 6h | 222 | 198 | 43% | -3.81 | -7.05 … -0.57 | -8% | NEGATIVE_AFTER_COSTS |
| LONGSHOT_BIAS | 24h | 347 | 281 | 69% | -0.21 | -2.21 … +1.78 | -0% | INCONCLUSIVE |
| CALIBRATION_EDGE | 24h | 12 | 6 | 83% | +6.15 | -20.30 … +32.60 | 8% | INSUFFICIENT_DATA (26 more scored signals needed) |

## By entry price band (avg net ¢ · scored)

| Strategy | <0.10 | 0.10-0.90 | >0.90 |
|---|---|---|---|
| BOOK_IMBALANCE | -0.34 · 993 | -0.85 · 2725 | -1.07 · 124 |
| MEAN_REVERSION | -3.01 · 27 | -0.03 · 299 | -0.45 · 14 |
| MOMENTUM | +2.66 · 10 | -4.30 · 181 | -0.53 · 7 |
| LONGSHOT_BIAS | -1.01 · 199 | -1.00 · 1 | +1.75 · 81 |
| CALIBRATION_EDGE | — · 0 | +6.15 · 6 | — · 0 |

## Held to resolution

| Strategy | Resolved | Avg net (¢) | 95% CI (¢) | Win rate | Verdict |
|---|---|---|---|---|---|
| BOOK_IMBALANCE | 876 | +16.74 | +14.32 … +19.17 | 68% | PROMISING (not validated — Phases 8-9) |
| MEAN_REVERSION | 223 | +0.02 | -5.74 … +5.77 | 40% | INCONCLUSIVE |
| MOMENTUM | 112 | -3.01 | -11.21 … +5.19 | 60% | INCONCLUSIVE |
| LONGSHOT_BIAS | 160 | +1.20 | -2.17 … +4.57 | 95% | INCONCLUSIVE |
| CALIBRATION_EDGE (judged here) | 4 | -3.97 | -40.79 … +32.84 | 75% | INSUFFICIENT_DATA (26 more scored signals needed) |

## Market calibration — price 24h before resolution

30362 samples from 15214 resolved markets · Brier 0.067 (no-skill 0.25)

| Price bin | Samples | Markets | Mean price | Actually won | 95% CI | Bias | Verdict |
|---|---|---|---|---|---|---|---|
| 0.00-0.02 | 8129 | 8129 | 0.5% | 0.4% | 0.3% … 0.6% | -0.0pp | CONSISTENT |
| 0.02-0.05 | 1598 | 1598 | 3.2% | 3.4% | 2.6% … 4.5% | +0.2pp | CONSISTENT |
| 0.05-0.10 | 1167 | 1167 | 7.2% | 8.5% | 7.0% … 10.2% | +1.3pp | CONSISTENT |
| 0.10-0.20 | 1316 | 1316 | 14.4% | 15.6% | 13.7% … 17.6% | +1.1pp | CONSISTENT |
| 0.20-0.30 | 928 | 928 | 24.7% | 26.9% | 24.2% … 29.9% | +2.3pp | CONSISTENT |
| 0.30-0.40 | 812 | 812 | 34.8% | 32.9% | 29.7% … 36.2% | -2.0pp | CONSISTENT |
| 0.40-0.50 | 1116 | 1115 | 45.8% | 44.4% | 41.5% … 47.4% | -1.3pp | CONSISTENT |
| 0.50-0.60 | 1338 | 1213 | 53.3% | 54.6% | 51.9% … 57.2% | +1.3pp | CONSISTENT |
| 0.60-0.70 | 809 | 809 | 64.8% | 66.4% | 63.0% … 69.5% | +1.6pp | CONSISTENT |
| 0.70-0.80 | 930 | 930 | 75.0% | 73.0% | 70.1% … 75.8% | -2.0pp | CONSISTENT |
| 0.80-0.90 | 1292 | 1292 | 85.3% | 83.8% | 81.6% … 85.7% | -1.5pp | CONSISTENT |
| 0.90-0.95 | 1176 | 1176 | 92.6% | 91.6% | 89.9% … 93.0% | -1.1pp | CONSISTENT |
| 0.95-0.98 | 1592 | 1592 | 96.7% | 96.3% | 95.2% … 97.1% | -0.4pp | CONSISTENT |
| 0.98-1.00 | 8159 | 8159 | 99.5% | 99.6% | 99.4% … 99.7% | +0.1pp | CONSISTENT |

**Long shots (< 10¢):** 10894 samples, priced 1.6%, won 1.7% → CONSISTENT

**Favourites (≥ 90¢):** 10927 samples, priced 98.4%, won 98.2% → CONSISTENT

## Hypotheses

- **BOOK_IMBALANCE** — Resting order-book depth heavily skewed to one side precedes a short-term drift toward the heavy side.
- **MEAN_REVERSION** — A sharp 1h move that is large relative to the market's own volatility is partly an over-reaction and reverses.
- **MOMENTUM** — A steady 6h trend, confirmed by the last hour, reflects information still being absorbed and continues.
- **LONGSHOT_BIAS** — Favourite-longshot bias: bettors over-pay for long shots and under-pay for heavy favourites.
- **CALIBRATION_EDGE** — The 8B fair-value model: a market is mispriced by its price band's measured, shrunk historical bias in its own segment (sports / field / binary).
