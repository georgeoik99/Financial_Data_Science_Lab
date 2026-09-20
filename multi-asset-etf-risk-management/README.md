# Multi-Asset ETF Risk Management & Stress Testing

A Financial Mathematics + Python project focused on portfolio risk measurement rather than return forecasting.

## ETF universe

- SPY — broad U.S. equities
- SOXX — semiconductors
- XLE — energy / oil equities
- TLT — long-duration U.S. Treasuries
- GLD — gold

All instruments trade in the U.S. market and share one aligned trading calendar.

## Main workflow

```text
ETF Returns
    ↓
Portfolio Loss Distribution
    ↓
Historical VaR / ES
    ↓
Gaussian VaR
    ↓
Student-t VaR
    ↓
Monte Carlo VaR / ES
    ↓
Multi-day Risk
    ↓
Stress Testing
    ↓
VaR Failure Example
    ↓
Convex Risk Measures
```

## Mathematical topics

- Loss distributions
- Value at Risk
- Normal VaR
- Location-scale VaR
- Student-t tails
- Correlation and portfolio volatility
- Square-root-of-time scaling
- Simulation-based VaR
- Risk-factor mapping
- Expected Shortfall / Average VaR
- Tail VaR
- Subadditivity
- Convex risk measures

## Portfolio convention

The notebook uses an equal-weight €100,000 portfolio:

```text
SPY   20%
SOXX  20%
XLE   20%
TLT   20%
GLD   20%
```

Loss is defined as the negative of portfolio P&L, so positive values represent losses.

## Stress scenarios

The notebook includes illustrative shocks for:

- semiconductor stress,
- energy/oil stress,
- rising-rate stress,
- broad risk-off conditions.

These are scenario-analysis inputs, not forecasts.

## Structure

```text
multi-asset-etf-risk-management/
├── README.md
├── requirements.txt
└── multi_asset_etf_risk_management.ipynb
```

## Run

```bash
python -m pip install -r requirements.txt
jupyter notebook multi_asset_etf_risk_management.ipynb
```

Internet access is required for Yahoo Finance data.

## Academic basis

The notebook follows the Financial Mathematics lecture on **Value at Risk and other risk measures**, including:

- VaR as a loss quantile,
- Gaussian and location-scale examples,
- portfolio VaR,
- multi-period volatility scaling,
- simulation-based VaR,
- the failure of VaR under default-type risks,
- Tail VaR / Expected Shortfall,
- convex risk measures.

The defaultable-bond example is retained because it provides the clearest demonstration of why VaR alone can be misleading.

> Educational quantitative-finance research only. Not investment advice.
