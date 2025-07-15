# Heterogenous Patterns of Crop Yield Growth Stagnation across U.S. Counties in the Next Decade

The full research paper is available here: [Full Paper (PDF)](../project-assets/Nava-jmp-bayes.pdf).

This paper introduces a **hierarchical Bayesian framework** that models the interaction between climate variables and crop yield growth at the U.S. county level, enabling **probabilistic short-term yield projections**.

The main methodological innovation is the development of a **parametrized Beta-type likelihood model** for crop yields, where both **location and spread parameters** depend on weather variables—specifically, precipitation, growing degree days (GDD), and extreme degree days (EDD). Key features include:

* **Flexible link functions** to ensure parameter domain validity and interpretability;
* **Hamiltonian Monte Carlo (H-MCMC)** for posterior sampling, allowing the model to handle complex dependencies and high-dimensional parameter spaces;
* A **hierarchical prior structure** that allows parameter variation across counties, incorporating both temporal and spatial heterogeneity;
* Estimation of **joint weather effects** using a multivariate prior on weather coefficients, with hyperpriors enabling correlation among climate impacts;
* Integration of **IPCC-based climate forecasts (SSP2-4.5)** into the simulation process, yielding interpretable and robust probabilistic forecasts.

Compared to previous methods (e.g., Ricardian or standard Beta models), this framework uniquely combines **distributional flexibility, unit-level heterogeneity, and full Bayesian inference**, making it particularly suited for short-term, spatially disaggregated climate impact assessment. The methodology is demonstrated through 2032 projections for corn and soybean yields under different crop growth regimes.

For a visual overview, see the slides [ers-aaea2023 (PDF)](../project-assets/ers-aaea2023-session.pdf), presented at the AAEA 2023 meeting in Washington, DC.
