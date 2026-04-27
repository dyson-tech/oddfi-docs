# Liquidity Provision (Market Making)

Provide ODD to the Betting Pool and become the platform's counterparty liquidity. When users win, the Betting Pool pays out; when users lose, the funds enter the Pool. Liquidity providers share the platform's overall profit pro-rata.

### Reward Composition

| Item | Description |
|---|---|
| LP yield | Platform-wide Margin × 80%, distributed by share |
| Platform yield | Platform-wide Margin × 20% |
| Safety buffer | Payout tax 1pp (L3 buffer) continuously injected into the Betting Pool's internal reserve, strengthening solvency |

> After ODD's upgrade to Clean Token, the Betting Pool is no longer fed by a "sell profit tax 4pp". Capital safety relies on the initial 15M ODD lock-up principal + L3 buffer.

Yield distributed by "your deposit / total pool size" ratio.

### Lock-up Periods & Reward Multipliers

| Lock-up | Reward Multiplier |
|---|---|
| 7 days | 0.5x |
| 14 days | 1.0x |
| 28 days | 1.8x |
| 60 days | 2.5x |
| 90 days | 3.5x |

### Redemption Rules

- **Mature redemption**: principal 100% returned, accrued yield claimable
- **Early redemption**: principal 100% returned, **yield 100% forfeited**

### Risk Disclosure

LPs bear the platform's overall loss risk. If user hit-rates spike during a period and the Betting Pool sees net outflow, LPs may face temporarily negative returns. The platform mitigates exposure via dynamic odds shifting, the signal-light system, and the L3 tax buffer as additional backstop.

---
