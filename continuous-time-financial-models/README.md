# Continuous-Time Financial Models

Financial Mathematics + Python project covering Brownian motion, Itô calculus, GBM, Ornstein–Uhlenbeck mean reversion and the continuous-time equivalent martingale measure.

## Experiments
- NVIDIA (`NVDA`) — GBM calibration and simulation
- WTI Crude Oil (`CL=F`) — OU mean-reversion calibration

## Structure
```text
continuous-time-financial-models/
├── README.md
├── requirements.txt
└── continuous_time_financial_models.ipynb
```

## Run
```bash
python -m pip install -r requirements.txt
jupyter notebook continuous_time_financial_models.ipynb
```

The notebook stops before Black–Scholes option pricing.

Educational research only; not investment advice.
