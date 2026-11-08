# PrivatEx

Non-custodial limit order trading terminal on BNB Smart Chain.

Website: https://privatex.trade
Terminal: https://privatex.trade/trade

## What it is

PrivatEx is an order book trading terminal on BNB Smart Chain. Users connect MetaMask or Trust Wallet and place limit orders. Funds stay in the user's own wallet until the moment of execution. The smart contract only executes the trade and never holds user funds.

One order book combines limit orders from all traders with DEX liquidity (PancakeSwap, Uniswap), so every trade gets the best available price and never worse than the order price.

Besides crypto, the terminal supports tokenized US stocks (Binance bStocks: Tesla, NVIDIA, Apple, SpaceX, Intel and more) and Tether gold. Trading is 24/7, spot only, no leverage. No sign-up and no KYC.

## How it works

1. Connect a wallet (MetaMask, Trust Wallet).
2. Approve the token once to the Router contract.
3. Place a limit order. The order is stored on-chain in the OrderBook contract.
4. When the price is reached, the order is executed in a single transaction and the tokens arrive directly in the user's wallet.

## Network

BNB Smart Chain (chain ID 56)

## Smart contracts

| Contract  | Address |
|-----------|---------|
| Router    | [0x42F1FD38D635A7D05C1e96BD9A7f2F281Ac26b61](https://bscscan.com/address/0x42F1FD38D635A7D05C1e96BD9A7f2F281Ac26b61) |
| OrderBook | [0xDA2bbb903CEF15c769E27402f86768E898821bD8](https://bscscan.com/address/0xDA2bbb903CEF15c769E27402f86768E898821bD8) |

Source code is verified on BscScan. The contracts are not upgradeable.

## Fees

- Maker fee: 0.1%
- Taker fee: 0.25%

## Security

- Non-custodial: the contracts never hold user funds between trades.
- The Router can only move tokens for an order the user created, for the exact amount and price of that order.
- In the same transaction the user receives the counter token at the limit price or better, otherwise the transaction reverts.

## Contact

Website: https://privatex.trade
