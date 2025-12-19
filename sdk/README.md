# FYRST SDK

TypeScript SDK for interacting with the FYRST on-chain program.

## Build

```bash
npm install
npm run build
```

## Usage

```typescript
import { FyrstClient } from "@fyrst/sdk";

const client = new FyrstClient(wallet, connection);
await client.createEscrow(tokenMint, 1.0);
```

## API

| Method | Description |
|--------|-------------|
| `createEscrow(mint, sol)` | Lock deployer collateral |
| `releaseEscrow(mint)` | Reclaim after safe period |
| `buyTokens(mint, sol)` | Buy on bonding curve |
| `sellTokens(mint, amount)` | Sell on bonding curve |
| `claimRefund(mint)` | Claim pro-rata refund |
