# Bayesian Homework

This repository contains a Jupyter Notebook (`Hw8.ipynb`) that demonstrates three different Bayesian modeling tasks using PyMC. Below is a brief overview of each question, the data used, and the general approach taken.

---

## Contents

- **`Hw8.ipynb`**: Main notebook implementing the Bayesian models for Q1, Q2, and Q3.
- **`Raisin_Dataset.csv`**: Dataset for Q1 (Binary outcome for logistic regression).
- **`StudentsPerformance.csv`**: Dataset for Q2 (Multiple continuous outcomes for multivariate regression).
- **`train.csv`**: Dataset for Q3 (Multiple binary outcomes for multivariate classification).

---

## Q1: Bayesian Logistic Regression

**Objective**  
- Model a binary outcome using a Bernoulli likelihood with a logit link function.  
- Place independent Normal priors on the regression coefficients.

**Data**  
- **Raisin_Dataset.csv**: Features describing raisin varieties (binary classification).

**Approach**  
- Used PyMC to build and sample from a logistic regression model.
- Performed MCMC to obtain posterior distributions for the coefficients.
- Assessed convergence via MCMC diagnostics (trace plots, summary statistics).

---

## Q2: Bayesian Multivariate Regression

**Objective**  
- Handle multiple continuous outcomes (e.g., 15 yearly measurements) as a multivariate response.
- Place independent Normal priors on the regression coefficients.
- Use an LKJCholeskyCov prior for the response covariance.

**Data**  
- **StudentsPerformance.csv**: Example data repurposed to illustrate multiple continuous outcome columns (e.g., reading, math, writing scores).

**Approach**  
- Constructed a design matrix with an intercept and standardized predictor.
- Implemented a multivariate normal model in PyMC, sampling the regression coefficients and the covariance matrix.
- Examined posterior summaries, trace plots, and covariance matrix estimates to ensure reasonable inference and convergence.

---

## Q3: Bayesian Multivariate Classification

**Objective**  
- Model multiple binary outcomes simultaneously via a latent variable approach (e.g., probit regression).
- Place independent Normal priors on the regression coefficients.
- Specify an appropriate prior for the latent covariance structure (e.g., LKJ).

**Data**  
- **train.csv**: Contains multiple binary outcomes for classification tasks.

**Approach**  
- Created a latent variable model in PyMC, linking binary responses to underlying normal variables.
- Performed MCMC sampling to estimate posterior distributions of coefficients and the latent covariance.
- Used diagnostic plots to assess model performance and ensure convergence.

---
