---
type: "risk-doctrine"
title: "FRIDAY Risk Doctrine"
owner: "David Wright"
version: "1.0"
status: "seeded"
---

# FRIDAY Risk Doctrine

> Seeded by FRIDAY (Phase 4A) from the project record. **Owned by David.**
> The numeric limits that are actually enforced live in configuration and
> the Risk Governor code, not in this note.

## Principles
1. **Survival first.** A strategy that can ruin the account is rejected,
   whatever its expected return.
2. **Prove expectancy before risking capital.** Research → backtest →
   paper → shadow → controlled live, each gate signed off.
3. **No martingale.** Never increase size to recover losses.
4. **No uncontrolled leverage.**
5. **NO_TRADE is always acceptable.** No edge, no trade.
6. **Growth targets never justify risk.** A bankroll target is an
   aspiration, not a reason to raise exposure.
7. **The Risk Governor has the final vote** over any model, operator
   convenience, or schedule.

## Controls (configured, enforced in code)
| Control | Config key | Current default |
|---|---|---|
| Risk per trade | `RISK_PER_TRADE` | 1% of bankroll |
| Max daily loss | `MAX_DAILY_LOSS` | 5% |
| Max drawdown | `MAX_DRAWDOWN` | 15% |
| Max open exposure | `MAX_OPEN_EXPOSURE` | 25% |
| Minimum edge | `MIN_EDGE` | 0.05 |
| Minimum liquidity | `MIN_LIQUIDITY` | 100 |
| Live trading | `LIVE_TRADING_ENABLED` | hard-disabled in code |

## Kill switches
- Hermes kill switch: `POST /api/hermes/kill` — stops all automated work;
  restart requires a named human reset.
- Execution Gate: LOCKED; no code path exists to place an order.
