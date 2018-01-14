# Scope

Gekko is a free and open source starter kit for automated trading on cryptocurrency markets. Gekko has a low barrier to entry as only minimal knowledge of javascript is required to write trading strategies.

## Market data

Gekko aggregates market data into [OHLC candles](https://en.wikipedia.org/wiki/Open-high-low-close_chart). Gekko only stores candle data on disk taking up a predictable amount of hard drive space. The tradebot will use some additional market data (Such as the orderbook) in order to efficiently execute orders, but this data cached in memory and not accessible.

## Strategies

Strategies are scripts that receive market data in the form of (OHLC candles) and execute buy / sell orders which could involve the calculation and usage of trading indicators. See [Creating a Strategy](../strategies/creating_a_strategy.html) for more information.

The limits of this design are::

- The smallest time frame a strategy can act on is one minute.
- Strategies do not see trades
- Strategies cannot look at the order book.
- Strategies do not know what the current portfolio looks like.
- Strategies can only trigger LONG or SHORT advice.

## Strategy Execution

When you are using Gekko to execute real trades (TradeBot mode) Gekko will create orders at the exchange whenever your strategy signals execution advice (long or short). A `SHORT` signal advices Gekko to attempt buying as much "asset" as it can with the currently alotted currency budget. For example if your strategy is running on the USD/BTC market then `SHORT` advice would mean attemping to buy all the BTC possible given the current price point and USD budget. As for creating the orders Gekko is conservative and stays on your side of the orderbook.  That means means you do not lose on the spread, slippage, or taker fees. For example:

The strategy signals a LONG signal given the following order book:

<img width="279" alt="screen shot 2017-08-26 at 23 26 22" src="https://user-images.githubusercontent.com/969743/29745564-0bb096a6-8ab6-11e7-8bdb-12a6c0274482.png">

In this case Gekko will try to buy bitcoin by placing a limit order at a price of `4336.29` in the hope someone sells into the order. Every few seconds Gekko will readjust the order to stay on top of the orderbook. *Note that order simulation (in the paper trader and backtester) is handled differently, since the orderbook is not used in the simulation.*
