🌐 **English** · [中文](../zh/deposit.md)

---

# Deposit & Withdrawal

### Portfolio (Asset Overview)

Once funded, your assets sit in your Portfolio across four buckets:

| Bucket | Description |
|---|---|
| Cash | Available balance — for betting or withdrawal |
| Bet | Locked in active bets (unsettled) |
| Stake | Locked in staking |
| Liquidity | Funds in the market-making pool |

All amounts shown in ODD + USD equivalent.

---

### Deposit

OddFi assigns each user a unique **personal proxy wallet**. Send funds to this address — the platform identifies you by it, regardless of which wallet the funds came from.

Three deposit methods:

| Method | Description |
|---|---|
| Direct transfer | Send ODD (BSC BEP-20) directly to your proxy wallet address |
| Same-chain swap | Swap BNB or other BSC tokens to ODD on PancakeSwap, then send to proxy wallet |
| Cross-chain swap | Use Relay bridge to swap assets from other EVM chains into ODD |

**Direct transfer steps:**

1. Go to "Wallet" → "Deposit"
2. Copy your personal proxy wallet address
3. Send ODD (BSC BEP-20) from your EOA wallet to that address
4. Wait for 12 block confirmations (~36 seconds)
5. Balance auto-credits

> Only ODD on BSC is supported. Do not transfer from Ethereum mainnet or other chains — funds will not be recoverable.

---

### Withdrawal

Go to "Asset Management" → "Withdraw":

- **≤ $5,000**: auto-processed, instant on-chain settlement, no manual step
- **> $5,000**: enters manual review, completed within 24 hours

You can withdraw to any valid EVM wallet address — not limited to the one you connected with. Once you receive ODD, you can swap to USDT or other tokens via the ODD/USDT pair on PancakeSwap.

---
