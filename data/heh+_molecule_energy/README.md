# Helium Hydride Ion (HeH⁺) Optimization Logs (`data/heh+_molecule_energy/`)

This folder contains the verification data for the heteronuclear **Helium Hydride molecular ion (HeH⁺)**, evaluating the algorithmic generalizability and physical symmetry conservation of the Weighted SSVQE framework.

## Computational Settings
* **Interatomic Distance ($R_{eq}$)**: 1.74 a.u.
* **Basis Set**: STO-6G (4-qubit representation).
* **Exact FCI Target Energy**: Ground state mapped at the second excited index ($k = 2$, $E_{2}$ = -2.894941 Ha).

### Columns Definition:
* **`trial`**: Run index over 30 independent trials using the Adam or COBYLA optimizer.
* **`w`**: Cost function weight parameter targeting the specific particle sector.
* **`delta_E`**: Absolute energy recovery accuracy (Δ E).
* **`fidelity`**: State fidelity metric (F) relative to the exact FCI wavefunction target.
* **`N_expect`**: The electron number expectation value (\(\langle N \rangle\)). Critical for checking if the circuit stays inside the unmixed physical 2-electron sector.

## Sample Data Structure:
```csv
trial,w,delta_E,fidelity,N_expect
1,0.5,0.000996,0.994016,2.005842
2,0.5,0.000372,0.976519,2.001176
3,0.5,0.003205,0.998497,2.026807
```
