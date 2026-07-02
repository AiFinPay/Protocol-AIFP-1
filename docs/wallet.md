# Wallet Guide

Wallets fund agents, enforce spending controls, and settle value with merchants.

## Supported Settlement Modes

| Mode | Description |
|---|---|
| Stablecoin | USDC, USDT settlement on supported networks; PYUSD (planned) |
| Native asset | SOL (Solana) and POL/MATIC (Polygon) settlement |
| Fiat hybrid | Fiat on/off-ramp with stablecoin settlement via BVNK |
| Non-custodial | Agent or user-controlled wallet; the agent holds its own keys and signs locally |
| MPC | Managed signing with distributed key custody (planned) |

## Settlement Flow

```mermaid
flowchart LR
    Quote["Quote"] --> Budget["Budget policy"]
    Budget --> Wallet["Wallet authorization"]
    Wallet --> Settlement["Stablecoin / fiat settlement"]
    Settlement --> Receipt["Receipt issued"]
    Receipt --> Webhook["Merchant webhook"]
```

## Canonical References

- [Security & Cryptography Specification](aifp/04-Security-and-Cryptography-Specification.md)
- [AIFP-1 RFC](aifp/01-AIFP-1-RFC-Payment-Protocol-Specification.md)
- [OpenAPI 3.1](aifp/08-OpenAPI-3.1-Specification.yaml)
