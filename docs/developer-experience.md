# Developer Experience

AiFinPay should feel boring in production and elegant in development: clear docs, typed contracts, predictable examples, and low-friction sandboxing.

## Developer Surfaces

| Surface | Purpose |
|---|---|
| Root README | Executive overview and fastest path into the project |
| Docs portal | Role-based navigation and conceptual docs |
| Canonical docs | Normative RFCs, specs, guides, governance, branding |
| OpenAPI | API contract for generated clients and docs |
| JSON Schemas | Validation contract for protocol objects |
| Postman | Manual API exploration and onboarding |
| SDKs | Merchant middleware, agent client, wallet helpers, receipt verifier |
| Examples | Copyable recipes for common flows |
| Sandbox | Local and hosted flow simulation |
| Tests | Conformance and regression strategy |

## Quality Bar

- Every role has a clear start path.
- Every protocol object links to its source of truth.
- Every example uses current `pricing_tier` terminology.
- Every price-bearing object follows Standard, Complex, Premium tiers.
- Every security-sensitive flow links to the security model.

