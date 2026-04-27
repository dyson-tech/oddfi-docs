# Odds Mechanism

### How Odds Are Generated

The platform pulls reference odds from third-party professional data sources, strips out the source's original margin to recover true probabilities, then applies OddFi's 10% Margin to generate opening odds.

```
Payout Odds = 1 / (true probability × Overround factor)
```

Typical Overround: 110%.

### Reading the Odds

| Odds | Implied Probability | Meaning |
|---|---|---|
| 1.5 | 66.70% | Strong favorite — low return |
| 2.0 | 50.00% | 50/50 — 2× your stake |
| 3.0 | 33.30% | Underdog — 3× your stake |
| 5.0 | 20.00% | Heavy underdog — 5× your stake |

### Dynamic Adjustment

After each bet, the system detects volume imbalance across sides and adjusts dynamically:

- **Heavy side**: odds compressed (reduces platform risk)
- **Light side**: odds boosted (attracts opposing bets, balances exposure)

Odds lock 1 hour before kickoff and don't move after that. Movements > 0.05 are pushed to the frontend in real time.

### Odds-Movement Confirmation

If odds move > 0.05 between filling in the amount and confirming, the system pops a modal showing the latest odds — you must re-confirm. The locked odds are those at confirmation time.
