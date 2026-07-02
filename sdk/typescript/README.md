# TypeScript SDK

Target packages:

| Package | Purpose |
|---|---|
| `@aifinpay/merchant` | Express, Fastify, Next.js, and generic Node middleware |
| `@aifinpay/agent` | Agent fetch wrapper, quote/pay/retry client, budget policy hooks |
| `@aifinpay/core` | Types, errors, receipt verification, pricing helpers |

## Merchant Sketch

```ts
import { aifpPaywall } from "@aifinpay/merchant";

app.use(aifpPaywall({
  merchantId: "mrch_...",
  pricing: {
    "/api/data": { tier: "standard" },
    "/api/search": { tier: "complex" },
    "/api/inference": { tier: "premium" }
  }
}));
```

## Agent Sketch

```ts
import { AIFPAgent } from "@aifinpay/agent";

const agent = new AIFPAgent({
  apiKey: process.env.AIFP_AGENT_KEY,
  walletId: "wlt_...",
  budget: { dailyUsd: 5 }
});

const response = await agent.fetch("https://merchant.example.com/api/data");
```

