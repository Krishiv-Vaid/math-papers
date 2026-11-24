# math-papers

**Independent investigations into open problems in mathematics**

Krishiv Vaid · Mathematics, University of Waterloo

---

## About

This repository documents independent research on open mathematical problems and conjectures, mostly in number theory and combinatorics. Every project is set up to support the full research workflow:

- **Mathematical theory:** precise statements, definitions, literature reviews and (eventually) original arguments.
- **AI-assisted research:** Claude Code and similar tools are used for literature search, exploration, drafting and proof-checking assistance. They do not replace human understanding or verification.
- **Computational experimentation:** exact-arithmetic experiments to test hypotheses and find patterns.
- **Formal verification:** Lean 4 and Mathlib, where formalization is feasible and worthwhile.
- **Original contributions:** new lemmas, partial results, improved bounds, counterexamples or complete resolutions, written up as papers that can be reviewed independently.

## Research philosophy

The goal is to work on questions that are actually unresolved and, where possible, to produce new results, not just to reproduce known mathematics.

Two rules apply throughout:

1. **Every mathematical claim must be backed by a rigorous argument or a precise reference.**
2. **Computational evidence is never presented as a proof of a general statement.** A finite search can establish a finite statement, such as "no solution exists in a given range", or it can exhibit an example. It cannot establish non-existence over an infinite search space.

### On AI-assisted mathematics

AI systems now contribute to research mathematics in real ways. They have also produced many convincing-looking but wrong "proofs". This repository keeps the following categories separate and never merges them:

| Category | Meaning |
|---|---|
| Claimed | Someone, human or AI, has announced a result. Nothing more is implied. |
| Partial advance | A verified result that makes progress without resolving the problem. |
| Independently verified | Checked by qualified people other than the authors, or machine-checked against a reviewed formal statement. |
| Accepted resolution | Published after peer review and/or recognized by the relevant authority (e.g. a problem curator or prize committee). |

For example, this repository makes **no** claim about the status of the Riemann Hypothesis or the Navier–Stokes existence and smoothness problem. The Clay Mathematics Institute ([claymath.org](https://www.claymath.org/millennium-problems/)) is the authority on whether a Millennium Prize Problem has been solved, and a press report or an AI transcript is not.

The curator of [erdosproblems.com](https://www.erdosproblems.com) has written about the effect of AI-generated proof claims on that site ([*Changes*, T. F. Bloom, 6 October 2026](https://www.erdosproblems.com/forum/thread/blog:9)). In line with that post, any write-up produced here will be written and understood by a human, will state its sources, and will say exactly how AI was used.

## Research projects

| # | Problem | Name | Area | Source | Status (checked 2026-11-24) |
|---|---|---|---|---|---|
| 1 | [Erdős #647](01-erdos-647-divisor-count/) | Divisor-count inequality: is there $n>24$ with $\max_{m<n}(m+\tau(m))\le n+2$? | Elementary / analytic number theory | [erdosproblems.com/647](https://www.erdosproblems.com/647) | **Open.** No $n>24$ known. Unrefereed searches report none up to $10^{22}$. **Active project.** |
| 2 | [Erdős #307](02-erdos-307-prime-reciprocals/) | Prime reciprocal sums: finite sets of primes $P,Q$ with $\left(\sum_{p\in P}1/p\right)\left(\sum_{q\in Q}1/q\right)=1$? | Number theory, unit fractions | [erdosproblems.com/307](https://www.erdosproblems.com/307) | **Open.** No example known. |
| 3 | [Erdős #850](03-erdos-850-erdos-woods/) | Erdős–Woods conjecture: distinct $x,y$ with $x+i, y+i$ having the same prime factors for $i=0,1,2$? | Number theory, primes | [erdosproblems.com/850](https://www.erdosproblems.com/850) | **Open.** A "no" answer would follow from an explicit form of the *abc* conjecture. |
| 4 | [Erdős #7](04-erdos-007-odd-covering-systems/) | Odd covering problem: is there a distinct covering system with all moduli odd? | Number theory, covering systems | [erdosproblems.com/7](https://www.erdosproblems.com/7) | **Open.** The squarefree case is impossible (Balister–Bollobás–Morris–Sahasrabudhe–Tiba, 2022). |

**How status was checked.** On 6 October 2026, erdosproblems.com stopped displaying problem statuses. Statuses above come from the community database [teorth/erdosproblems](https://github.com/teorth/erdosproblems), which lists all four problems as *verifiable*: open, but if the answer is "yes", a single finite example would prove it. Each status was then cross-checked against the remarks on the problem page and recent literature. The site warns that its records may be out of date, so statuses must be re-checked before any claim of novelty. Details and caveats are in each project's README.

## Repository layout

```
math-papers/
├── README.md                    ← this file
├── LICENSE                      ← MIT (code) + CC BY 4.0 (papers and documentation)
├── .gitignore
├── 01-erdos-647-divisor-count/  ← active project
│   ├── README.md
│   ├── paper/                   ← LaTeX paper (main.tex, references.bib)
│   ├── research/                ← problem background, literature review
│   ├── proof/                   ← human-readable mathematical arguments (empty for now)
│   ├── lean/                    ← Lean 4 / Mathlib formalization (empty for now)
│   └── experiments/             ← computational experiments (empty for now)
├── 02-erdos-307-prime-reciprocals/
│   ├── README.md
│   ├── research/problem-background.md
│   └── paper/
├── 03-erdos-850-erdos-woods/
│   ├── README.md
│   ├── research/problem-background.md
│   └── paper/
├── 04-erdos-007-odd-covering-systems/
│   ├── README.md
│   ├── research/problem-background.md
│   └── paper/
└── templates/
    ├── research-paper-template.tex
    ├── references-template.bib
    └── problem-template.md
```

To start a new project, copy `templates/problem-template.md` into a new `NN-short-name/README.md` and `templates/research-paper-template.tex` into `NN-short-name/paper/main.tex`.

## Research tools

- **[Claude Code](https://claude.com/claude-code):** AI-assisted literature search, exploration, drafting and code.
- **Python:** exact integer arithmetic (`int`, `fractions.Fraction`), `sympy`, `gmpy2`.
- **[SageMath](https://www.sagemath.org/):** number-theoretic computation, where appropriate.
- **[Lean 4](https://lean-lang.org/) and [Mathlib](https://leanprover-community.github.io/):** formal verification. Formal statements of all four problems already exist in [google-deepmind/formal-conjectures](https://github.com/google-deepmind/formal-conjectures/tree/main/FormalConjectures/ErdosProblems).
- **LaTeX:** papers (`amsart`, BibTeX). Build with `latexmk -pdf -outdir=build main.tex`.
- **Git and GitHub:** version control and history.

## Standards

Every document in this repository must label each claim as one of the following:

1. **Established result:** a classical theorem, with a textbook or primary reference.
2. **Previously published result:** with a full citation to the peer-reviewed source.
3. **Reported but unrefereed:** preprints, forum posts and repositories, marked as such and not relied on without checking.
4. **New conjecture:** stated as a conjecture and never phrased as a fact.
5. **Computational observation:** with the exact range, method and code needed to reproduce it, and never generalized beyond what was computed.
6. **Original proven result:** with a complete proof in `proof/` or `paper/`.
7. **Formalized and independently verified:** with a Lean proof (no `sorry`, no unexplained axioms), the exact formal statement used, and a record of independent review.

A conjecture is **not** considered solved because an AI model produced a convincing-looking argument. Anything that is uncertain is marked **unverified**.

## Citing the problems

Following the request of erdosproblems.com, cite the original sources of Erdős for each problem, and acknowledge the website as

> T. F. Bloom, *Erdős Problem #N*, https://www.erdosproblems.com/N, accessed YYYY-MM-DD.

## License

Code is released under the MIT License. Papers and documentation are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE).
