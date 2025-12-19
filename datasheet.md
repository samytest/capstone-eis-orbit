# Datasheet for BBO Capstone Project Dataset

## Motivation
This dataset was created to support the Bayesian Black‑Box Optimisation (BBO) capstone project. It captures my query history and function evaluations across ten optimisation rounds under a limited query budget. The goal is to demonstrate transparent, reproducible decision‑making in black‑box optimisation and to provide peers with a clear record of my process.

## Composition
- **Contents:** Eight synthetic functions (2D–8D) with one query per round, yielding 80 queries total.
- **Format:** Each query is a vector of floating‑point values (six decimal places), stored in `.npy` files.
- **Size:** 80 input vectors with corresponding scalar outputs.
- **Gaps:** Sparse coverage in high‑dimensional functions (6D–8D); boundary regions under‑sampled.

## Collection Process
- **Generation:** Queries were selected using a mix of surrogate modelling (Gaussian Processes with UCB/EI), manual perturbations, and boundary exploration.
- **Strategy:** Early rounds emphasised exploration; later rounds shifted toward exploitation and refinement.
- **Time Frame:** Ten rounds over several weeks, with iterative updates based on observed outputs.

## Preprocessing and Uses
- **Transformations:** Inputs standardised to [0,1]; outputs negated where minimisation tasks were reframed as maximisation.
- **Intended Uses:** Benchmarking optimisation strategies, reproducibility studies, and peer comparison.
- **Inappropriate Uses:** Not suitable for training production ML models or inferring real‑world chemical/medical properties.

## Distribution and Maintenance
- **Availability:** Public GitHub repository (linked in README).
- **Terms of Use:** Open for educational and peer‑review purposes.
- **Maintenance:** Maintained by me (Suresh Selvapandian) for the duration of the capstone project.
