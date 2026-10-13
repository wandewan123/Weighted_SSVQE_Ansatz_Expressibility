# Datasets for: Ansatz-Dependent Role of Weighting Factors in Weighted SSVQE
<a href="https://python.org"><img src="https://shields.io" alt="Python"></a>
<a href="https://pennylane.ai"><img src="https://shields.io" alt="Framework"></a>
<a href="https://opensource.org"><img src="https://shields.io" alt="License"></a>

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
