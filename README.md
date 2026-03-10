# Monte Carlo Trading Simulator & Kelly Criterion Calculator

A free, browser-based tool to stress-test trading strategies using Monte Carlo simulation and calculate optimal position sizes with the Kelly Criterion.

**[Try it live → hasch74.github.io](https://hasch74.github.io/)**

## Features

- **Monte Carlo Simulation** — Run 1,000–10,000+ randomized trading scenarios to see the full range of possible outcomes
- **Kelly Criterion** — Calculate the mathematically optimal bet size (Full, Half, Quarter Kelly)
- **Equity Curves** — Visualize all simulation paths with a highlighted median
- **Risk Analysis** — Probability of profit/loss, drawdown thresholds (25%/50%/75%), Sharpe Ratio
- **Final Capital Distribution** — Histogram showing where your account is likely to end up
- **Drawdown Distribution** — Understand worst-case dips before recovery
- **100% Client-Side** — No data sent anywhere. Everything runs locally in your browser.

## Input Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| Starting Capital | Your initial account balance | $10,000 |
| Win Rate | Percentage of trades that win | 55% |
| Number of Trades | Trades simulated per run | 200 |
| Win Amount | Profit per $1 risked on a win | $1.50 |
| Loss Amount | Loss per $1 risked on a loss | $1.00 |
| Bet Size | % of capital risked per trade | 2% |
| Simulations | Number of Monte Carlo runs | 1,000 |

## Screenshot

![Monte Carlo Simulator Screenshot](https://hasch74.github.io/screenshot.png)

## How It Works

1. **Enter your strategy parameters** — win rate, risk/reward, position size
2. **Click "Run Simulation"** — the tool runs thousands of independent random walks
3. **Analyze the results** — median outcome, worst case, drawdown risk, and whether your bet size is optimal according to Kelly

### Kelly Criterion Formula

```
Kelly% = W - (1 - W) / b
```
Where `W` = win rate, `b` = win/loss ratio. The Kelly fraction maximizes long-term geometric growth rate. Most professional traders use Half Kelly or less for safety.

## Tech Stack

- Single HTML file, zero dependencies to install
- [Chart.js](https://www.chartjs.org/) for interactive charts (loaded via CDN)
- Vanilla JavaScript for Monte Carlo engine

## Use Cases

- Day traders evaluating strategy edge and position sizing
- Sports bettors calculating optimal bankroll management
- Poker players analyzing risk of ruin
- Students learning about probability and risk management
- Anyone curious about the Kelly Criterion

## License

MIT

## Disclaimer

This tool is for **educational purposes only**. It does not constitute financial advice. Past performance and simulated results do not guarantee future returns. Always do your own research before trading.
