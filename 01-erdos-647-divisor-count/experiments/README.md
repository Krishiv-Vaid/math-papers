# experiments/

Computational experiments for Erdős #647.

**Empty for now.** No computations have been run.

## Conventions for future content

- Exact integer arithmetic only, with no floating point in any decision step.
- Each experiment lives in its own directory with:
  - the code,
  - a `README.md` giving the exact range, parameters, hardware, run time and software versions,
  - small curated result files. Bulky raw output goes in `output/`, which is git-ignored.
- Results are **computational observations**. A search over a finite range is
  never described as evidence of non-existence in general.
- Where possible, produce *certificates* (e.g. factorizations) that can be
  checked independently of the search code.
