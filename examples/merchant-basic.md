# Merchant Basic Example

This example shows a merchant protecting `/api/data` with AIFP.

> Note: `@aifinpay/merchant` is planned — for now verify receipts with a standard JWT library (e.g. `jose`). Live SDKs today: Python (`aifinpay-agent`), Node (`@aifinpay/agent`), MCP (`@aifinpay/mcp`).

```ts
import express from "express";
import { aifpPaywall } from "@aifinpay/merchant";

const app = express();

app.use(aifpPaywall({
  merchantId: "mrch_9f3a1c2b",
  pricing: {
    "/api/data": { tier: "standard" }
  }
}));

app.get("/api/data", (req, res) => {
  res.json({ data: "premium machine-readable resource" });
});

app.listen(3000);
```

Expected behavior:

1. Paid actions return `402 Payment Required` when no valid receipt is present.
2. The agent quotes the Standard tier, starting from `$0.00001`.
3. The agent pays, AiFinPay applies a 1% protocol fee, and 99% settles to the merchant excluding network or settlement costs.
4. Requests retried with a valid receipt return `200`.
5. Invalid, expired, or replayed receipts are rejected.
