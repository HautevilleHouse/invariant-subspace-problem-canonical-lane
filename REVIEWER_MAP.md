# Reviewer Map

    ## Claim Scope

    - Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
    - Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.

    ## Theorem Dependency Chain

    1. `EG1`: coercive response and active control floor.
    2. `EG2`: capture and admissible continuation.
    3. `EG3`: compactness and no-collapse spacing.
    4. `EG4`: rigidity and transfer.
    5. Identification bridge: strict coherence on the determining class.
    6. Scalar closure: `ISP_G1, ISP_G2, ISP_G3, ISP_G4, ISP_G5, ISP_G6, ISP_GM` all `PASS`.

    Primary files:

    - `paper/INVARIANT_SUBSPACE_PROBLEM_PREPRINT.md`
    - `notes/EG1_public.md`
    - `notes/EG2_public.md`
    - `notes/EG3_public.md`
    - `notes/EG4_public.md`
    - `notes/IDENTIFICATION_BRIDGE.md`

    ## Closure Gates

    | Gate | Constant | Description |
    |------|----------|-------------|
    | `ISP_G1` | `kappa_operator` | projected operator response has a strict positive floor |
| `ISP_G2` | `sigma_spectral` | spectral defect stays above capture floor across admissible perturbation losses |
| `ISP_G3` | `kappa_compact` | normalized near-failure families are precompact and spectral windows do not collapse |
| `ISP_G4` | `rho_rigidity` | bad operator countermodels without invariant subspace are excluded |
| `ISP_G5` | `subspace_transfer` | rigid limit transfers to the invariant-subspace endpoint class |
| `ISP_G6` | `eps_coh` | strict coherence / identification closure |
| `ISP_GM` | derived | final strict margin |

    ## Falsification Conditions

    - `repro/certificate_runtime.json` has any non-`PASS` gate.
    - `lane.active_lane != "manifold_constrained"`.
    - `all_pass != true`.
    - Any manifest hash mismatch under `repro/repro_manifest.json`.
    - A certified counterexample to any EG theorem statement used in the paper.
