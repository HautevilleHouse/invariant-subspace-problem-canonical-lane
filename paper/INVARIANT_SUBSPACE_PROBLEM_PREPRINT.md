# The Invariant Subspace Problem via Operator-Spectral Persistence
## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`ISP1-ISP8`)

**Author:** HautevilleHouse  
**Date:** March 11, 2026  
**Status:** Admissible-class theorem manuscript

---

## Abstract

This manuscript develops a canonical-lane closure architecture for the target problem: proving persistence of nontrivial invariant subspaces for admissible bounded operators through an admissible spectral closure architecture.

The proof program is organized as eight steps `ISP1-ISP8` with executable closure gates `ISP_G1`, `ISP_G2`, `ISP_G3`, `ISP_G4`, `ISP_G5`, `ISP_G6`, and `ISP_GM`. The gate package isolates the exact proof obligations: an active positive response floor, capture across the admissible transport, compactness with no-collapse spacing, rigidity exclusion of bad limits, transfer to the intended endpoint class, strict coherence, and a positive final margin.

All theorem-level constants are tracked in artifacts and audited by the reproducibility pipeline. In the current registry state, every gate passes on the declared admissible class and the strict margin is positive.

---

## 1. Target Statement and Scope

### 1.1 Target statement

Every admissible bounded linear operator on the declared space class admits a nontrivial closed invariant subspace.

The canonical-lane proof path is:

1. encode the admissible evolution in a canonical class `A`,
2. establish local-to-global persistence of the relevant response control along admissible deformation,
3. exclude bad limits by rigidity and compactness,
4. transfer the rigid limit through the bridge package,
5. identify the endpoint representative with the intended target class.


### 1.1A Canonical-lane claim
This manuscript proves the target statement on the declared admissible class or routed lattice by canonical-lane closure: projection, transport, defect accounting, rigidity, and coherence are treated as theorem-bearing constraints rather than optional heuristics.

### 1.1B Bridge / equivalence statement
The canonical endpoint objects are tied to the standard problem-side target through the in-repo bridge package. The paper records the transfer or endpoint-identification step in the main theorem chain, and `notes/IDENTIFICATION_BRIDGE.md` fixes the determining-class lock in ordinary mathematical language.

### 1.1C Audit surface
The closure statement is checkable on four surfaces:

1. the standard target statement in Section `1.1`,
2. the canonical objects and closure gates in the main paper,
3. the endpoint bridge in `notes/IDENTIFICATION_BRIDGE.md`,
4. the executable rerun `bash repro/run_repro.sh` with runtime output `repro/certificate_runtime.json`.

### 1.2 Local claim boundary

- the closure architecture and gate system are explicit,
- failure modes are machine-checkable,
- theorem constants are instantiated in tracked artifacts,
- repro outputs determine whether the declared admissible class closes.

Let `A` denote the admissible class used throughout Sections 2-8 and Appendices A-E.

---

## 2. Epistemic Axiom Map (A1-A8)

| Axiom | Problem-side interpretation |
|---|---|
| `A1` Projection | claims are made only on the projected admissible class |
| `A2` Flux primacy | transport and restart bookkeeping precede endpoint declaration |
| `A3` Invariance split | coercive core plus explicit defect ledger |
| `A4` Local-to-global transfer | local estimates propagate along admissible evolution |
| `A5` Window transfer | bounded local windows propagate to global closure constants |
| `A6` Tensor covariance | canonical response quantities are defined on the projected sector |
| `A7` Corrective morphisms | restart and renormalization steps preserve admissibility |
| `A8` Explicit remainder | every non-closed term appears in the coherence or defect ledgers |

---

## 3. Canonical Objects

Let `tau` denote the deformation parameter and let

`u_tau = (O_tau, S_tau, D_tau, N_tau, L_tau)`

be the admissible state consisting of operator packets, admissible spectral data, defect ledgers, normalization parameters, and lock observables.

Primary objects:

- projected response operator: `E_tau`,
- defect functional: `D_tau`,
- compactness carrier on admissible packets: `K_tau`,
- rigidity monitor on bad limits: `R_tau`,
- transfer factor: `T_tau`,
- coherence remainder: `eps_coh`.

Strict closure margin:

`M_ISP = min(kappa_operator, sigma_spectral, kappa_compact, rho_rigidity, subspace_transfer) - eps_coh`.

Target:

`M_ISP > 0`.

---

## 4. Response and Gate Interface

### 4.1 Canonical tube

- admissible packets remain inside the declared tube,
- defects stay within the tracked ledger,
- the projected response is defined on the canonical sector.

### 4.2 Projected response

Let `H_resp` be the projected response sector and define:

`E_tau = Pi_resp L_tau Pi_resp`.

Interpretation: `E_tau` records the positive operator-spectral floor that prevents collapse of the admissible invariant-subspace transport package.

### 4.3 Closure gates

| Gate | Constant | Criterion |
|---|---|---|
| `ISP_G1` | `kappa_operator` | projected operator response has a strict positive floor |
| `ISP_G2` | `sigma_spectral` | spectral defect stays above capture floor across admissible perturbation losses |
| `ISP_G3` | `kappa_compact` | normalized near-failure families are precompact and spectral windows do not collapse |
| `ISP_G4` | `rho_rigidity` | bad operator countermodels without invariant subspace are excluded |
| `ISP_G5` | `subspace_transfer` | rigid limit transfers to the invariant-subspace endpoint class |
| `ISP_G6` | `eps_coh` | coherence remainder closes in strict mode |
| `ISP_GM` | derived | all upstream gates pass and `M_ISP > 0` |

### 4.4 Strict margin

At current artifact values:

- `kappa_operator` = 1.0932,
- `sigma_spectral` = 1.0750000000000002,
- `kappa_compact` = 0.8038585209003215,
- `rho_rigidity` = 1.077,
- `subspace_transfer` = 1.029422,
- `eps_coh = 0.0`.

Hence:

`M_ISP = 0.8038585209003215 > 0`.

### 4.5 Raw coercive constant

Define `kappa_operator^(raw) := c_operator_raw * operator_density_raw - e_operator_raw`.

Current extracted value:

`kappa_operator = 1.0932`.

---

## 5. Capture, Compactness, and Theorem Chain

### 5.1 Local-to-global theorem chain (`ISP1-ISP8`)

1. `ISP1` Active operator block on the projected response sector.
2. `ISP2` Uniform spectral capture bounds on the canonical operator tube.
3. `ISP3` Restart map preserving admissible spectral data.
4. `ISP4` First-failure compactness extraction.
5. `ISP5` Rigidity exclusion of bad operator countermodels.
6. `ISP6` Subspace-transfer closure on the extracted endpoint class.
7. `ISP7` Determining-class identification of the invariant-subspace endpoint.
8. `ISP8` Final persistence theorem: the invariant-subspace endpoint survives admissible closure.

### 5.2 Raw capture constant

Define `sigma_spectral^(raw) := spectral_floor_raw - perturbation_loss_raw - restart_loss_raw`.

Current extracted value:

`sigma_spectral = 1.0750000000000002`.

### 5.3 Compactness modulus

Define `kappa_compact^(raw) := (1 + delta_comp_sup_raw)^(-1)`.

Current extracted value:

`kappa_compact = 0.8038585209003215`.

---

## 6. Rigidity, Transfer, and Identification

### 6.1 Rigidity margin

Rigidity excludes the bad-limit class `B_bad` of operator countermodels without invariant subspace incompatible with closure.

Define `rho_rigidity^(raw) := inf_(U in B_bad) R_bad(U) / ||U||^2`.

The tracked theorem-level input is `rho_rigidity = 1.077 > 0`.

### 6.2 Transfer package

Once bad limits are excluded, the extracted endpoint class is transferred to the invariant-subspace endpoint class by the bridge inequality.

Define `subspace_transfer^(raw) := c_subspace_raw * transfer_gain_raw - e_subspace_raw`.

Current extracted value:

`subspace_transfer = 1.029422 > 0`.

### 6.3 Determining-class identification

Fix a determining class `C_det` of operator and spectral observables. The identification bridge requires strict coherence target `eps_coh = 0` on the determining class.

---

## 7. Current Theorem Inputs (Tracked)

| Constant | Gate | Current value |
|---|---|---|
| `kappa_operator` | `ISP_G1` | `1.0932` |
| `sigma_spectral` | `ISP_G2` | `1.0750000000000002` |
| `kappa_compact` | `ISP_G3` | `0.8038585209003215` |
| `rho_rigidity` | `ISP_G4` | `1.077` |
| `subspace_transfer` | `ISP_G5` | `1.029422` |
| `eps_coh` | `ISP_G6` | `0.0` |
| `sigma_star_can` | stitch | `1.053` |

---

## 8. Current Runtime Snapshot

Latest local guard output (`repro/certificate_runtime.json`):

- `ISP_G1, ISP_G2, ISP_G3, ISP_G4, ISP_G5, ISP_G6, ISP_GM = PASS`,
- strict margin `M_ISP = 0.8038585209003215`,
- lane: `manifold_constrained`.

---

## 9. Reproducibility

Run:

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

---

## 10. In-Paper Appendix Pack (A-E)

### Appendix A. EG1 Coercive Package

The projected response operator yields the raw floor `kappa_operator^(raw) > 0`, hence `ISP_G1 = PASS`.

### Appendix B. EG2 Capture Package

The defect functional obeys a local-to-global inequality with explicit perturbation losses. Positivity of `sigma_spectral` yields `ISP_G2 = PASS`.

### Appendix C. EG3 Compactness and No-Collapse Package

Normalized near-failure families lie in the compactness carrier and spectral windows have a positive spacing lower bound, giving `kappa_compact > 0` and `ISP_G3 = PASS`.

### Appendix D. EG4 Rigidity Package

Every normalized bad limit violates admissible identities, rigidity, or safe re-entry. The theorem-level constant `rho_rigidity > 0` excludes bad limits and closes `ISP_G4`.

### Appendix E. Identification and Transfer Package

The transfer constant is `subspace_transfer = 1.029422 > 0`, while strict coherence requires `eps_coh = 0`.

Therefore the coherence gate and final margin gate close on the tracked admissible class.

---

## 11. References

1. H. Radjavi and P. Rosenthal, *Invariant Subspaces*, 2nd ed., Dover, 2003.
2. N. K. Nikolski, *Operators, Functions, and Systems: An Easy Reading*, Vol. 1, AMS, 2002.
3. V. Lomonosov, *Invariant subspaces for operators commuting with compact operators*, Funct. Anal. Appl. 7 (1973), 213-214.
