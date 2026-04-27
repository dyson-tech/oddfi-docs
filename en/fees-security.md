🌐 **English** · [中文](https://oddfi.gitbook.io/oddfi-docs-zh/fees-security) · [日本語](https://oddfi.gitbook.io/oddfi-docs-ja/fees-security)

---

# Fees & Security

### Platform-Wide Fee Schedule

| Operation | Fee | Paid By |
|---|---|---|
| Deposit (direct transfer) | Gas fee | User |
| Place bet | **Bet tax 1% (extra ODD on top of principal — 100% to direct referrer / platform if none)** | Auto-deducted |
| Early settlement | None | — |
| Payout (winning) | **Payout tax 5%** (2pp staking / 1pp L3 buffer / 1pp platform / 1pp direct referrer) | Deducted from payout |
| Buy / Sell ODD | **Zero tax** (Clean Token at contract layer — no buy/sell tax, no profit tax, no cooldown, no per-tx cap) | — |
| Gas fee (any on-chain op) | On-chain gas | User |
| Referrer Claim (ODD → USDT) | PancakeSwap 0.25% LP fee + gas | Referrer |
| Deposit / withdraw via swap | Standard DEX fee + gas | User |

### Security Measures

| Measure | Description |
|---|---|
| Self-custody | All user funds held by user wallets — platform cannot unilaterally withdraw |
| Multisig settlement | Match settlement requires Gnosis Safe multisig approval |
| ReentrancyGuard | All StakingPool / BettingPool fund operations are reentrancy-protected |
| Pausable | All three core contracts support emergency pause |
| Claim slippage protection | ODD → USDT live swap defaults to 2% slippage cap, customizable (max 5%) |
| Minimum claim threshold | 10 ODD — prevents gas costs eating small claims |
| L3 + L4 buffer waterfall | Extreme payouts cascade through LP funds → platform vault → L3 buffer → L4 buffer pool — four layers preventing single-point pool blowout |
| Third-party audit | Mandatory security audit before mainnet (CertiK / SlowMist / PeckShield) |
| LP lock | DEX liquidity LP token permanently locked |
| Price-manipulation defense | TWAP / oracle cross-validation guards against flash-loan attacks |
| Balance verification | Frontend + contract dual balance check on all operations |

> ODD is a Clean Token with no contract-layer transfer restrictions. Price stability is supported by three business-layer mechanisms: staggered release schedule, active strategic-reserve defense, and application-layer tax recirculation.

### Risk Disclosure

- **Smart contract risk**: Despite audits, contracts may contain undiscovered vulnerabilities. Don't invest more than you can afford to lose.
- **Market risk**: ODD price is subject to market forces. LP and staking yields denominated in ODD carry price-volatility risk.
- **Liquidity risk**: LP funds within the lock-up period cannot be redeemed early without forfeiture.
- **Match risk**: In edge cases (match cancellation, disputed result), a manual settlement flow may trigger and delay payout.

---
