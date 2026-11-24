# lean/

Lean 4 / Mathlib formalization for Erdős #647.

**Empty for now.** No formalization has been attempted.

## Planned setup (later stage)

- A Lake project (`lakefile.toml`, `lean-toolchain`, `lake-manifest.json`), all committed. `.lake/` is git-ignored.
- Statements aligned with the community formal statement:
  [google-deepmind/formal-conjectures `ErdosProblems/647.lean`](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/647.lean).
- Every theorem's axioms are audited with `#print axioms`. Results depending on
  `sorry`, `native_decide` or custom axioms are labelled as such and never
  described as fully verified.
