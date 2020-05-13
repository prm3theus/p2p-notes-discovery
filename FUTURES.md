# Futures + Smart Contracts

Some research into futures for [collective-commerce](https://github.com/prm3theus/p2p-notes-discovery/blob/master/EXPERIMENT.md) & [minimal-viable-futures](https://github.com/prm3theus/minimal-viable-eth-futures)

## examples
- normal futures: https://www.bitmex.com/app/futuresGuide
- dy/dx contracts perpetual futures: https://docs.dydx.exchange/#/perpetual-protocol
- 0x contracts: https://0x.org/docs/guides/v2-specification#filling-orders
- futureswap: https://www.futureswap.com/

## perpetual futures
- require liqudation bots
- always remain open
- uses a dynamic funding rate to incent a fair price
- uses an 'insurance fund' to on bot / market malfunction

## approach
- start with a V1 with no perpetualness
- needs account / margin state of balances
- 'makerApprove' + 'takerBuild' for: 1) approve + signature creation then 2) to be fullfilled via some taker in the future
- can't perform `approve` on native ether. must use [`WETH`](https://weth.io/) or some other ERC20
- could use a twitter bot to pull & post on a feed of futures

