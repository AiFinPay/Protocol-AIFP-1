# Python SDK

Target packages:

| Package | Purpose |
|---|---|
| `aifinpay-merchant` | FastAPI, Flask, Django middleware and receipt verification |
| `aifinpay-agent` | Agent client, quote/pay/retry helpers, budget policy hooks |
| `aifinpay-core` | Types, errors, receipt verification, pricing helpers |

## Agent Sketch

```py
from aifinpay_agent import AIFPAgent

agent = AIFPAgent(
    api_key=os.environ["AIFP_AGENT_KEY"],
    wallet_id="wlt_...",
    daily_budget_usd=5,
)

response = agent.get("https://merchant.example.com/api/data")
```

