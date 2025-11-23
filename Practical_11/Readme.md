# Sunspot Activity Analysis using Gamma Distribution and MCMC

This notebook performs an analysis of monthly mean total sunspot numbers, modeling the phenomenon using a Gamma distribution and estimating its parameters using a Metropolis-Hastings Markov Chain Monte Carlo (MCMC) algorithm.

## Project Overview

The project aims to analyze historical sunspot data, understand its distribution, and apply Bayesian inference using MCMC to estimate the parameters of a Gamma distribution that models sunspot activity. The analysis considers different segments of the data (first 50 samples, all samples, last 50 samples) to observe how parameter estimates might vary over time.

## Data Loading and Preprocessing

The sunspot data is loaded from a publicly available `.txt` file provided by the SILSO (Sunspot Index and Long-term Solar Observations) World Data Center. The data includes monthly mean total sunspot numbers from 1749 to the present.

- **Source**: `https://www.sidc.be/silso/DATA/SN_m_tot_V2.0.txt`
- The data is loaded into a pandas DataFrame, with columns such as `year`, `month`, `decimal_date`, and `sunspot`.
- A `date` column is created by combining `year` and `month` for time-series analysis.

## Exploratory Data Analysis (EDA)

Initial exploration includes:
- Plotting the monthly mean total sunspot number over the entire period to visualize long-term trends and cyclical patterns.
- Generating a histogram of sunspot counts to understand their overall distribution.

## Modeling with Gamma Distribution

The sunspot phenomenon is modeled with a Gamma distribution. To account for potential changes over long periods, the data is divided into 12-year cycles, and Gamma distribution parameters (`a` and `b`) are fitted for each cycle.

- The notebook calculates a `cycle_id` for each data point based on 12-year intervals.
- For each cycle, the `scipy.stats.gamma.fit` function is used to estimate the shape (`a`) and rate (`b`) parameters of the Gamma distribution.

## Metropolis-Hastings MCMC Analysis

A custom Metropolis-Hastings algorithm is implemented to estimate the posterior distribution of the Gamma distribution parameters (`a` and `b`).

- **`log_posterior_gamma_ab(y, a, b)`**: This function calculates the log-posterior probability given data `y`, shape `a`, and rate `b`. It combines the log-likelihood of the Gamma distribution with a weakly informative prior `p(a,b) ∝ 1/(1+a^2) * 1/(1+b^2)`.
- **`mcmc_gamma_ab(y, a0, b0, n_iter, proposal_scale)`**: This function runs the MCMC sampler.
    - It uses a random-walk proposal, where new `a` and `b` values are proposed from a normal distribution centered at the current values.
    - The sampler is run for `n_iter` iterations (defaulting to 5000).
- The MCMC is run on three different data subsets:
    - `y_first50`: The first 50 sunspot observations.
    - `y_all`: All sunspot observations.
    - `y_last50`: The last 50 sunspot observations.

## Posterior Analysis

After running the MCMC:
- **Trace Plots**: The traces of `a` and `b` parameters are plotted for each data subset to visually assess convergence and mixing of the chains. A burn-in period (defaulting to 1000 iterations) is applied.
- **Posterior Histograms**: Histograms of the post-burn-in `a` and `b` samples are generated to visualize their marginal posterior distributions.
- **Posterior Summaries**: Mean, median, and 95% credible intervals are calculated for `a` and `b` from the post-burn-in MCMC samples for each data subset, providing quantitative summaries of the parameter estimates.

## Dependencies

- `numpy`
- `pandas`
- `matplotlib.pyplot`
- `scipy.stats`
- `seaborn`
