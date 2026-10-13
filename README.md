# Datasets for: Ansatz-Dependent Role of Weighting Factors in Weighted SSVQE
[![Python](https://shields.io)](https://python.org)
[![Framework](https://shields.io)](https://pennylane.ai)
[![License](https://shields.io)](https://opensource.org)

This repository contains the numerical datasets and simulation logs supporting the manuscript:
> **Ansatz-Dependent Role of Weighting Factors in the Weighted Subspace-Search Variational Quantum Eigensolver**
> **Dewan J. T. R. Tamsih, A. Abdurrouf, Gagus K. Sunnardianto, and Yanoar P. Sarwono\**

---
## 📂 Data Directory Structure
- `data/entangling_capability/`: Raw Meyer–Wallach entanglement CSV files across ansatzes and layers.
- `data/expressibility/`: Raw Kullback–Leibler divergence CSV files.
- `data/h2_molecule_energy/`: Weighted SSVQE energy accuracy and iteration logs for Hydrogen molecule.
- `data/heh+_molecule_energy/`: Multi-metric evaluation logs (accuracy, iteration, fidelity, and electron number expectation values) for Helium Hydride Cation.
- `data/heh+_convergence/`: Optimizer trajectory logs comparing Adam (with various learning rates) and COBYLA.
