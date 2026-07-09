# Variance-Reduction-Techniques-for-Monte-Carlo-Pricing-of-European-Call-Options
Comparing the effeciency of several different variance reduction methods.



# Option Pricing & Variance Reduction Analysis

A comparative quantitative finance framework implementing and benchmark-testing classic Monte Carlo variance reduction techniques for pricing European call options under the Black-Scholes model.

This repository hosts the official code implementation accompanying the research paper: [**"Variance Reduction Techniques for Monte Carlo Pricing of European Call Options"**](draft.pdf).

---

## 📊 Overview

Monte Carlo simulation is a highly flexible numerical tool for evaluating financial derivatives, but its standard convergence rate of N^{-1/2} demands significant computational overhead for high-precision pricing. This project systematically implements and visualizes three foundational variance reduction methodologies to optimize estimator efficiency:

1. **Antithetic Variates:** Exploits distribution symmetry by utilizing negatively correlated variable pairs to lower overall sampling variance.
2. **Control Variates:** Minimizes estimator error by applying an analytically tracking correction coefficient against the terminal stock price.
3. **Quasi-Monte Carlo (QMC):** Replaces pseudo-random distributions with scrambled Sobol low-discrepancy sequences to achieve near-deterministic convergence rates.

---

## 📈 Performance Benchmarks

The simulation evaluates pricing errors across six scale dimensions (N = 2^10 up to N = 2^20) over 30 independent runs to evaluate convergence standard deviations against the closed-form analytical Black-Scholes baseline.

* **Antithetic Variates:** Delivers a stable variance reduction factor of approximately 1.5 times to 2 times.
* **Control Variates:** Achieves a powerful efficiency increase, outperforming baseline errors by 4 times to 6 times.
* **Quasi-Monte Carlo (Sobol):** Demonstrates exceptional precision scaling, reducing pricing error variance by up to **two orders of magnitude** compared to naive sampling.

---

## 🛠️ Environment & Tooling

The mathematical pipelines are engineered entirely inside Python utilizing highly optimized scientific computing structures:
* `NumPy` - Vectorized geometric Brownian motion array generations.
* `SciPy` - Low-discrepancy Sobol sequence generators (`scipy.stats.qmc`) and inverse transform distributions.
* `Matplotlib` - Logarithmic convergence visualization engines.

### Prerequisites

To install the necessary dependencies, run:
```bash
pip install numpy scipy matplotlib


## 🚀 How to Run the Simulation

1. Clone this repository to your local machine:
   git clone https://github.com/ayhamalashwal/Variance-Reduction-Techniques-for-Monte-Carlo-Pricing-of-European-Call-Options.git

2. Open the notebook file in Visual Studio Code or Jupyter:
   Variance Reduction Techniques for Monte Carlo Pricing of European Call Options.ipynb

---

## 📜 Citation

If you use this framework or reference the comparative findings in an academic context, please cite the corresponding paper:

@article{alashwal2026variance,
  title={Variance Reduction Techniques for Monte Carlo Pricing of European Call Options},
  author={Alashwal, Ayham Amin},
  year={2026}
}
