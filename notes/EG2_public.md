# EG2 Public Note (Capture and Restart)

Canonical wording: `transport / local-to-global transfer`.

In-paper anchor: `paper/INVARIANT_SUBSPACE_PROBLEM_PREPRINT.md` (`ISP_G2`).

## Goal
Expand the compressed capture/restart language into the local-to-global transport gate for `proving persistence of nontrivial invariant subspaces for admissible bounded operators through an admissible spectral closure architecture`.

## Objects

- transport carrier: the admissible evolution, deformation, or routed lattice declared in the preprint.
- capture floor: `sigma_spectral`.
- restart law: the normalization/re-entry rule that keeps corrective steps inside the admissible class.
- carried losses: defect, restart, and normalization losses that must remain explicit.

## Closure Criterion

`ISP_G2` closes when `sigma_spectral` survives admissible losses and restart corrections: spectral defect stays above capture floor across admissible perturbation losses.
This is the transport contribution to `M_ISP`.

## Lemma Chain and Proof Payload

### Lemma EG2.1 (transport accounting)
Every transport step used by the lane is charged to the declared defect ledger instead of being absorbed into prose.

Payload: check that the capture constant `sigma_spectral` is present in the constants registry and extraction inputs.

### Lemma EG2.2 (restart preservation)
Restart or normalization preserves the declared admissible class and does not create an untracked remainder.

Payload: inspect the repro script and guard output for the gate tied to `sigma_spectral`.

### Theorem EG2.3 (capture gate closure)
If transport accounting and restart preservation hold, then `ISP_G2` carries local control forward without breaking admissibility.

## Current Instantiation

- gate: `ISP_G2`
- artifact key: `sigma_spectral`
- canonical equivalent: `transport / local-to-global transfer`
- audit surface: `repro/run_repro.sh` and `repro/certificate_runtime.json`
