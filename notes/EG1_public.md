# EG1 Public Note (Projected Response Floor)

Canonical wording: `projection / protected core`.

In-paper anchor: `paper/INVARIANT_SUBSPACE_PROBLEM_PREPRINT.md` (`ISP_G1`).

## Goal
Make the projected response floor explicit as the protected-core gate for `proving persistence of nontrivial invariant subspaces for admissible bounded operators through an admissible spectral closure architecture`.

## Objects

- admissible class: the declared class `A` or routed admissible lattice in the main preprint.
- canonical/base object package: Let `A` denote the admissible class used throughout Sections 2-8 and Appendices A-E.
- projected core: the response sector controlled by `kappa_operator`.
- carried remainder interface: downstream defect and coherence terms remain outside the protected core rather than being hidden in it.

## Closure Criterion

`ISP_G1` closes when `kappa_operator` satisfies the response-floor requirement: projected operator response has a strict positive floor.
This is the protected-core contribution to the strict margin `M_ISP`.

## Lemma Chain and Proof Payload

### Lemma EG1.1 (projection reduction)
On the declared admissible class, the response object may be read on the projected sector without changing the target gate.

Payload: check that all quantities used by `kappa_operator` are defined on the projected sector named in the main preprint.

### Lemma EG1.2 (protected-core floor)
If the projected response floor is positive on the admissible sector, then the core cannot collapse before the later transport and remainder gates are evaluated.

Payload: check the artifact key `kappa_operator` and the corresponding extraction input/provenance record.

### Theorem EG1.3 (core gate closure)
If Lemmas EG1.1-EG1.2 hold and the runtime artifact accepts `kappa_operator`, then `ISP_G1` supplies the projected/protected-core input to `M_ISP`.

## Current Instantiation

- gate: `ISP_G1`
- artifact key: `kappa_operator`
- canonical equivalent: `projection / protected core`
- audit surface: `artifacts/constants_registry.json`, `artifacts/constants_extracted.json`, and `repro/certificate_runtime.json`
