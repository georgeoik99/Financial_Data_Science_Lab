# Financial Data Science Lab

**Quantitative Finance · Financial Mathematics · Python · Portfolio Analytics · Risk Management · Machine Learning**

A collection of focused, notebook-based case studies exploring how mathematical models and Python can be applied to financial markets. The repository combines financial theory, empirical market data, simulation, portfolio construction, and risk measurement.

The emphasis is on understanding **model assumptions, implementation choices, and economic interpretation**—not on claiming that more complex models necessarily deliver better investment outcomes.

## Projects

### Financial Mathematics & Risk Analytics

| Project | Focus | Market / Instruments |
| --- | --- | --- |
| [Binomial Stock Dynamics & One-Period Option Pricing](binomial-stock-dynamics/) | Discounting, binomial price dynamics, physical vs. risk-neutral probabilities, martingales, European option payoffs, replicating portfolios, and no-arbitrage pricing. | TotalEnergies ADR (`TTE`) |
| [Continuous-Time Financial Models](continuous-time-financial-models/) | Brownian motion, Itô's lemma, Geometric Brownian Motion, Ornstein–Uhlenbeck mean reversion, calibration, and risk-neutral dynamics. | NVIDIA (`NVDA`); WTI crude oil futures (`CL=F`) |
| [Fixed Income & Yield Curve Analytics](fixed-income-yield-curve-analytics/) | Bond pricing and yield to maturity, duration, convexity, Treasury yield curves, Nelson–Siegel fitting, and illustrative short-rate models. | U.S. Treasury yields / FRED |
| [Greek Equity Portfolio Optimization & Risk Analytics](greek-equity-portfolio-risk-analytics/) | Diversification, mean–variance optimization, efficient frontier, tangency portfolio, CAPM, performance measures, and historical VaR / CVaR. | Greek equities and ATHEX Composite |
| [Multi-Asset ETF Risk Management & Stress Testing](multi-asset-etf-risk-management/) | Historical, Gaussian, Student-t, and Monte Carlo VaR; Expected Shortfall; multi-day risk; stress scenarios; and the limitations of VaR. | `SPY`, `SOXX`, `XLE`, `TLT`, `GLD` |

### Portfolio Strategies & Applied Machine Learning

| Project | Focus | Market / Instruments |
| --- | --- | --- |
| [Portfolio Allocation Rules](portfolio-allocation-rules/) | Equal-weight and inverse-volatility allocation rules, with an S&P 500 comparison. | Equity portfolio / S&P 500 |
| [Investment Strategies & ML Classification](investment-strategies-and-ml/) | Greek equity investment strategies and MLP / LSTM classification using European oil-sector market data. | Greek equities; Repsol / European oil sector |

Each folder has its own README describing its methodology and usage. The projects are separate case studies; they are **not** presented as one unified trading system.

## Repository Structure

```text
Financial_Data_Science_Lab/
├── binomial-stock-dynamics/
├── continuous-time-financial-models/
├── fixed-income-yield-curve-analytics/
├── greek-equity-portfolio-risk-analytics/
├── investment-strategies-and-ml/
├── multi-asset-etf-risk-management/
├── portfolio-allocation-rules/
├── .gitignore
└── README.md
```

## Approach

The financial-mathematics notebooks generally follow this sequence:

**Financial question → Mathematical formulation → Python implementation → Numerical or empirical results → Interpretation and limitations**

Depending on the project, the work includes market-data calibration, simulated scenarios, optimization, statistical estimation, or comparisons with reference strategies. Where hypothetical rates or stress shocks are used, they are intended for illustration rather than as live market forecasts.

## Tools

- **Core:** Python, Jupyter, NumPy, pandas, Matplotlib, SciPy
- **Market data:** yfinance; FRED data where relevant
- **Machine learning:** scikit-learn and TensorFlow/Keras in the applicable project

Dependencies differ by project; use its local `requirements.txt` when provided.

## Getting Started

1. Open the folder of the project you want to explore.
2. Read that project's `README.md` for its data sources and setup instructions.
3. Install its dependencies (where a requirements file is supplied):

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open the notebook in Jupyter or VS Code and run its cells in order.

Some notebooks download financial data at runtime and require internet access. Download availability, ticker symbols, historical data revisions, and provider APIs can affect reproducibility.

## Scope & Disclaimer

This repository is an **educational and portfolio research collection**, not a live trading or investment-advice service. Model-based prices, simulated paths, backtests, VaR, and stress scenarios depend on assumptions and historical information. Past performance and estimated risk measures do not guarantee future outcomes.
