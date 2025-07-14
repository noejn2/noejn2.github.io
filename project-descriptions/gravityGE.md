---
layout: page
title: "gravityGE: Gravity Models with General Equilibrium"
---

# gravityGE R/Julia Package

The **gravityGE** package implements a one-sector Armington-CES gravity model with general equilibrium (GE) effects. This model is designed to analyze international and domestic trade by capturing the impacts of trade costs and policy changes within a general equilibrium framework. Additionally, it includes a local parameter to run simulations on productivity. The package provides functions for calibration, simulation, and analysis of the model.

## Key Features

- **One-Sector Armington-CES Framework**: Implements the standard trade model with product differentiation by country of origin
- **General Equilibrium Effects**: Captures economy-wide impacts of trade policy changes
- **Trade Cost Analysis**: Analyzes the effects of various trade costs on bilateral trade flows
- **Policy Simulation**: Evaluates the impacts of trade policy changes within a GE framework
- **Productivity Analysis**: Includes parameters for running productivity-based simulations
- **Calibration Tools**: Provides functions for model calibration and parameter estimation

## R Installation

```r
# Install from CRAN
install.packages("gravityGE")

# Load the package
library(gravityGE)
```

**CRAN Package**: [https://CRAN.R-project.org/package=gravityGE](https://CRAN.R-project.org/package=gravityGE)



## Julia Installation

```julia
# Installing the package in environment
import Pkg
Pkg.add(gravityGE)

using gravityGE
```