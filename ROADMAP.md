# AiFinPay Paywall Roadmap

AiFinPay Paywall Protocol is moving from draft documentation toward a public protocol release, conformance program, and production SDK ecosystem.

## Release Tracks

| Track | Goal | Status |
|---|---|---|
| Protocol | Stabilize AIFP-1 and AIP process | Draft Standard |
| API | Publish OpenAPI 3.1 and schema validation | In progress |
| SDKs | Merchant and agent SDKs across major languages | Planned |
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
- [ ] Full canonical document sync from source package
- [ ] Binary PDF artifact sync

### v0.2 Documentation Release

- [ ] Publish canonical Docs 01-15 in `docs/aifp/`
- [ ] Validate cross-links
- [ ] Validate OpenAPI 3.1
- [ ] Validate JSON Schemas
- [ ] Add generated docs navigation
- [ ] Add branded diagrams and assets

### v0.3 Developer Preview

- [ ] Merchant SDK reference implementation
- [ ] Agent SDK reference implementation
- [ ] Wallet and webhook examples
- [ ] Sandbox challenge/pay/receipt flow
- [ ] Receipt verifier test vectors

### v0.4 Conformance Preview

- [ ] Protocol conformance runner
- [ ] Error registry tests
- [ ] Replay and idempotency tests
- [ ] JWKS and key rotation tests
- [ ] CI conformance workflow

### v1.0 Draft Standard Release

- [ ] AIFP-1 tagged release
- [ ] Public developer portal
- [ ] Security review
- [ ] AIP governance opened
- [ ] SDK packages published
- [ ] Certification program announced

## Non-Goals

- AIFP does not introduce a native token.
- AIFP does not require merchants to depend on AiFinPay for per-request access checks.
- AIFP does not replace HTTP authentication; it adds a payment layer for machine access.
