# Merchant Basic Example

This example shows a merchant protecting `/api/data` with AIFP.

```ts
import express from "express";
import { aifpPaywall } from "@aifinpay/merchant";

const app = express();

app.use(aifpPaywall({
  merchantId: "mrch_9f3a1c2b",
  freeQuota: 100,
  pricing: {
    "/api/data": { complexity: "standard" }
  }
}));

app.get("/api/data", (req, res) => {
  res.json({ data: "premium machine-readable resource" });
});

app.listen(3000);
```

Expected behavior:

1. Requests within free quota return `200`.
2. Requests after quota return `402 Payment Required`.
3. Requests retried with a valid receipt return `200`.
4. Invalid, expired, or replayed receipts are rejected.
