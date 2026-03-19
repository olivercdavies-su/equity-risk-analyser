# Equity Portfolio Risk Analyser

> A Python-based framework for measuring and visualising equity portfolio risk using industry-standard methods — Value at Risk (VaR), Conditional Value at Risk (CVaR), and mean-variance optimisation.

---

## Overview

This project builds a quantitative risk analysis pipeline for a custom equity portfolio. Using real market data, it measures downside risk through multiple methodologies and identifies optimal portfolio allocations that minimise risk for a given level of return.

The project is structured as a progression from simple to sophisticated — mirroring how risk models are layered in practice.

---

## Objectives

- Retrieve and process real historical equity price data via public APIs
- Implement three standard VaR/CVaR estimation approaches:
  - **Historical Simulation** — non-parametric, data-driven
  - **Parametric (Variance-Covariance)** — assumes normally distributed returns
  - **Monte Carlo Simulation** — stochastic path simulation across thousands of scenarios
- Apply mean-variance optimisation to find the minimum-variance portfolio
- Visualise the efficient frontier, return distributions, and portfolio correlation structure

---

## Project Structure

```
equity-risk-analyser/
│
├── notebooks/
│   ├── 01_data_pipeline.ipynb          # Data retrieval and cleaning
│   ├── 02_var_cvar_analysis.ipynb      # Historical & parametric VaR/CVaR
│   ├── 03_monte_carlo_simulation.ipynb # Monte Carlo risk estimation
│   └── 04_portfolio_optimisation.ipynb # Mean-variance optimisation & efficient frontier
│
├── data/                               # Cached price data (auto-generated)
├── outputs/                            # Saved charts and results
├── requirements.txt
└── README.md
```

---

## Tech Stack

| Tool | Purpose |
|---|---|
| `yfinance` | Real equity price data retrieval |
| `pandas` / `numpy` | Data processing and return calculations |
| `scipy` / `cvxpy` | Portfolio optimisation |
| `matplotlib` / `seaborn` | Visualisation |

---

## Key Concepts

**Value at Risk (VaR)** — the maximum expected loss over a given time horizon at a specified confidence level (e.g. 95% or 99%).

**Conditional VaR (CVaR)** — the expected loss *given* that the loss exceeds the VaR threshold. A more conservative and coherent risk measure.

**Mean-Variance Optimisation** — finds portfolio weights that minimise portfolio variance (risk) for a target level of return, tracing out the efficient frontier.

---

## Status

| Phase | Status |
|---|---|
| Data pipeline | In progress |
| Historical & parametric VaR/CVaR | Planned |
| Monte Carlo simulation | Planned |
| Portfolio optimisation | Planned |
| Visualisations & writeup | Planned |

