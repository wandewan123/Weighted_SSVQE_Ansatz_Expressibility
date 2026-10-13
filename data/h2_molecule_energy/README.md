# Hydrogen Molecule (H₂) Optimization Logs (`data/h2_molecule_energy/`)

This directory houses the numerical logs targeting the three lowest energy eigenstates ($E_{0}$, $E_{1}$, $E_{2}$) of the neutral **Hydrogen molecule ($\text{H}_{2}$)** using the single-state Weighted SSVQE algorithm.

## Computational Settings
* **Interatomic Distance ($R_{eq}$)**: 1.40 a.u. (Equilibrium geometry)
* **Basis Set**: STO-6G mapped onto a 4-qubit system via Jordan–Wigner transformation.
* **Target Energy Benchmarks (FCI)**: $E_{0}$ = -1.145929 Ha, $E_{1}$ = -0.542788 Ha, $E_{2}$ = -0.542788 Ha.

### Columns Definition:
* **`trial`**: Stochastic trial index (1 to 30) initialized uniformly from $[0, 2\pi]$.
* **`L`**: The parameterized quantum circuit (PQC) depth / number of repeated layers ($L \in \{1, 2, 3, 4, 5\}$  ).
* **`energy`**: The computed molecular energy value (in Hartree, Ha) achieved after the sirkuit optimization successfully reaches convergence.
* **`cost`**: The final scalar value of the Weighted SSVQE cost function evaluated at the point of convergence.
* **`iter`**: The number of minimization steps required to satisfy the convergence tolerance criterion.
* **`w`**: The active weight parameter in the cost function ($w \in [0.0, 1.0]$).

## Sample Data Structure:
```csv
Trial,L,energy,cost,iter,w
0,1,-1.1240243804902923,-0.011240243804902923,63,0.01
1,1,-1.1249792357860553,-0.011249792357860553,85,0.01
2,1,-1.1249020082753591,-0.011249020082753592,91,0.01
```
