# AiFinPay Documentation Portal

Welcome to the AiFinPay Paywall Protocol documentation portal.

AIFP is an open payment protocol that enables AI agents to natively pay for websites, APIs, data, compute, and digital services, while enabling providers to monetize AI traffic instead of blocking it. HTTP 402 compatibility is one of its interoperability features.

## Start Here

| Role | Recommended Path |
|---|---|
| New developer | [Quick Start](quickstart.md) |
| Merchant engineer | [Merchant Guide](merchant.md) → [Integration Guide](aifp/02-Merchant-Integration-Guide.md) |
| Agent builder | [Agent Guide](agent.md) → [Agent SDK Spec](aifp/03-AI-Agent-SDK-Specification.md) |
| Wallet/platform engineer | [Wallet Guide](wallet.md) → [Security Spec](aifp/04-Security-and-Cryptography-Specification.md) |
| Protocol implementer | [AIFP-1 RFC](aifp/01-AIFP-1-RFC-Payment-Protocol-Specification.md) |
| API tooling | [OpenAPI 3.1](aifp/08-OpenAPI-3.1-Specification.yaml) and [JSON Schemas](aifp/10-JSON-Schemas.md) |
| Maintainer | [Repository Architecture](aifp/15-Repository-Architecture.md) and [AIP Process](aifp/06-AIP-Improvement-Proposal-Process.md) |

## Documentation Sections

| Section | Description |
|---|---|
| [Architecture](architecture.md) | System model, trust boundaries, data plane, control plane |
| [Quick Start](quickstart.md) | First merchant, agent, wallet, and sandbox flows |
| [Navigation](navigation.md) | Complete documentation map |
| [AIFP Docs](aifp/README.md) | Canonical documentation package |
| [SDKs](../sdk/README.md) | SDK package strategy and language matrix |
| [Examples](../examples/README.md) | Runnable examples and recipes |
| [Sandbox](../sandbox/README.md) | Development and testing environment |
| [Schemas](../schemas/README.md) | Validation and machine-readable contracts |

## Protocol In One Flow

```mermaid
flowchart LR
    A["Agent requests resource"] --> B["Merchant returns 402 challenge"]
    B --> C["Agent requests quote"]
    C --> D["Agent pays"]
    D --> E["AiFinPay signs receipt"]
    E --> F["Agent retries request"]
    F --> G["Merchant verifies receipt locally"]
    G --> H["Access granted"]
```

## Canonical Documents

The canonical documentation package lives in [`docs/aifp/`](aifp/README.md). These documents govern protocol behavior and should be treated as source of truth.
