# Expressibility Datasets (`data/expressibility/`)

This directory contains the raw simulation logs for the **Kullback-Leibler divergence ($D_{KL}$)** evaluations, supporting the structural characterization of the parameterized quantum circuits (PQCs).

## Data Schema & Content
Each `.csv` file contains 5,000 statistical fidelity samples collected over 30 independent stochastic optimization trials for four distinct architectures (ID-01, ID-03, ID-06, ID-14) across scaling layers (L = 1 to 5).

### Columns Definition:
* **`trial`**: The index of the independent computational run (1 to 30) to ensure statistical robustness.
* **`L`**: The parameterized quantum circuit depth / number of repeated layers ($L \in \{1, 2, 3, 4, 5\}$).
* **`KL`**: The calculated Kullback-Leibler divergence value ($D_{KL}$). Lower values signify higher expressibility approaching a unitary 2-design.

## Sample Data Structure:
```csv
trial,L,KL
1,1,2.1538326677728038e-17
2,1,1.4521717162097048e-17
3,1,9.0594198809412700e-17
```
