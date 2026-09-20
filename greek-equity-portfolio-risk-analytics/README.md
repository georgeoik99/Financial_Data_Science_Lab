# Greek Equity Portfolio Optimization & Risk Analytics

A Financial Mathematics + Python portfolio project focused on the Athens Stock Exchange.

## Equity universe

- Public Power Corporation / ΔΕΗ (`PPC.AT`)
- OTE / Hellenic Telecommunications Organization (`HTO.AT`)
- GEK TERNA (`GEKTERNA.AT`)
- Motor Oil Hellas (`MOH.AT`)
- National Bank of Greece (`ETE.AT`)

**Market proxy:** ATHEX Composite Index (`GD.AT`)

The universe intentionally combines different sectors so the project can study diversification rather than simply grouping highly similar stocks.

## Main workflow

```text
Greek Equity Returns
        ↓
Mean / Covariance / Correlation
        ↓
Diversification
        ↓
Monte Carlo Opportunity Set
        ↓
Markowitz Optimization
        ↓
Efficient Frontier
        ↓
ECB Risk-Free Proxy
        ↓
Tangency Portfolio + CML
        ↓
CAPM
        ↓
VaR / CVaR
        ↓
Performance Indices
```

## Methods

- Portfolio expected return and variance
- Covariance and diversification
- Equal-weight diversification experiment
- Monte Carlo feasible portfolios
- Global Minimum Variance portfolio
- Long-only efficient frontier
- Maximum-Sharpe / tangency portfolio
- Capital Market Line
- CAPM alpha and beta against the ATHEX Composite
- Historical VaR
- Historical CVaR / Expected Shortfall
- Gaussian VaR
- Sharpe ratio
- Treynor ratio
- Jensen alpha
- Appraisal ratio
- Maximum drawdown

## Risk-free proxy

The notebook downloads the latest **ECB Deposit Facility Rate** from FRED at runtime and uses it as a euro-area risk-free proxy for the Sharpe/CML/CAPM sections.

It is explicitly treated as a proxy rather than a perfectly investable risk-free security.

## Structure

```text
greek-equity-portfolio-risk-analytics/
├── README.md
├── requirements.txt
└── greek_equity_portfolio_risk_analytics.ipynb
```

## Run

```bash
python -m pip install -r requirements.txt
jupyter notebook greek_equity_portfolio_risk_analytics.ipynb
```

Internet access is required for Yahoo Finance and FRED downloads.

## Academic basis

The project follows the MSc Financial Mathematics material on:

- portfolio returns,
- covariance and diversification,
- Markowitz mean-variance optimization,
- efficient frontier,
- Tobin model and Capital Market Line,
- Sharpe ratio,
- CAPM,
- portfolio performance measures.

The supplied classroom `portfolio.ipynb`, `var.ipynb`, and historical Refinitiv/Eikon CSV were used as conceptual references. The final implementation is rebuilt for a Greek-equity case study rather than reproducing the original classroom dataset.

## Important implementation improvements

This version uses internally consistent portfolio formulas:

- annual covariance = `252 × daily covariance`,
- Sharpe denominator = portfolio **volatility**,
- simple returns for exact weighted portfolio returns,
- explicit long-only constraints,
- positive loss conventions for VaR/CVaR,
- current risk-free proxy downloaded at runtime.

> Educational quantitative-finance research only. Not investment advice.
