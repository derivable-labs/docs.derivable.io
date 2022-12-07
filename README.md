---
description: Basic concepts in Derivable
---

# Concepts

CEX: Centralized Exchange. E.g. Binance, Coinbase, FTX, Mt. Gox, etc.

DEX: Decentralized Exchange. E.g. Uniswap, Pancake Swap, etc.

Token Price (P) is the market price of one token (base) to another (quote). P is fetched either from off-chain CEXes, or on-chain DEXes. ETH/USD price is the conversion rate of ETH to US Dollars, and it must be fetched from an off-chain CEX. ETH/USDC is the conversion rate of ETH to USDC token, and it can be fetched from an on-chain DEX or off-chain CEX. ETH/USDC and ETH/USD are not the same.

Power Perpetual (PP): Derivatives that track an asset price in the form of $${P\over M}^x$$where $$P$$ is a Token Price and M is a Mark Price.

Mark Price (M) in Derivable is initialized with the first value of P being fetched, and will not follow the market price after that. Mark Price will be changed by internal mechanisms of the Power Perpetual protocol in a deterministic way.

E.g. A Power Perpetual token $${ETH\over USDC}^4$$ has its M initialized with 1500, when the market price of ETH/USDC changes to 1600, the price of the token will be $${1600\over 1500}^4 = 1.294538272$$.

Exposure: how many times the derivative token value will be changed if the underlining price changes a fixed reference rate of price (+1%). In the example above, the exposure of the derivative token is $$e = ({1616\over 1500}^4-{1600\over 1500}^4)  ≈ 5.26$$.

Liquidity Provider Token (LP): the token received when the liquidity is added to an AMM pool.

Collateral Provider Token (CP): the token received when the collateral is added to a Derivable DDL pool.
