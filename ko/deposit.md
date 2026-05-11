🌐 [English](https://oddfi.gitbook.io/oddfi-docs-en/deposit) · [中文](https://oddfi.gitbook.io/oddfi-docs-zh/deposit) · [日本語](https://oddfi.gitbook.io/oddfi-docs-ja/deposit) · **한국어**

---

# 입금 및 출금

### Portfolio (자산 개요)

입금 후 자산은 Portfolio에서 네 개의 구획에 표시됩니다:

| 구획 | 설명 |
|---|---|
| Cash | 사용 가능 잔고 — 베팅 또는 출금에 사용 |
| Bet | 활성 베팅에 락업됨 (미정산) |
| Stake | 스테이킹에 락업됨 |
| Liquidity | 마켓 메이킹 풀에 예치됨 |

모든 금액은 ODD + USD 환산값으로 표시됩니다.

---

### 입금

OddFi는 사용자마다 고유한 **스마트 어카운트 지갑**을 부여합니다. 이 주소로 자금을 보내면 어떤 지갑에서 보냈든 플랫폼이 이를 통해 사용자를 식별합니다.

세 가지 입금 방식:

| 방법 | 설명 |
|---|---|
| 직접 전송 | ODD (BSC BEP-20)를 스마트 어카운트 지갑 주소로 직접 전송 |
| 동일 체인 스왑 | PancakeSwap에서 BNB나 기타 BSC 토큰을 ODD로 스왑한 뒤 스마트 어카운트 지갑으로 전송 |
| 크로스체인 스왑 | Relay 브릿지로 다른 EVM 체인 자산을 ODD로 스왑 |

**직접 전송 절차:**

1. "Wallet" → "Deposit" 이동
2. 스마트 어카운트 지갑 주소 복사
3. EOA 지갑에서 해당 주소로 ODD (BSC BEP-20) 전송
4. 블록 12회 확인 대기 (약 36초)
5. 잔고 자동 반영

> BSC의 ODD만 지원됩니다. Ethereum 메인넷 등 다른 체인에서 전송하지 마세요 — 자금을 복구할 수 없습니다.

---

### 출금

"Asset Management" → "Withdraw" 이동:

- 온체인 트랜잭션이 확정되면 즉시 출금 — 수동 심사 없음

연결한 지갑에 한정되지 않고, 유효한 EVM 지갑 주소라면 어디로든 출금할 수 있습니다. ODD를 수령한 뒤에는 PancakeSwap의 ODD/USDT 페어를 통해 USDT나 기타 토큰으로 스왑할 수 있습니다.

---
