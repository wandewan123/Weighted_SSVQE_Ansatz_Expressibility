# Hydrogen Molecule (H₂) Optimization Logs (`data/h2_molecule_energy/`)

This directory houses the numerical logs targeting the three lowest energy eigenstates ($E_{0}$, $E_{1}$, $E_{2}$) of the neutral **Hydrogen molecule ($\text{H}_{2}$)** using the single-state Weighted SSVQE algorithm.

## Computational Settings
* **Interatomic Distance ($R_{eq}$)**: 1.40 a.u. (Equilibrium geometry)
* **Basis Set**: STO-6G mapped onto a 4-qubit system via Jordan–Wigner transformation.
* **Target Energy Benchmarks (FCI)**: $E_{0}$ = -1.145929 Ha, $E_{1}$ = -0.542788 Ha, $E_{2}$ = -0.542788 Ha.

### Columns Definition:
* **`trial`**: Stochastic trial index (1 to 30) initialized uniformly from $[0, 2\pi]$.
* **`w`**: The active weight parameter in the cost function ($w \in [0.0, 1.0]$).
* **`delta_E`**: The absolute energy accuracy error ($\Delta E = \vert{}E_{VQE} - E_{FCI}\vert{}$). The chemical accuracy threshold is $1.6 × 10^{-3}$ Ha.
* **`iterations`**: The number of minimization steps required to satisfy the convergence tolerance criterion.

## Sample Data Structure:
```csv
trial,w,delta_E,iterations
1,0.2,4.521e-05,115
2,0.2,3.134e-05,108
3,0.2,5.393e-05,124
```
