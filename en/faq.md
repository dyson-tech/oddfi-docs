🌐 **English** · [中文](../zh/faq.md)

---

# FAQ

### Account & Connection

| Question | Answer |
|---|---|
| Do I need to register? | No. Just connect an EVM wallet and sign a message — no email, password, or KYC. |
| Which wallets are supported? | MetaMask, OKX Wallet, Bitget Wallet, Phantom, Binance Wallet, Coinbase Wallet, and any WalletConnect-compatible wallet. |
| What chain does OddFi run on? | BNB Smart Chain (BSC, chainId = 56). |
| Do I need BNB? | Yes — to pay gas fees. Keep a small amount of BNB in your wallet. |
| What if I switch wallet accounts? | OddFi detects the change and prompts re-authentication with the new address. |
| Is there a mobile app? | OddFi is a web app, optimized for both desktop and mobile. On mobile, a system browser is recommended. |

### Deposit & Withdrawal

| Question | Answer |
|---|---|
| My deposit shows arrived, but balance is 0? | Deposits require 12 block confirmations (~36 seconds). If still missing after 5 minutes, verify the asset is BSC-chain ODD and was sent to the correct proxy wallet address. |
| Can I withdraw to a different wallet? | Yes — to any valid EVM wallet address. |
| Why is my deposit address different from my login wallet address? | OddFi assigns each user a separate proxy wallet as the deposit address — this lets the platform recognize ownership regardless of which wallet sent the funds. |

### Bets & Returns

| Question | Answer |
|---|---|
| What if odds change before I confirm? | If they shift > 0.05, the system pops a confirmation modal — you must re-confirm. The locked odds are those at confirmation time. |
| Is there a minimum bet? | Minimum 10 ODD. |
| Is there a tax on bets? | Yes — a 1% bet tax in ODD on top of your stake. 100% goes to your direct referrer; if you have none, it goes to the platform. |
| Is there a tax on payouts? | Yes — a 5% payout tax: 2pp staking pool / 1pp L3 buffer / 1pp platform / 1pp direct referrer. |
| What happens with a parlay if one match has no result and the others all won? | A parlay needs all legs settled to compute the outcome. If any leg is unsettled, the entire parlay stays Pending. |

### Position Lending

| Question | Answer |
|---|---|
| Collateral position won, borrowed bet lost? | Borrowed bet loses normally (loss capped at 50% of collateral principal). Collateral pays out as usual. |

### Staking & Market Making

| Question | Answer |
|---|---|
| What do I lose with early staking redemption? | Principal 100% returned, all accrued yield forfeited. |
| Where does staking yield come from? | Payout tax 2pp + early-redemption forfeitures. Distributed by user staked × multiplier weight. |

### Referrals & Token

| Question | Answer |
|---|---|
| Can I change my referral relationship? | No. First binding is written on-chain and is permanent. |
| When do referral rewards arrive? | Not in real-time. Once 10+ ODD accumulates in BettingPool, click Claim — the contract live-swaps ODD to USDT and sends to your wallet. |
| Do I need to stake to receive referral rewards? | No. Under the Clean Token model, referrers have no threshold. |
| Is there a tax on buying/selling ODD? | No. ODD is a Clean Token — zero tax at the contract layer. All taxes are charged inside BettingPool on bets and payouts only. |
| Will the 100M supply ever inflate or burn? | Neither. Zero inflation, zero burn — supply is fixed forever. |

### Supported Languages

中文, English, Português, 日本語, हिन्दी, Español, Türkçe, Deutsch, Français

---

Get help: OddFi.io/support · Telegram · Discord
