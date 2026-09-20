# Fixed Income & Yield Curve Analytics

Financial Mathematics + Python project covering bond valuation, interest-rate risk, real Treasury yield-curve analytics and classical short-rate models.

## Main workflow

```text
Bond Cash Flows
    ↓
Price / Yield
    ↓
Newton-Raphson YTM
    ↓
Duration
    ↓
Convexity
    ↓
U.S. Treasury Yield Curve
    ↓
Forward Rates
    ↓
Nelson-Siegel Curve Fitting
    ↓
Vasicek / CIR
```

## Real-market data

The notebook downloads U.S. Treasury constant-maturity yields from FRED at runtime for 1M, 3M, 6M, 1Y, 2Y, 5Y, 10Y, 20Y and 30Y maturities.

## Structure

```text
fixed-income-yield-curve-analytics/
├── README.md
├── requirements.txt
└── fixed_income_yield_curve_analytics.ipynb
```

## Run

```bash
python -m pip install -r requirements.txt
jupyter notebook fixed_income_yield_curve_analytics.ipynb
```

Internet access is required for the FRED section.

## Modeling note

Treasury constant-maturity yields are not identical to zero-coupon spot rates, so forward-rate calculations based directly on them are labeled as educational approximations. Vasicek and CIR parameters are illustrative, not live calibrated.

> Educational quantitative-finance research only. Not investment advice.
