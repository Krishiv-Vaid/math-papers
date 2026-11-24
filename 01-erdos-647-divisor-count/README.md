# Erdős Problem #647: A Divisor-Count Inequality

**Status: open** (checked 2026-11-24) · **Active project** · **Prize:** £25 offered by Erdős (1992) for an example

| | |
|---|---|
| Source | [erdosproblems.com/647](https://www.erdosproblems.com/647) |
| Proposers | P. Erdős and J. L. Selfridge |
| Area | Elementary / analytic number theory (divisor function) |
| Erdős sources | [Er79] Math. Mag. **52** (1979) 67–70; [Er79d] Acta Math. Acad. Sci. Hungar. (1979) 71–80; [Er80, p. 107]; [Er92e] Eureka (1992) 44–48; [Er95c] Octogon Math. Mag. (1995) 3–5 |
| Formal statement | [formal-conjectures/ErdosProblems/647.lean](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/647.lean) |
| OEIS | [A062249](https://oeis.org/A062249) ($m+\tau(m)$), [A087280](https://oeis.org/A087280) (solutions of equality), [A400986](https://oeis.org/A400986) ($\Delta(n)$) |

## The problem

Let $\tau(m)$ be the number of positive divisors of $m$. **Is there an integer $n>24$ such that**

$$\max_{1\le m<n}\bigl(m+\tau(m)\bigr)\le n+2 \;?$$

Equivalently: is there $n>24$ with $\tau(n-k)\le k+2$ for every $1\le k\le n-1$?

The inequality holds for $n=24$, and $n+2$ cannot be replaced by $n+1$ for $n\ge 7$. Erdős thought infinitely many such $n$ "extremely doubtful".

## Contents

| Path | Contents |
|---|---|
| [`paper/main.tex`](paper/main.tex) | Background and problem-definition paper (LaTeX). **No new results.** |
| [`paper/references.bib`](paper/references.bib) | Bibliography, with verification notes |
| [`research/problem-background.md`](research/problem-background.md) | Statement, history, prize, status |
| [`research/literature-review.md`](research/literature-review.md) | Classical results on $\tau$, and recent (mostly unrefereed) work on #647 |
| [`proof/`](proof/) | Human-readable arguments (none yet) |
| [`lean/`](lean/) | Lean 4 / Mathlib formalization (none yet) |
| [`experiments/`](experiments/) | Computational experiments (none yet) |

## Building the paper

```sh
cd paper
latexmk -pdf -outdir=build main.tex      # output: paper/build/main.pdf (git-ignored)
```

To commit a final PDF, copy it to `paper/main.pdf`. PDFs outside `build/` are not ignored.

## Current state

- [x] Problem statement, history, prize and literature documented
- [ ] Independent verification of the reported structural reductions
- [ ] Original investigation (next stage)

> **Caveat.** All computations listed in the literature review are *finite-range* exclusions reported by others and are unrefereed. They do not show that no solution exists.
