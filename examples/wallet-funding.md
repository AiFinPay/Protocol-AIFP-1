# Wallet Funding Example

AIFP wallets fund agent payments and enforce spending limits.

```json
{
  "wallet_id": "wlt_3a1b",
  "agent_id": "agt_4f9a2c7e",
  "assets": ["USDC", "USDT", "POL"],
  "preferred_chain": "polygon",
  "budget": {
    "daily_usd": "5.00",
    "max_per_request_usd": "0.10"
  }
}
```

Wallet integrations should expose:

- Funding source.
- Supported assets and chains.
- Spending limits.
- Risk policy.
- Audit log.
- Settlement references.
