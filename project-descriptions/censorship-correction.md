# Censorship Correction in Almost Ideal Demand (AID) systems

This research introduces a methodological advance in demand estimation by integrating **censoring corrections into Quadratic Almost Ideal Demand Systems (QUAIDS)**. The approach addresses a key challenge in applied demand analysis: households often report zero consumption of certain goods, which, if ignored, can bias results. By embedding censoring directly into the QUAIDS framework, the method enables more accurate and behaviorally consistent estimation of demand elasticities and welfare effects, as demonstrated in the evaluation of Mexico's sugar-sweetened beverage tax.

## Methodological Overview

The core innovation is a unified estimation framework that simultaneously models both the decision to purchase (extensive margin) and the amount consumed (intensive margin). This is achieved by:

* **Accounting for zero-purchase behavior**: Properly handling censored (zero) observations in household survey data
* **Implementing truncated log-likelihood estimation**: Allowing for joint estimation of purchase incidence and consumption levels
* **Preserving theoretical consistency**: Producing demand elasticities that respect economic theory, including Engel aggregation and Cournot consistency
* **Improving welfare analysis**: Providing a structurally coherent alternative to two-step censored models, resulting in more credible welfare estimates

## The censoredAIDS R Package

The methodology is implemented in the **censoredAIDS** R package, available on CRAN. This package equips applied researchers with practical tools for estimating censored Almost Ideal (AI) and Quadratic Almost Ideal (QUAI) demand systems using Maximum Likelihood Estimation.

**CRAN Package**: [https://CRAN.R-project.org/package=censoredAIDS](https://CRAN.R-project.org/package=censoredAIDS)
**DOI**: [10.32614/CRAN.package.censoredAIDS](https://doi.org/10.32614/CRAN.package.censoredAIDS)

### Key Features

* **Censored demand system estimation** for both AI and QUAI models
* **Maximum Likelihood Estimation** with truncated log-likelihood functions
* **Integration of demographic variables** into demand share equations
* **Numerical approximation of elasticities** with standard errors via the Delta Method
* **Designed for zero-purchase data** common in household consumption surveys

### Installation and Usage

```r
# Install from CRAN
install.packages("censoredAIDS")

# Load the package
library(censoredAIDS)
```

### Dependencies

Requires R (≥ 3.5) and imports: Matrix, mnormt, mvtnorm, stats, and matrixcalc.

### Package Description

The censoredAIDS package provides functions for estimating censored AI and QUAI demand systems, calculating demand share equations, and handling censored data where some observations are zero due to non-purchase. It also includes procedures for numerical approximation of demand elasticities and estimation of standard errors, making it especially useful for applied research with household consumption data.

