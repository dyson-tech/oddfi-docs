🌐 **English** · [中文](https://oddfi.gitbook.io/oddfi-docs-zh/liquidity)

---

# Liquidity Provision (Market Making)

Provide ODD to the Betting Pool and become the platform's counterparty liquidity. When users win, the Betting Pool pays out; when users lose, the funds enter the Pool. Liquidity providers share the platform's overall profit pro-rata.

### Reward Composition

| Item | Description |
|---|---|
| LP yield | Platform-wide Margin × 80%, distributed by share |
| Platform yield | Platform-wide Margin × 20% |
| Safety buffer | Payout tax 1pp (L3 buffer) continuously injected into the Betting Pool's internal reserve; L4 buffer pool from the strategic reserve provides additional backstop, strengthening solvency |

> After ODD's upgrade to Clean Token, the Betting Pool is no longer fed by a "sell profit tax 4pp". Capital safety relies on the initial 15M ODD lock-up principal + L3 buffer + L4 buffer pool.

Yield distributed by "your deposit / total pool size" ratio.

> **Target annualized yield ≈ 40%–80% APY**, varying with platform volume, user hit-rate, and your lock-up multiplier. Not a guarantee.

### Risk Control Module

The Betting Pool has a built-in dynamic odds adjustment mechanism. Compared with fixed-odds designs, it offers three core advantages:

| Advantage | Description |
|---|---|
| Auto-balance exposure | Real-time monitoring of fund distribution per market; odds auto-adjust to balance potential payouts on both sides |
| Cap extreme risk | When one-sided betting on a single match approaches the cap, odds converge quickly to prevent single-side arbitrage of the pool |
| Multi-layer defense | Signal-light system + L3 tax buffer + L4 buffer pool absorb abnormal volatility in tiers |

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

LPs bear the platform's overall loss risk. If user hit-rates spike during a period and the Betting Pool sees net outflow, LPs may face temporarily negative returns. The platform mitigates exposure via dynamic odds shifting, the signal-light system, and the L3 tax buffer + L4 buffer pool as multi-layer backstop.

---
