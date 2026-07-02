# AiFinPay Paywall Roadmap

AiFinPay Paywall is moving from documentation package to public protocol release, SDK ecosystem, conformance program, and production developer portal.

## Release Tracks

| Track | Goal | Status |
|---|---|---|
| Protocol | Stabilize AIFP-1 and AIP process | Draft Standard |
| API | OpenAPI 3.1, Postman, JSON Schemas | Synced |
| Documentation | Canonical Docs 01-15 and refreshed PDFs | Synced |
| SDKs | Merchant and agent SDKs across major languages | Design ready |
| Conformance | Test vectors and certification suite | Planned |
| Portal | Developer portal generated from docs-as-code | Planned |
| Governance | Open AIP workflow and security council | Draft |

## Milestones

### v0.1 Repository Foundation

- [x] Premium repository README
- [x] Documentation portal structure
- [x] GitHub issue and PR templates
- [x] Security, support, contributing, code of conduct
- [x] CI workflow skeletons
- [x] SDK, examples, sandbox, schemas, assets, scripts, tests entry points
- [x] Full canonical document sync from source package
- [x] Refreshed PDF artifact sync
- [x] Pricing model migrated to Standard, Complex, Premium tiers

### v0.2 Documentation Release

- [x] Publish canonical Docs 01-15 in `docs/aifp/`
- [x] Publish OpenAPI 3.1 and Postman collection
- [x] Publish JSON Schemas document
- [x] Add role-based documentation navigation
- [x] Add protocol economics, security model, and conformance overview pages
- [ ] Run automated external link validation after public domain URLs are final
- [ ] Add exported architecture diagrams to `assets/diagrams/`

### v0.3 Developer Preview

- [ ] Merchant SDK reference implementation
- [ ] Agent SDK reference implementation
- [ ] Receipt verifier test vectors
- [ ] Wallet budget and policy fixtures
- [ ] Sandbox challenge, quote, pay, receipt, and webhook flow
- [ ] Generated SDK packages from OpenAPI and JSON Schemas

### v0.4 Conformance Preview

- [ ] Protocol conformance runner
- [ ] Error registry tests
- [ ] Replay and idempotency tests
- [ ] JWKS and key rotation tests
- [ ] CI conformance workflow
- [ ] Certification checklist for merchants, agents, wallets, and SDKs

### v1.0 Draft Standard Release

- [ ] AIFP-1 tagged release
- [ ] Public developer portal
- [ ] Independent security review
- [ ] AIP governance opened
- [ ] SDK packages published
- [ ] Conformance certification program announced

## Non-Goals

- AIFP does not introduce a native token.
- AIFP does not require merchants to depend on AiFinPay for per-request access checks.
- AIFP does not replace HTTP authentication; it adds a payment layer for machine access.
