# EG3 Public Note (Compactness and No-Zeno Control)

Canonical wording: `first-failure compactness / no-collapse`.

In-paper anchor: `paper/INVARIANT_SUBSPACE_PROBLEM_PREPRINT.md` (`ISP_G3`).

## Goal
Make the compactness/no-Zeno gate explicit for `proving persistence of nontrivial invariant subspaces for admissible bounded operators through an admissible spectral closure architecture`: near-failure behavior must be captured, not allowed to drift or accumulate invisibly.

## Objects

- near-failure class: normalized candidate failures inside the declared admissible class.
- compactness modulus: `kappa_compact`.
- no-collapse condition: restart spacing and compactness prevent Zeno-style accumulation of corrective steps.
- remainder channel: any residual failure data remains visible to the coherence gate.

## Closure Criterion

`ISP_G3` closes when `kappa_compact` provides compactness/no-collapse control: normalized near-failure families are precompact and spectral windows do not collapse.
This is the first-failure capture contribution to `M_ISP`.

## Lemma Chain and Proof Payload

### Lemma EG3.1 (near-failure extraction)
Any sequence that approaches gate failure has a normalized extracted candidate inside the declared admissible class.

Payload: check that `kappa_compact` is registered and participates in the runtime certificate.

### Lemma EG3.2 (no-Zeno spacing)
Corrective restart steps cannot accumulate without being detected by the compactness or coherence surface.

Payload: check that the guard treats compactness as a gate input, not as narrative decoration.

### Theorem EG3.3 (compactness gate closure)
If near-failure extraction and no-Zeno spacing hold, then `ISP_G3` prevents hidden drift before rigidity is applied.

## Current Instantiation

- gate: `ISP_G3`
- artifact key: `kappa_compact`
- canonical equivalent: `first-failure compactness / no-collapse`
- audit surface: `artifacts/constants_registry.json` and `repro/certificate_runtime.json`
