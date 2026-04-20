# Equity Portfolio Risk Analyser

A Python project exploring how to measure and manage risk in an equity portfolio, using real market data and a progression of techniques from basic statistical analysis through to portfolio optimisation.

This started as a way to get hands-on with quantitative finance concepts I'd been studying in my economics degree — things like Value at Risk and mean-variance optimisation are easy to read about, but building them from scratch with real data is a different experience entirely.

---

## What the project covers

The work is split across four notebooks, each building on the last.

**[01 — Data Pipeline](notebooks/01_data_pipeline.ipynb)**  
Pulls five years of daily price data (2020–2024) for ten diversified equities using `yfinance`, calculates daily returns, and produces summary statistics and a correlation heatmap. The cleaned data is saved locally and used as the input for all subsequent notebooks.

**[02 — VaR & CVaR Analysis](notebooks/02_var_cvar_analysis.ipynb)**  
Implements Value at Risk and Conditional Value at Risk at 90%, 95%, and 99% confidence levels using two methods — historical simulation and parametric (variance-covariance). Also breaks down risk at the individual stock level, which surfaces some interesting differences across the portfolio.

**[03 — Monte Carlo Simulation](notebooks/03_monte_carlo_simulation.ipynb)**  
Runs 10,000 simulated return scenarios and 200 portfolio paths over a 252-day horizon to estimate risk through simulation rather than historical data alone. Includes a comparison of all three VaR methods side by side.

**[04 — Portfolio Optimisation](notebooks/04_portfolio_optimisation.ipynb)**  
Uses mean-variance optimisation to find the maximum Sharpe ratio and minimum volatility portfolios across 5,000 randomly generated allocations. Plots the efficient frontier and compares optimised portfolios against a simple equal-weight benchmark.

---

## Some results worth highlighting

The equal-weight portfolio produced an annualised return of around 15.9% over the period, with a Sharpe ratio of 0.81. Optimising for maximum Sharpe pushed the return up to 17.8% while actually reducing volatility to 15.1% — a Sharpe of 1.18. The minimum volatility portfolio brought annualised vol down to 12.1%, largely by concentrating weight in GLD and BRK-B.

On the risk side, the 95% one-day VaR came out at around -1.6% using historical simulation. The 2022 spike in the rolling VaR chart lines up clearly with the rate-hiking cycle, which was a good real-world validation that the model is picking up what it should.

---

## Portfolio

| Ticker | Company | Sector |
|---|---|---|
| AAPL | Apple | Technology |
| MSFT | Microsoft | Technology |
| JPM | JPMorgan Chase | Financials |
| JNJ | Johnson & Johnson | Healthcare |
| XOM | ExxonMobil | Energy |
| AMZN | Amazon | Consumer Discretionary |
| PG | Procter & Gamble | Consumer Staples |
| BA | Boeing | Industrials |
| GLD | SPDR Gold ETF | Commodities |
| BRK-B | Berkshire Hathaway | Financials |

---

## Tech stack

- **Data:** `yfinance`, `pandas`, `numpy`
- **Risk modelling:** `scipy`
- **Optimisation:** `scipy.optimize`
- **Visualisation:** `matplotlib`, `seaborn`
- **Environment:** Python 3, Jupyter Notebook, Anaconda

---

## Project status

| Notebook | Status |
|---|---|
| 01 — Data Pipeline | ✅ Complete |
| 02 — VaR & CVaR Analysis | ✅ Complete |
| 03 — Monte Carlo Simulation | ✅ Complete |
| 04 — Portfolio Optimisation | ✅ Complete |

---

## About

Economics student with an interest in data science and quantitative finance. This is part of a broader set of projects applying Python to real financial and economic problems.

Other projects: [House Price Predictive Model](https://github.com/olivercdavies-su) · [Sector Performance Dashboard](https://github.com/olivercdavies-su)
