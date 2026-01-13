# SDK Usage Guide

## Installation

```bash
git clone https://github.com/fyrst-fun/fyrst.git
cd fyrst/sdk
npm install
npm run build
```

## Quick Start

```typescript
import {{ FyrstClient }} from "@fyrst/sdk";

const client = new FyrstClient(wallet, connection);

// Create escrow
const tx = await client.createEscrow(tokenMint, 1.0);

// Buy tokens
const buyTx = await client.buyTokens(tokenMint, 0.5);

// Sell tokens
const sellTx = await client.sellTokens(tokenMint, 1000);
```

## Error Handling

All methods throw `FyrstError` on failure. Common errors:

| Code | Name                   | Description                    |
|------|------------------------|--------------------------------|
| 6000 | InsufficientCollateral | Collateral below minimum       |
| 6001 | SafePeriodNotExpired   | Cannot release during safe     |
| 6003 | SlippageExceeded       | Price moved beyond tolerance   |
| 6008 | MathOverflow           | Arithmetic overflow detected   |
