# About Gekko

Gekko is a **free and open source** trading and backtesting platform that connects to popular crypto currency exchanges. It is written in javascript and runs on [nodejs](http://nodejs.org).

Gekko makes it very easy to automate your own trading stragies using a wide assortment of technical analysis (TA) indicators and metrics.

*Use Gekko at your own risk.*

![screen shot of gekko backtesting](https://cloud.githubusercontent.com/assets/969743/24838718/8c790a86-1d45-11e7-99ae-e7e551cb40cb.png)

## The gist

![gist of gekko](https://gekko.wizb.it/_static/gekko-gist.png)

Either create a new custom strategy or start with the built-in example. Run the strategy in one of the following modes:

- **Backtest**: Simulate the strategy over a historical data period in order to determine how profitable it is.
- **Paper trader**: Run a realtime simulation of the strategy with fake money.
- **Tradebot**: You can run the strategy in realtime and automatically execute orders based on signals.

All the above modes can be run from the user interface.  It shows both charts and performance/risk statistics.

## Strategies

Gekko comes with some [example strategies](../strategies/example_strategies.md) (which implement a single indicator). With some basic javascript knowledge you can [create your own strategies](../strategies/creating_a_strategy.md). You can use over 130 indicators to create the perfect prediction model ([full list](../strategies/talib_indicators.md) of supported indicators). *Why don't you combine Bollinger Bands, CCI and MACD with a STOCHRSI indicator?*

## Automated Trading platform

Gekko can automatically execute strategies on realtime markets. Gekko saves realtime market data creating the possibility of simulating / repeating other strategies again over the same market conditions (backtesting).

## Limitations

Gekko is not built for [HFT](https://en.wikipedia.org/wiki/High-frequency_trading). Please see the [scope page](./scope.md) to read more about what you can and cannot do with Gekko.

## How does Gekko work?

![Gekko architecture](https://wizb.it/gekko/static/architecture.jpg)

For more see the [architecture documentation](../internals/architecture.md).

## Credits

* The title is inspired by [Bateman](https://github.com/fearofcode/bateman).
* This project is inspired by the [GoxTradingBot](https://github.com/virtimus/GoxTradingBot/) Chrome plugin (which in turn is inspired by [Goomboo's journal](https://bitcointalk.org/index.php?topic=60501.0)).

## Final

If Gekko helped you in any way, you can always leave me a tip at (BTC) 13r1jyivitShUiv9FJvjLH7Nh1ZZptumwW

## Disclaimer

Gekko (nor anyone behind this project) DOES NOT give investment advice. All advice seen within Gekko is the result of running YOUR OWN strategies against the market. On top of that there might be bugs in the code - Gekko DOES NOT come with ANY warranty.

## License

The MIT License (MIT)

Copyright (c) 2014 Mike van Rossum <mike@mvr.me>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
