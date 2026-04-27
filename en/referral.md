🌐 **English** · [中文](https://oddfi.gitbook.io/oddfi-docs-zh/referral) · [日本語](https://oddfi.gitbook.io/oddfi-docs-ja/referral)

---

# Referral Rewards

After connecting your wallet, you automatically get a unique referral link. Referral relationships are bound on-chain permanently — once bound, immutable.

### Reward Sources

| Reward Type | Rule |
|---|---|
| Bet tax share | For each bet your referee places, you earn **1% ODD** of their bet principal |
| Payout tax share | For each winning payout to your referee, you earn **1% ODD** of the payout (1pp out of the 5pp payout tax) |
| Team-tier bonus | See S1–S5 ladder below |

> No staking threshold required to receive rewards. For users without a referrer, the 1% bet tax + 1pp payout tax share that would have gone to the referrer goes to the platform vault.

### Claim Mechanism (Important)

Referral rewards do not credit in real-time — they accumulate inside the BettingPool contract and you claim actively:

```
Referee bets/wins → BettingPool accumulates ODD into your Claim balance
  ↓
You check your claimable ODD balance
  ↓
Click Claim → contract swaps ODD → USDT live via PancakeSwap
  ↓
USDT lands directly in your wallet
```

| Item | Description |
|---|---|
| Minimum claim threshold | 10 ODD (prevents gas costs from eating small claims) |
| Swap route | PancakeSwap V2 Router (ODD → USDT) |
| Slippage protection | Default 2%, customizable (max 5%) |
| Gas | Paid by the referrer |
| Failure handling | Swap failure reverts the entire claim; ODD balance preserved |

> Design rationale: USDT settlement avoids exposing the referrer to ODD price volatility, and a single Claim event saves gas vs. many tiny transfers.

### Team-Tier Bonus

| Tier | Team Cumulative Bets | Team Bonus |
|---|---|---|
| — | < $10,000 | Base share only (1% bet tax + 1pp payout tax), no bonus |
| S1 | ≥ $10,000 | +0.04 |
| S2 | ≥ $50,000 | +0.08 |
| S3 | ≥ $100,000 | +0.12 |
| S4 | ≥ $500,000 | +0.16 |
| S5 | ≥ $1,000,000 | +0.20 |

> Tier-spread model: upline only earns the differential, not the downline's full share. Bonus is paid from the ecosystem incentive pool, separate from the main Claim path.
>
> Team bets only count toward team cumulative volume and trigger rewards after the match has been settled.

### First-Deposit Reward

| First Deposit Amount | Referee Gets | Referrer Gets |
|---|---|---|
| ≥ $50 | 10 ODD | 5 ODD |
| ≥ $200 | 50 ODD | 25 ODD |
| ≥ $500 | 150 ODD | 75 ODD |
| ≥ $1,000 | 350 ODD | 175 ODD |

Rewards lock for 30 days, then claimable.

---
