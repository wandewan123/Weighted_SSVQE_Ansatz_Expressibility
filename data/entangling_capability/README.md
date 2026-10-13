# Entangling Capability Datasets (`data/entangling_capability/`)

This directory contains the numerical simulation data for the **Meyer–Wallach entanglement measure (\(\langle Q \rangle\))** used to define the accessible solution space inside the Hilbert space.

## Data Schema & Content
The files map the capacity of the circuit architectures to generate highly entangled many-body states, which is critical to capturing non-trivial correlations for excited-state chemical predictions.

### Columns Definition:
* **`trial`**: The independent stochastic calculation run index (1 to 30).
* **`L`**: The specific ansatz circuit layer configuration (L = 1, 2, 3, 4, 5).
* **`KL`**: The computed Meyer–Wallach entanglement value (the right label is **`Q`**), bounded in the interval \([0.0, 1.0]\). A value of `0.0` represents completely separable product states (e.g., Ansatz ID-01).

## Sample Data Structure:
```csv
trial,L,Q
1,1,0.171688
2,1,0.170445
3,1,0.172843
```
