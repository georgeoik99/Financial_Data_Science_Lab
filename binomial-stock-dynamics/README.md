# Binomial Stock Dynamics & One-Period Option Pricing

A Financial Mathematics + Python project that develops the binomial stock model from first principles and extends it to one-period European option pricing.

## Underlying

- **TotalEnergies SE ADR (`TTE`)** — used for empirical calibration.

The project uses one underlying instead of mixing market calendars.

## Topics

- Discounting and time value
- Binomial stock-price dynamics
- Log returns and empirical calibration
- Filtrations and conditional expectation
- Markov property
- Discounted prices and martingales
- Physical probability `P` vs risk-neutral probability `Q`
- No-arbitrage condition
- European call and put payoffs
- Risk-neutral option valuation
- Replicating portfolios
- Mispricing and arbitrage
- Buyer/seller superhedging prices
- Complete markets and unique martingale measure
- Monte Carlo martingale checks
- CLT and lognormal limiting structure

## Core option-pricing equations

\[
q=\frac{1+r-d}{u-d}
\]

and

\[
V_0=\frac{qF_u+(1-q)F_d}{1+r}.
\]

The replicating stock position is

\[
\theta_1=\frac{F_u-F_d}{S_0(u-d)}.
\]

The notebook verifies numerically that

\[
\text{risk-neutral value}
=
\text{replication cost}.
\]

## Structure

```text
binomial-stock-dynamics/
├── README.md
├── requirements.txt
└── binomial_stock_dynamics.ipynb
```

## Run

```bash
python -m pip install -r requirements.txt
jupyter notebook binomial_stock_dynamics.ipynb
```

Market data are downloaded at runtime with `yfinance`.

## Scope

The current version stops at **one-period option pricing**. Multi-period trees and backward induction are intentionally deferred until they appear in the course material.

> Educational quantitative-finance research only. Not investment advice.
