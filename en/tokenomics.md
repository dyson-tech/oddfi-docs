# ODD Tokenomics

### Basic Info

| Item | Details |
|---|---|
| Token Name | OddFi Token |
| Symbol | ODD |
| Chain | BSC (BNB Smart Chain) |
| Standard | BEP-20 (ERC-20 compatible) — **Clean Token** |
| Total Supply | 100,000,000 (100M), minted once, no further issuance |
| Inflation / Burn | Zero inflation, zero burn (fixed supply) |
| Transfer Tax | Zero (no contract-layer buy/sell tax / referrer tax / cooldown / sell cap) |
| Tax Layer | Application-layer two-tier tax (bet tax 1% + payout tax 5%, both charged in BettingPool) |
| DEX Pair | ODD/USDT (PancakeSwap) |

### Token Allocation

| Allocation | Share | Amount | Notes |
|---|---|---|---|
| Private Sale (3 rounds) | 15% | 15M | Seed / Strategic / Private — staggered linear release |
| Public Sale (3 rounds) | 12% | 12M | Pre-IDO / IDO R1 / Launchpad — partial TGE circulation |
| Team | 20% | 20M | Multisig-locked, 24-month linear release starting after the World Cup |
| Betting Pool Initial Liquidity | 15% | 15M | Locked in contract as Pool principal; payout tax 1pp (L3 buffer) provides ongoing top-up |
| DEX Initial Liquidity | 10% | 10M | Paired with $1M USDT into PancakeSwap, LP token permanently locked |
| Ecosystem Incentives + Marketing | 10% | 10M | Multisig-controlled — KOLs / private testing / referral team bonuses |
| Strategic Reserve | 18% | 18M | Multisig-locked; 2M earmarked for World Cup price stability |
| **Total** | **100%** | **100M** | — |

### TGE & Sale

| Item | Details |
|---|---|
| TGE Price | $0.10 / token |
| TGE Date | 2026-06-01 |
| DEX Opening Liquidity | $2M (10M ODD + $1M USDT) |
| TGE Day Circulation | ~9.3M (Launchpad 5M + IDO R1 2.8M + Pre-IDO 1.5M) |

#### Private Sale (3 rounds, ~$900K total)

| Round | Price | Share | Raised | Release Schedule |
|---|---|---|---|---|
| Seed | $0.03 | 3% | $90K | 38-day linear from 6/11, ends 7/19 |
| Strategic | $0.05 | 5% | $250K | 33-day linear from 6/16, ends 7/19 |
| Private | $0.08 | 7% | $560K | 28-day linear from 6/21, ends 7/19 |

#### Public Sale (3 rounds, ~$1.115M total)

| Round | Price | Share | Raised | Release Schedule |
|---|---|---|---|---|
| Pre-IDO Whitelist | $0.085 | 3% | $255K | 50% TGE release, balance 30-day linear |
| IDO Round 1 | $0.09 | 4% | $360K | 70% TGE release, balance 15-day linear |
| Launchpad | $0.10 | 5% | $500K | 100% TGE circulation |

> All three private rounds start staggered from the 6/11 World Cup kickoff and end on 7/19 final day, protecting the TGE price discovery window.

### Token Utility

| Use Case | Description |
|---|---|
| Predict | All bets priced and settled in ODD |
| Stake | Share platform payout-tax dividend, unlock VIP daily bet limits |
| Market Make | Inject liquidity into Betting Pool, share Margin |
| Govern | Hold ODD to vote on platform proposals |
| Reward | First-deposit bonus, referral reward, airdrops |

### Tax Mechanism (Application-Layer Two-Tier)

> All taxes are charged inside the **BettingPool contract**. The ODD token contract itself has zero tax logic. Holding / transferring / market-making / cross-chain — all friction-free.

#### Bet Tax: 1%

For every bet, the user pays an extra 1% ODD on top of the principal:

| Destination | Share | Description |
|---|---|---|
| Direct referrer (Claim balance) | 100% | Accumulates in referrer's Claim account, withdrawn manually |
| No direct referrer | — | 100% to platform vault |

**Example:** bet 1,000 ODD → wallet debits 1,010 ODD (1,000 principal + 10 tax).

#### Payout Tax: 5% (charged on winning payouts only)

| Destination | Share (pp) | Description |
|---|---|---|
| Staking Pool dividend | 2pp | Distributed to all active stakers (rewardPerShare model) |
| L3 tax buffer | 1pp | Enters BettingPool internal reserve, backstops extreme payouts |
| Platform vault | 1pp | Multisig address |
| Direct referrer (Claim) | 1pp | Accumulates in referrer's Claim account |
| **Total** | **5pp** | — |

**Example:** payout of 10,000 ODD → user receives 9,500 ODD (200 to staking / 100 L3 / 100 platform / 100 referrer).

### VIP Tiers

Stake ODD to unlock higher daily bet limits (conversion rate locked at $0.1 / ODD):

| Tier | Effective Stake (ODD) | Daily Bet Limit (ODD) | USD Equivalent |
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

> Real-time evaluation, no protection period — stake changes apply immediately.

### Growth Flywheel

```
More users bet
  ↓
BettingPool collects bet tax 1% + payout tax 5%
  ↓
  ├─ Bet tax 1% ───→ Referrer Claim (ODD → USDT) → drives referral activity
  └─ Payout tax 5%:
      ├─ 2pp → Staking dividend ──→ APY rises ──→ more users lock ODD
      ├─ 1pp → L3 buffer ────→ BettingPool solvency strengthens
      ├─ 1pp → Platform vault ──→ Operations / buyback / ecosystem
      └─ 1pp → Referrer Claim ──→ drives referral activity
  ↓
Stake lock-up + VIP bet demand → natural ODD buying → price rises
  ↓
Volume scales → tax absolute volume scales → staking APY rises further (loop)
```

### Supply Constancy

- **Zero inflation:** 100M fixed supply, no mint interface, no further issuance after TGE
- **Zero burn:** No burn mechanism (v2.4's profit-tax burn is retired)
- **Float management:** Effective circulation managed via staking lock-up + private sale linear release, not via burn

---
