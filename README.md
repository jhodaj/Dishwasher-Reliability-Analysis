# Dishwasher Reliability and Failure-Mode Analysis

## Overview

This project evaluates the reliability of dishwasher spray arms under two competing failure modes: **breakage** and **obstruction**.

The analysis combines parametric and nonparametric reliability methods to characterize failure behavior, estimate survival probabilities, compare candidate lifetime distributions, and identify which failure mechanism presents the greater reliability concern.

For each failure mode, failures from the competing mechanism are treated as right-censored observations.

## Objectives

The project aims to:

- Model the lifetime behavior of dishwasher spray arms under breakage and obstruction.
- Compare alternative lifetime distributions using probability plots and maximum-likelihood estimation.
- Estimate survival probabilities using Kaplan–Meier methods.
- Compare the two failure mechanisms.
- Evaluate overall dishwasher reliability when both failure modes are considered.

## Methods

The analysis was conducted in **R** using reliability and survival-analysis methods including:

- Right-censored lifetime data analysis
- Maximum-likelihood estimation
- Weibull, lognormal, loglogistic, and Fréchet distribution comparisons
- Probability plots
- Kaplan–Meier survival estimation
- Survival and hazard-function estimation
- Reliability quantiles and confidence intervals
- Likelihood-ratio testing
- Multiple-failure-mode reliability analysis

## Key Results

### Breakage

The **Weibull distribution** provided the best fit among the candidate distributions considered for spray-arm breakage.

- Estimated mean time to failure (MTTF): **790.6 cycles**
- Approximately 95% of spray arms survived breakage for at least **141.9 cycles**

### Obstruction

The **Fréchet distribution** provided the best fit among the candidate distributions considered for spray-arm obstruction.

- The MTTF does not exist under the fitted Fréchet model because of its estimated shape parameter.
- Approximately 95% of spray arms survived obstruction for at least **10.2 cycles**

### Reliability Insight

The analysis indicates that **obstruction occurs substantially earlier than breakage**, making obstruction the more immediate reliability concern for the spray-arm system.

When both failure mechanisms are considered, approximately 95% of spray arms survived at least **10.2 cycles**.

## Repository Structure

```text
dishwasher-reliability-analysis/
│
├── README.md
├── Dishwasher_Reliability_Analysis.Rmd
├── Dishwasher_Reliability_Analysis.pdf
├── Dishwasher_Reliability_Presentation.Rmd
├── Dishwasher_Reliability_Presentation.pdf
├── references.bib
├── appendix.md
│
└── data/
    ├── DishwasherBreakonly.csv
    ├── DishwasherObstructiononly.csv
    ├── DishwasherReliability1.csv
    ├── DishwasherReliability2.csv
    ├── DishwasherReliabilityBreak.csv
    ├── DishwasherReliabilityBreak2.csv
    ├── DishwasherReliabilityObstruction.csv
    └── DishwasherReliabilityObstruction2.csv
