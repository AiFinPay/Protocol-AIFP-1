# SDKs

AiFinPay SDKs provide merchant middleware, agent auto-pay clients, receipt verification, wallet binding, and protocol helpers.

## Language Matrix

| Language | Merchant SDK | Agent SDK | Package Target |
|---|---:|---:|---|
| TypeScript / Node | Yes | Yes | `@aifinpay/merchant`, `@aifinpay/agent` |
| Python | Yes | Yes | `aifinpay-merchant`, `aifinpay-agent` |
| Go | Yes | Yes | `github.com/aifinpay/aifp-go` |
| Rust | Planned | Planned | `aifinpay` |
| Java | Planned | Planned | `io.aifinpay:aifp` |
| PHP | Planned | Planned | `aifinpay/aifp` |
| .NET | Planned | Planned | `AiFinPay` |

## SDK Architecture

```mermaid
flowchart TD
    Core["Protocol Core"] --> Types["Generated Types"]
    Core --> Receipt["Receipt Verifier"]
    Core --> Errors["Error Registry"]
    Types --> Merchant["Merchant Middleware"]
    Types --> Agent["Agent Client"]
    Types --> Wallet["Wallet Client"]
    Merchant --> Frameworks["Express / Fastify / Next / Django / Rails"]
    Agent --> Fetch["fetch / requests / http clients"]
    Wallet --> Settlement["Stablecoin / fiat adapters"]
```

## Source Documents

- [AI Agent SDK Specification](../docs/aifp/03-AI-Agent-SDK-Specification.md)
- [SDK Reference](../docs/aifp/11-SDK-Reference.md)
- [OpenAPI 3.1](../docs/aifp/08-OpenAPI-3.1-Specification.yaml)
- [JSON Schemas](../docs/aifp/10-JSON-Schemas.md)
