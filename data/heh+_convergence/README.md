# Helium Hydride Ion (HeH⁺) Optimization Logs (`data/konvergensi heh+/`)

This folder contains the verification data for the heteronuclear **Helium Hydride molecular ion (HeH⁺)**, evaluating the algorithmic generalizability and physical symmetry conservation of the Weighted SSVQE framework across different optimization configurations.

## Computational Settings
* **Interatomic Distance ($R_{eq}$)**: 1.74 a.u.
* **Basis Set**: STO-6G (4-qubit representation).
* **Exact FCI Target Energy**: Ground state mapped at the second excited index ($k = 2$), $E_{2}$ = -2.894941 Ha).

## Data Structure & Optimization Protocol
The folder contains log files tracking the convergence trajectory across **4 different optimizer configurations**:
1. **Adam (Learning Rate = 0.01)**
2. **Adam (Learning Rate = 0.05)**
3. **Adam (Learning Rate = 0.10)**
4. **COBYLA**

### Protocol per Data File:
* **Fair Baseline**: For each unique file, an identical initial parameter set is distributed across all 4 optimizer configurations to guarantee a fair baseline comparison.
* **Step-by-Step Trajectory**: Unlike final state metrics, this folder records structural values at each individual step. The Adam optimizers run for exactly **500 iterations** (Indices `0` to `499`). 
* **Row Aggregation**: A single file accumulates the sequential convergence entries of all 4 optimizers, resulting in a total dataset size of **2,000 rows** per file.
* **Replication**: This routine is systematically evaluated across **30 independent runs (Trials)** using distinct initial states for configuration identifiers `ID-03` and `ID-6`.

### Columns Definition:
* **`Bobot`**: The active scalar weight parameter ($w$) assigned to the target excited state within the multi-state cost function ($w \in [0.0, 1.0]$).
* **`Trial`**: The explicit label identifying the current active optimizer configuration (e.g., `Adam_lr_0.01`, `Adam_lr_0.05`, `Adam_lr_0.10`, or `COBYLA`).
* **`Optimizer_Config`**: Structural metadata specifying the entry context type (e.g., `Iterasi`).
* **`Energi_Target (Hartree)`**: The instantaneous computed molecular energy value (in Hartree, Ha) recorded at that specific operational step.
* **`Total_Cost`**: The scalar value of the total Weighted SSVQE objective cost function evaluated at the given step.
* **`Fidelity`**: The current state fidelity calculation ($F$) measuring the exact overlap projection between the ansatz trial wavefunction and the target FCI state.
* **`Jumlah_Elektron`**: The expectation value of the electron number operator ($\langle N \rangle$), crucial for verifying if the trajectory remains within the proper physical 2-electron subspace.
* **`Delta_Cost (Error)`**: The active minimization error delta mapping the absolute structural distance from the target convergence criteria.

## Sample Data Structure:
```csv
Bobot,Trial,Optimizer_Config,Energi_Target (Hartree),Total_Cost,Fidelity,Jumlah_Elektron,Delta_Cost (Error)
0.80,Adam_lr_0.10,Iterasi,-2.4343349878334606,-6.486718687766266,0.15824118644112517,2.4604949060868755,1.0589755970699333
0.80,Adam_lr_0.11,Iterasi,-2.670929472463483,-7.250537726485101,0.1661797394572226,2.6412424999724746,0.763819038718835
0.80,Adam_lr_0.12,Iterasi,-2.8165148007603045,-7.703762517976737,0.147506008048517,2.797296285101603,0.4532247914916363
```
