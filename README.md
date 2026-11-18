# Data for "Solution of the Qubit Marginal Problem from Fermionic Representability"

D. A. Mazziotti

Ground-state energies of periodic rings of *n* = 12 qubits.

## Files

### `data_heisenberg_J1J2_N12.csv`

Frustrated Heisenberg ring:

$$
H = J_1 \sum_i \mathbf{S}_i \cdot \mathbf{S}_{i+1} + J_2 \sum_i \mathbf{S}_i \cdot \mathbf{S}_{i+2},
\qquad \mathbf{S}_i = \boldsymbol{\sigma}_i / 2, \qquad J_1 = 1 .
$$

First column: $J_2/J_1$ from 0.00 to 1.00 in steps of 0.05.

### `data_TFIM_N12.csv`

Transverse-field Ising ring:

$$
H = -J \sum_i Z_i Z_{i+1} - g \sum_i X_i, \qquad J = 1 .
$$

First column: $g/J$ from 0.0 to 2.0 in steps of 0.1.

## Columns

| Column | Description |
|---|---|
| `E_exact` | Exact diagonalization |
| `E_22POS` | (2,2)-positivity conditions |
| `E_partial23POS` | Partial (2,3)-positivity conditions: (2,2) plus T1/T2-type anticommutator conditions |
| `E_23POS` | Full (2,3)-positivity conditions |

## Notes

All 2-RDM energies are lower bounds obtained from semidefinite programs solved with the
boundary-point algorithm. At the exact points ($J_2/J_1 = 1/2$ and $g = 0$) they agree with
the exact energy to within the convergence tolerance of the solver.
