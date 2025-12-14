# Enhanced Mean-Variance Optimization Using a Multi-Branch LSTM

This repository hosts a research write-up exploring the use of a custom multi-branch LSTM architecture within a mean-variance optimization (MVO) framework for portfolio construction.

The objective of this work was **not** to maximize backtest performance, but to evaluate whether architectural inductive bias—via asset-specific recurrent branches—can improve robustness, scalability, and stability under realistic financial constraints.

---

## Motivation

Advanced machine learning models are often assumed to outperform classical portfolio optimization techniques. In practice, however, increased model complexity can introduce fragility, overfitting, and sensitivity to regime shifts.

This project investigates that trade-off explicitly by:
- comparing a predictive Multi-Branch LSTM–driven MVO pipeline against a tuned standard MVO baseline,
- prioritizing failure analysis and robustness over headline performance metrics,
- and critically evaluating when added complexity is unjustified.

---

## Key Findings

- **Standard MVO outperformed the enhanced approach** under realistic rebalancing and transaction cost assumptions, achieving superior risk-adjusted returns.
- **Architectural complexity did not reliably translate to better portfolio outcomes**, highlighting the limits of predictive modeling in noisy financial environments.
- **The primary advantage of the Multi-Branch LSTM lies in computational structure**, enabling efficient weight computation for larger asset universes when covariance estimates are precomputed.
- Careful design choices—particularly around loss functions, normalization, and training dynamics—had a greater impact on stability than model expressiveness alone.

---

## Research Emphasis

This work focused on **understanding failure modes**, including:
- loss function sensitivity under noisy targets,
- normalization strategies that preserve temporal autocorrelation,
- training instabilities introduced by scheduling and optimization choices,
- and degradation under regime changes.

Several architectural and training variants were explored but are omitted for brevity, as they exhibited similar fragility characteristics.

---

## Model Confidentiality

To protect ongoing research and scalability considerations:
- source code,
- proprietary data,
- and exact architectural specifications

are intentionally excluded.

The accompanying report emphasizes **reasoning, experimental design, and conclusions**, rather than implementation details.

---

## Contents of the Report

The full write-up covers:
- Model selection rationale and architectural design
- Data preprocessing and training considerations
- Failure modes and design trade-offs
- Scalability and liquidity constraints
- Comparative analysis: Standard vs. Enhanced MVO
- Key takeaways and limitations
- Directions for future research

---

## Takeaway

This project demonstrates that in portfolio optimization, **robustness and simplicity often dominate expressive modeling**, and that rigorous evaluation of when *not* to use machine learning is as valuable as successful application.

The primary contribution of this work lies in **architectural reasoning and failure analysis**, rather than performance gains.


## Author

Chaitanya Anil Palghadmal  
[work.chaitanyap@gmail.com](mailto:work.chaitanyap@gmail.com)
