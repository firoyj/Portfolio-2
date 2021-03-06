## Perpetual Contract Basics

Perpetual contracts are a type of futures contract, pioneered in the cryptocurrency space by Bitmex. Perpetual contracts are one of the most popular derivative products in the space.

Perpetual contracts allow traders to speculate on the future price of a given asset by buying (going long) or selling (going short) perpetual futures contracts. Unlike typical futures, perpetuals do not expire and remain effective until the trader closes their position.

The price of perpetual contracts will often diverge from the broader market (aka spot market). These deviations signal sentiment on the exchange - if a majority of traders expect the underlying asset to increase in value over time, the price of the perpetual contract will likely exceed the spot price. Likewise, if most traders expect the price to fall, the price of the perpetual will be below the spot price.

There are two mechanisms that moderate this process, and function to keep the perpetual contract price close to the spot price.

### Funding payments
Every hour, traders with open long or short positions will pay each other a funding payment, depending on market conditions. If the contract price is above the spot price, longs will pay shorts. If the contract price is below the spot price, shorts will pay longs. The size of the funding payment is a function of the difference between the contract price and the spot price, as well as the user's position size. This incentivizes traders to take the unpopular side of the market.

### Arbitrage
If the contract price diverges significantly from the spot price in other exchanges, arbitrageurs can benefit in _two ways_:
1. If they hold a position elsewhere, they can use _XXXXX_ Protocol to take the inverse position and earn funding payments. 
2. They buy or sell an asset elsewhere, and long or short that asset using _XXXXX_ Protocol, in the expectation that the price will tend to move back toward the spot price

_XXXXX_ will connect to API3 data beacons, which are atomic data feeds powered by a singular first-party oracle. Beacons will be used as inputs into the calculations of the logarithmic options pricing model. In partnering with API3, _XXXXX_ can scale its data categories and pairs while having the data feeds covered in the event of any mishaps or manipulation, as is currently prevalent in the data oracle space. API3 has a well-reserved coverage pool for valid claims.

In using first-party data oracles, API3 provides reliable and reputable data feeds with coverage. Having coverage attached to the use of the data feed increases the robustness and confidence in their use for decentralized applications and smart contracts.
API3 is a critical Web3 building block for the quality and quantity of datasets. In order to attract users, the addition of diverse data sets is needed, which grows the total value locked and fee revenue from the opening and closing of trading positions on the _XXXXX_ protocol.
By using API3???s solution we can open up support for ever more reputable direct data sources, which means that we will immediately be able to take advantage of this.

## vAMM
Our exchange model is very different from other exchanges, including AMM-based exchanges.
Key points:
-	_XXXXX_ Protocol does not use liquidity or liquidity providers.
-	_XXXXX_ Protocol is 100% AMM based; there is no order book.
-	The on-chain price reflects trades on XXXXX Protocol - the price only moves when positions are opened or closed.
_XXXXX_ tracks the log2 of the underlying asset's price as our mark, i.e., mark price = log2 (index price)

The log vAMM acts as an independent cash-settlement market. Hence to make the log vAMM mark price close to an underlying index, _XXXXX_ needs to add a funding rate, similar to funding payments for perpetual contracts on central limit order book exchanges.

Traders use collateral (USDC) to open long or short positions in a given asset. Every time a trade is made, the vAMM calculates the entry or exit price in the same way prices are calculated on Uniswap or other AMM style exchanges. 

An important difference with the vAMM is that no swap is occurring. Unlike Uniswap, for example, where traders arrive with asset A and leave with asset B, on _XXXXX_ Protocol traders always arrive with USDC, and leave with USDC. This allows the protocol to operate without ever having held the underlying asset.
