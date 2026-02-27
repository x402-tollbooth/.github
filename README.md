# ⛩️ tollbooth

**Turn any API into a paid API.** One YAML config. Zero code changes.

tollbooth is an open-source [x402](https://x402.org) payment gateway that sits in front of your API and handles micropayments in USDC — so you can monetize any HTTP endpoint without touching your backend.

## How it works

```
Client → tollbooth → Your API
         ↕
    x402 facilitator
    (payment settlement)
```

1. Client hits your endpoint through tollbooth
2. tollbooth returns `402 Payment Required` with a USDC price
3. Client signs a payment and retries
4. tollbooth verifies, settles on-chain, proxies the request
5. Your API responds as normal — it never knows about payments

## Repos

| Repo | Description |
|---|---|
| [**gateway**](https://github.com/x402-tollbooth/gateway) | Core gateway — routing, pricing, settlement, hooks |
| [**docs**](https://github.com/x402-tollbooth/docs) | Documentation at [docs.tollbooth.sh](https://docs.tollbooth.sh) |
| [**web**](https://github.com/x402-tollbooth/web) | Landing page at [tollbooth.sh](https://tollbooth.sh) |

## Quick start

```bash
npx x402-tollbooth init    # generate a config
npx x402-tollbooth start   # start the gateway
```

## Links

- 📖 [Docs](https://docs.tollbooth.sh)
- 📦 [npm](https://www.npmjs.com/package/x402-tollbooth)
- 🐳 [Docker](https://ghcr.io/x402-tollbooth/gateway)
- 🌐 [x402 ecosystem](https://x402.org/ecosystem)
