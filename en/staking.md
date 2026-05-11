🌐 **English** · [中文](https://oddfi.gitbook.io/oddfi-docs-zh/staking) · [日本語](https://oddfi.gitbook.io/oddfi-docs-ja/staking) · [한국어](https://oddfi.gitbook.io/oddfi-docs-ko/staking)

---

# ODD Staking

Lock up ODD to share the platform's payout-tax dividend and unlock higher daily betting limits (VIP tiers).

### Yield Sources

| Source | Description |
|---|---|
| Payout tax 2pp | Auto-injected into the StakingPool reward pool with every winning payout |
| Early-redemption forfeitures | 100% of unclaimed yield from early redemptions returns to the reward pool |

Yield is distributed pro-rata: `user staked × multiplier / Σ(all users' staked × multipliers)` (standard rewardPerShare model).

### Lock-up Periods & Reward Multipliers

| Lock-up | Multiplier | Notes |
|---|---|---|
| 7 days | 1.0x | Short tier |
| 30 days | 1.0x | Base tier |
| 60 days | 1.8x | Mid tier |
| 90 days | 4.0x | Long tier |
| 180 days | 8.0x | Extended tier |
| 360 days | 15.0x | Annual tier — max incentive |

### Redemption Rules

- **Mature redemption**: principal 100% returned, yield claimed normally
- **Early redemption**: principal 100% returned, **yield 100% forfeited** to the reward pool

> No partial penalty schedule — early redemption forfeits all yield, period. Designed to incentivize commitment.

### Staking ↔ Bet Position Coupling

| Cumulative Open Exposure | Requirement |
|---|---|
| ≤ 5,000 ODD | No staking required, free betting |
| > 5,000 ODD | Cumulative open ≤ current effective stake (in ODD) |

### VIP Tiers

Real-time evaluation, no protection period — stake changes apply immediately. Conversion rate locked at $0.1 / ODD.

| Tier | Effective Stake Threshold (ODD) | Daily Bet Limit (ODD) | USD Equivalent |
|---|---:|---:|---:|
| Standard | 0 | 10,000 | $1,000 |
| VIP 1 | ≥ 1,000 | 50,000 | $5,000 |
| VIP 2 | ≥ 5,000 | 100,000 | $10,000 |
| VIP 3 | ≥ 20,000 | 150,000 | $15,000 |
| VIP 4 | ≥ 50,000 | 200,000 | $20,000 |
| VIP 5 | ≥ 100,000 | 250,000 | $25,000 |
| VIP 6 | ≥ 200,000 | 300,000 | $30,000 |
| VIP 7 | ≥ 500,000 | 400,000 | $40,000 |
| VIP 8 | ≥ 1,000,000 | 500,000 | $50,000 |
| VIP 9 | ≥ 2,000,000 | 750,000 | $75,000 |
| VIP 10 | ≥ 5,000,000 | 1,000,000 | $100,000 |

---
