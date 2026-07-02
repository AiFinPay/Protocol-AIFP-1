# Agent Guide

This page is the human-facing overview for building an agent integration. The runnable
onboarding paths are in [Quick Start](quickstart/index.md) and [Core Concepts](core-concepts/index.md).

## What This Role Covers

| Responsibility | Description |
|---|---|
| Detect `402` | Recognize a payment challenge on the resource request |
| Request quote | Ask AiFinPay for a binding price for the resource |
| Enforce budget | Block spend before the wallet is charged |
| Pay safely | Use a wallet plus idempotency so retries do not double-charge |
| Retry request | Attach the receipt token and replay the original request |
| Track reputation | Use Agent Passport where the deployment supports it |

## Read Next

- [Node / TypeScript Quick Start](quickstart/node-typescript.md)
- [Python Quick Start](quickstart/python.md)
- [MCP Server Quick Start](quickstart/mcp-server.md)
- [x402 Flow](core-concepts/x402-flow.md)
- [Error Codes](reference/error-codes.md)
