# Go SDK

Target module: `github.com/aifinpay/aifp-go`.

## Package Layout

| Package | Purpose |
|---|---|
| `aifp` | Core protocol types and errors |
| `merchant` | HTTP middleware and receipt verification |
| `agent` | Quote/pay/retry client |
| `wallet` | Wallet policy and settlement helpers |

## Merchant Sketch

```go
handler := merchant.Paywall(next, merchant.Config{
    MerchantID: "mrch_...",
    Pricing: map[string]merchant.Price{
        "/api/data": {Tier: "standard"},
    },
})
```

