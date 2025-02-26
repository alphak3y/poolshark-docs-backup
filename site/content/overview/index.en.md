---
title: Overview
---
># Overview?

The **Poolshark Protocol** is a collection of noncustodial smart contracts that acts as a [decentralized exchange](glossary/##DEX) offering both [directional](glossary/directional-automated-market-maker) and [bidirectional liquidity](glossary/bidirectional-automated-market-maker). By having directional support, LPs can properly express their views on a given pair and increase liquidity available to the market at the same time. 

Each type of position is placed within a [liquidity pool](glossary/liquidity-pool) and transacted with via users swapping. Having multiple LP types allows Poolshark to function as a hybrid of an [**automated market maker**](glossary/##automated-market-maker) (AMM) and a [**limit order book**](glossary/##limit-order-book) (LOB) at once.

The key difference between Poolshark and limit order books is that LOBs have a order queue while Poolshark merges all liquidity into a single pool, allowing for greater transaction throughput.

The key difference between Poolshark and AMM is the addition of limit orders, take profits, trailing take profit, stop loss and trailing stop all as a liquidity provider.

<!-- [picture here difference between BDAMM and DAMM] -->
<br/><br/>
># **What Problem does Poolshark Address?**

## **Indeterminate Pricing**

For large institutions to use a spot exchange for everyday operations they must be able to provide a single asset to a position that allows them to set a immutable price and have irreversible execution. Given that current DEXes either deal with options, perpetuals or AMMs which either don't allow for spot trading, create gas issues or have execution that is irreversible the current DEXes on the market are unable to meet the needs of many institutions to move into providing assets on decentralized exchanges

## **Merged buy and sell sides**

Currently most fully on-chain DEXs are AMMs (for now) and focus on allowing users to create positions that trade into both tokens on the pair moving along an invariant curve. This is something that (due to the mechanisms of constant function pools) inherently implies you believe the price of both tokens in the pair will stay relatively stable. 

One of the features of the inherent design of an AMM from the view point of a LP is when the price of an asset is changing relative to the other and the LP's position is transacted with it changes to be comprised of more of the token that is decreasing in value. The reasoning for accepting this is due to transacting with by swaps in either direction continuously the LP's position accrues transaction fees from the users swapping in either direction with the liquidity pool.

The issue with AMM pools is, given the scenario above, the greater of a price change the less the user is receiving relative to what the value of the assets they initially deposited are worth. This is a type of oppertunity cost called **impermanent loss**. The reason it may be impermanent is if the price shifts back to where it was when the LP created their position the loss will be eliminated. 

The price of the asset held in a position is determined by the demand for that asset relative to the other asset in a pair. Due to this if there is a lot of swapping into a certain asset in an AMM pool that asset will decrease in price.

Poolshark addresses this by allowing LP's to choose from multiple types of positions to better reflect their beliefs on the market and manage their risk as they see fit.
<br/><br/>
># **Three Types of Positions**

Poolshark employs three types of positions:

- Limit positions
- Cover positions
- Range positions

Each of these positions are present in a different type of pool.

[Limit Pools](limit-pools) can be viewed as a limit order.

[Cover Pools](cover-pools) can be viewed as a stop loss/take profit which references the current price.

[Range Pools](range-pools) can be viewed as an AMM pool with liquidity bounded to a range.

Use cases for each can be observed on their respective pages.
<br/><br/>
># **Wrapping Up The Overview**

The team is excited to see new use cases found for each of the types of positions and listen to suggestions. 

With these added position types, liquidity providers can customize their risk profile to match the current price action in the market.

Directional LPing</em> allows for one-way fills similar to a traditional limit order, whereas current LP positions will trade both ways.

DeFi protocols are often the largest liquidity providers in the ecosystem, so we're excited to see how our community and ecosystem can build solutions around protocols that are seeking to greater improve their profitability and runway for the coming years.

If you would like to contribute or have any questions, don't hesistate to [open an issue on Github](https://github.com/poolsharks-protocol/docs/issues), or dm on [Twitter](https://twitter.com/PoolsharkLabs)

<br/><br/><br/>
