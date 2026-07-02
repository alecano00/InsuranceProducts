[readme_InsuranceProducts.md](https://github.com/user-attachments/files/29589143/readme_InsuranceProducts.md)
# Insurance Product
**Author:** Alessandro Canola Gavioli

## Overview
This repository contains a quantitative analysis and simulation project focused on actuarial loss modeling. The project explores the statistical properties of insurance losses, fits parametric distributions to the data, and uses Monte Carlo and Bootstrap techniques to estimate aggregate risk.

## Methodology
The analysis is divided into several key phases:
1. **Exploratory Data Analysis (EDA):** Visualizing loss data via histograms and empirical distributions to identify trends and potential heavy tails.
2. **Distribution Fitting & Selection:**
   - Fitting various parametric models (Gamma, Log-Normal, Normal) using Maximum Likelihood Estimation (MLE).
   - Comparing models using statistical tests (Kolmogorov-Smirnov) and information criteria (AIC, BIC).
3. **Aggregate Loss Simulation:**
   - **Monte Carlo Method:** Simulating aggregate losses by combining a frequency model (Poisson distribution) with a severity model (Log-Normal distribution).
   - **Bootstrap Resampling:** Using the empirical data directly to generate a non-parametric Bootstrap CDF for aggregate losses, providing a robust check against parametric assumptions.
4. **Risk Metrics:** Implementation of premium calculation principles based on variance (Premium = $\mathbb{E}[L] + \alpha \cdot \text{Var}(L)$).

## Key Components
* **KDE (Kernel Density Estimation):** Used to produce a smooth representation of the loss density function, aiding in visual distribution assessment.
* **Empirical CDF:** Used to compare the performance of theoretical distributions against the actual observed data.
* **Bootstrap Method:** Re-sampling the claim dataset to estimate the variability of the aggregate loss distribution without assuming a specific parametric form.

## Files
* `ASMT.ipynb`: The main notebook containing all Python code for fitting, simulation, visualization, and validation.
