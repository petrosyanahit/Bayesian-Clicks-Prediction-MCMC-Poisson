# Bayesian Clicks Prediction using MCMC and Poisson Distribution

This project implements Bayesian inference to predict the number of ad clicks per day based on historical data. The prediction model assumes a Poisson distribution for the number of clicks, with a Gamma prior on the Poisson rate parameter. Various Bayesian methods are used to estimate the posterior distribution and calculate credible intervals.

## Project Overview

The project includes the following steps:

1. **Grid Approximation**:
   - Uses 10 possible values for the parameter, based on a Gamma prior (𝑘=10, 𝜃=2).
   - Posterior distribution is computed using a grid-based approach.
   
2. **Conjugate Distribution Approach**:
   - Exploits the Gamma-Poisson conjugacy to derive the posterior distribution analytically.
   - Includes interactive visualizations for better interpretation.

3. **MCMC Algorithm**:
   - Employs Markov Chain Monte Carlo (MCMC) with 3 chains and 500 iterations for warmup.
   - The following diagnostic plots are provided:
     - **Trace Plots**: Shows the convergence behavior of the chains.
     - **Density and Autocorrelation Plots**: Visualize the distribution of chains and autocorrelation between samples.
     - **Shrink Factor Plot**: Displays the Gelman-Rubin statistic for assessing chain convergence.

4. **Credible Intervals**:
   - For each method (grid, conjugate, and MCMC), credible intervals are computed and compared.

## Data Description

The data used in this project represents the number of ad clicks over a 21-day period. The number of clicks is assumed to follow a Poisson distribution, with the goal of predicting future clicks based on this historical data.

## Methods

- **Prior Distribution**: Gamma(𝑘=10, 𝜃=2)
- **Likelihood**: Poisson distribution
- **Posterior Computation**:
  - Grid Approximation
  - Conjugate Distribution
  - MCMC Algorithm with 3 chains and 500 warmup iterations

## Visualizations

The project includes the following visualizations to assess model performance and convergence:

- **Trace Plots**: To check the stability and mixing of the MCMC chains.
- **Density and Autocorrelation Plots**: To visualize the posterior distribution and sample independence.
- **Shrink Factor Plot**: To confirm the convergence of the MCMC algorithm.


