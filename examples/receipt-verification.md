# Receipt Verification

Merchants verify receipts locally before serving a protected resource.

## Required Checks

| Check | Reject When |
|---|---|
| Signature | Signature cannot be verified with current JWKS key |
| Issuer | Issuer is not trusted |
| Audience | Merchant id does not match |
| Resource | Receipt resource does not match requested resource |
| Amount | Amount is below required resource price |
| Pricing tier | Tier is not the merchant-selected tier |
| Expiry | Receipt is expired |
| Nonce | Nonce was already used |

## Pseudocode

```ts
const claims = await verifyReceipt(receipt, { jwks });

assert(claims.aud === merchantId);
assert(claims.resource === request.path);
assert(claims.amount >= requiredAmount);
assert(claims.pricing_tier === requiredTier);
assert(claims.exp > now());
assert(await nonceStore.consume(claims.nonce));
```

