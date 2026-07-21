# AnalyticClarity.com

Advanced Analytics For Strategy Tester

**[analyticclarity.com](https://analyticclarity.com/)**

I created this project due to a real problem I saw among traders. MetaTrader 5 is an extremely popular and commonly used platform among traders that provides accurate back testing and some analytics, but what most traders fail to realize is that passing a back test simply is not sufficient to verify a valid strategy. Strategies are often over-fitted, or pass a backtest by pure luck. Institutions and hedge funds know this and perform a number of other tests to determine a viable strategy. I aim to help provide SOME of these institutional level tests for free. This is where [analyticclarity.com](https://analyticclarity.com/) comes in.

> **Note:** This could also work for custom Python strategy setups, provided your documented trades match the same format as MT5.

## How It Works

1. Export your trade history from MetaTrader 5 as a detailed CSV report.
2. Upload the CSV on the site and select the Trading Diagnostics analysis.
3. Download a generated PDF report covering performance, risk, and robustness.

## What the Analysis Covers

- **Portfolio performance** — total returns, drawdown analysis, equity growth visualisation
- **Trade-by-trade breakdown** — win/loss split, best and worst trades, execution quality
- **Risk assessment** — drawdown history, recovery analysis, path risk dynamics, behavioural patterns
- **Trade distribution** — win rates, profit factors, R/R analysis, holding periods
- **Session performance** — time-of-day analysis, session-specific returns, volatility patterns
- **Diversification and concentration** — symbol concentration, correlation matrix, beta vs the S&P 500
- **Statistical testing** — permutation tests and bootstrap confidence intervals, to help separate skill from luck
- **Robustness testing** — trade-removal stress tests, cost sensitivity, slippage modelling
- **Market regime analysis** — performance broken down by market conditions (calm / normal / turbulent)
- **Benchmark comparison** — measured against real S&P 500 market data
- **Strategy scoring** — a composite rating across profitability, consistency, and risk management
- **Educational content** — clickable table of contents and a glossary of the metrics used

## MT5 Export Requirements

For the analytics to be accurate, your MetaTrader 5 export must include:

- **Balance rows** — deposit (`DEP:`) and withdrawal (`WD:`) entries, used to reconstruct your starting balance
- **Complete trade history** — all closed positions with timestamps, P&L, commission, and swap

To export from MT5: right-click in the **Account History** tab → select **All History** or a custom date range → right-click again → **Report** → **Save as Detailed Report**, in CSV format with all transactions.

If the balance rows are missing, the platform will report a clear error rather than silently producing wrong numbers.

## Tech Stack

- **Frontend:** React
- **Backend:** Python + Flask
- **Analytics:** pandas, NumPy, SciPy
- **Reporting:** ReportLab (PDF generation), Matplotlib
- **Market data:** yfinance

I have also learnt full stack web development and deployment through this personal project.

## Team

- [@PaceWalker14](https://github.com/PaceWalker14)
- [@JoshSawyer](https://github.com/joshsawyer)
- [@Pace-Runner](https://github.com/Pace-Runner)
