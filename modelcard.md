# Model Card for BBO Optimisation Approach

## Overview
- **Name:** Hybrid Local‑Exploration Bayesian Optimisation (HLEBO)
- **Type:** Surrogate‑guided optimisation with manual heuristics
- **Version:** v1.0 (10‑round implementation)

## Intended Use
- **Suitable For:** Educational demonstrations of BBO, reproducibility exercises, peer benchmarking.
- **Avoid:** Deployment in safety‑critical domains (e.g., drug discovery, industrial control) without validation.

## Details
- **Rounds 1–3:** Broad exploration using random and Sobol‑like sampling.
- **Rounds 4–6:** Surrogate modelling with Gaussian Processes (Matern kernel) and UCB/EI acquisition.
- **Rounds 7–9:** Local refinement around promising regions; small perturbations to map gradients.
- **Round 10:** Consolidation phase; exploitation‑heavy with boundary probes in high dimensions.
- **Evolution:** Strategy shifted from global exploration to local exploitation as patterns emerged.

## Performance
- **Metrics:** Function outputs (scalar scores), relative improvements per round.
- **Summary:** Consistent gains in Functions 5 and 7; modest improvements in Functions 3 and 8; plateauing in Functions 1–2.
- **Evaluation:** Success measured by reproducibility of decisions and incremental improvements.

## Assumptions and Limitations
- **Assumptions:** Local smoothness, recent trends predictive, surrogate reliability in low dimensions.
- **Limitations:** Sparse coverage in high dimensions; path dependence; manual heuristics may bias exploration.

## Ethical Considerations
Transparency through datasheets and model cards ensures reproducibility and credibility. Documenting assumptions, biases, and limitations helps peers understand the scope and constraints of my approach. This supports responsible adaptation of optimisation strategies in real‑world contexts.
