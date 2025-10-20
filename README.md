# market-diffusion
> *Experiments in probabilistic modelling and diffusion processes for quantitative equity forecasting.*

---

## Overview
**Market Diffusion** is an open research project exploring how  **stochastic differential equations (SDEs)** and the **Fokker-Planck partial differential equation (PDE)** can be model short-horizon equity dynamics.

The workflow layers **numerical diffusion models**, **probabilistic forecasts**, and **portfolio decisions**—with each stage adding a small, testable refinement. The roadmap is exploratory and may evolve as results come in.

---

## Current Focus
**Stage 1 - Crisis-Mode Monte Carlo (fallback on real data)**

- Rigorous, short-horizon Monte Carlo forecaster for stress periods (e.g.,volatility spikes, breadth crashes).
- Produces next-day **mean/variance**, **P[win]**, **95% CI**, **first-passage probabilities** (e.g., "up before down"), and **$ES\_{97.5}\$**.
- Outputs a **conservative action** (with crisis multiplier) and a machine-readable prediction artifact.

Outputs include:
- daily JSON artifacts (per stock) with forecast stats and crisis flags
- metrics (drawdown, ES coverage, calibration) and plots
- LaTeX notes deriving the method and documenting triggers/assumptions


---

## Longer-Term Direction
Planned extensions (subject to change):

- **Emperical** drift/volatility estimation from market data
- One-day diffusion forecasts via **Fokker-Plank (PDE)** with Crank-Nicolson method
- Probability calibration and **Kelly-capped sizing**
- **Portfolio optimisation** with turnover/costs and risk constraints
- **Regime switching** (HMM) and **tail-risk overlay** (copula ES)

---
## Notes
- This repository is research/educational; it does **NOT** provide investment advice.
- Results are backtested; real world performance can differ due to execution, costs, and market impact.
