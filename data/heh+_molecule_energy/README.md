# Helium Hydride Ion (HeH⁺) Optimization Logs (`data/heh+_molecule_energy/`)

This folder contains the verification data for the heteronuclear **Helium Hydride molecular ion (HeH⁺)**, evaluating the algorithmic generalizability and physical symmetry conservation of the Weighted SSVQE framework.

## Computational Settings
* **Interatomic Distance ($R_{eq}$)**: 1.74 a.u.
* **Basis Set**: STO-6G (4-qubit representation).
* **Exact FCI Target Energy**: Ground state mapped at the second excited index ($k = 2$, $E_{2}$ = -2.894941 Ha).

### Columns Definition:
* **`TRIAL`**: The index of the independent stochastic optimization run (0, 1, 2, ...).
* **`BOBOT`**: The active scalar weight parameter ($w$) assigned to the target excited state within the multi-state cost function ($w \in [0.0, 1.0]$).
* **`ENERGY AKHIR`**: The final computed molecular energy value (in Hartree, Ha) extracted immediately after the quantum circuit optimization reaches convergence.
* **`COST AKHIR`**: The minimized scalar value of the total Weighted SSVQE objective cost function evaluated at the point of convergence.
* **`TOTAL ITERASI`**: The exact number of minimization steps required by the hybrid classical optimizer to satisfy the absolute convergence tolerance criteria.
* **`FIDELITY AKHIR`**: The final state fidelity calculation ($F$) measuring the overlap projection between the optimized ansatz trial wavefunction and the exact FCI state target.
* **`ELEKTRON AKHIR`**: The expected electron number operator value ($\langle N \rangle$). This metric is critical to verify if the optimization preserves the physical 2-electron physical sector.
* **`BASIS STATE DOMINAN`**: The primary computational basis state configuration (e.g., $\vert{}1110\rangle$) and its corresponding percentage contribution inside the final converged wave vector.

## Sample Data Structure:
```csv
TRIAL,BOBOT,ENERGY AKHIR,COST AKHIR,TOTAL ITERASI,FIDELITY AKHIR,ELEKTRON AKHIR,BASIS STATE DOMINAN
0,0.01,-3.161776518492281,-6.0805442960963125,123,7.477104404036458e-07,2.9999990087511303,|1110> (100.00%)
1,0.01,-3.1617761918143716,-6.080544398710159,133,5.593060634133427e-07,2.9999998001850616,|1110> (100.00%)
2,0.01,-3.161776448566788,-6.080544358372789,137,5.529508228803274e-07,2.9999996342849307,|1110> (100.00%)
```
