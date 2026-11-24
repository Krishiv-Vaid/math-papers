# Erdős #647: Literature Review

*Compiled 2026-11-24. This review separates **(A)** established results on the divisor function in general from **(B)** material specific to Problem #647. Everything in (B.3)–(B.5) is **unrefereed** and **not independently verified** by this project.*

---

## A. Established results on $\tau(n)$ (refereed / textbook)

| Result | Statement | Reference |
|---|---|---|
| Product formula | $\tau(p_1^{a_1}\cdots p_r^{a_r})=\prod(a_i+1)$, so $\tau$ is multiplicative | Hardy–Wright, Ch. 16 |
| Elementary bound | $\tau(n)\le 2\sqrt n$ | divisor pairing $d\leftrightarrow n/d$ |
| Subpolynomial growth | $\tau(n)=O_\varepsilon(n^\varepsilon)$ for every $\varepsilon>0$ | Hardy–Wright, Ch. 18 |
| Maximal order (Wigert) | $\limsup \dfrac{\log\tau(n)\log\log n}{\log n}=\log 2$ | Hardy–Wright, Ch. 18 |
| Explicit maximal bound | $\log\tau(n)\le 1.5379\log 2\,\dfrac{\log n}{\log\log n}$ for $n\ge 3$ | J.-L. Nicolas, G. Robin, *Canad. Math. Bull.* **26** (1983) 485–492 |
| Average order (Dirichlet) | $\sum_{n\le x}\tau(n)=x\log x+(2\gamma-1)x+O(\sqrt x)$ | Hardy–Wright, Ch. 18; Apostol, Ch. 3 |
| Normal order | $\omega(n),\Omega(n)$ have normal order $\log\log n$, so $\tau(n)=(\log n)^{\log 2+o(1)}$ for almost all $n$ | Hardy–Ramanujan, *Quart. J. Math.* **48** (1917) 76–92 |
| Hypothesis H | Conjecture: irreducible polynomials with no fixed prime divisor are simultaneously prime infinitely often | A. Schinzel, W. Sierpiński, *Acta Arith.* **4** (1958) 185–208 |

**Relevance.** These results show that $\tau(n-k)>k+2$ can only happen for $k$ small relative to $n$. The difficulty is that every small shift must satisfy $\tau(n-k)\le k+2$ *at the same time*, which is a prime-constellation-type condition. None of the results above decides #647.

---

## B. Material specific to Problem #647

### B.1 Erdős's remarks (primary, as reported on erdosproblems.com)
- Infinitely many solutions are "extremely doubtful". Conjecturally $\Delta(n)\to\infty$ [Er79].
- For each fixed $k$, the windowed version (only $n-k<m<n$) should hold infinitely often. This follows from Hypothesis H but is "hopeless with our present methods" [Er79d].

### B.2 Refereed partial results
- **None found** in this preliminary review. **To do:** a systematic MathSciNet / zbMATH search for citations of [Er79] and [Er79d], and of Guy §B8.

### B.3 Computational exclusions (finite ranges only; unrefereed)

| Reported by | Range with no solution | Method / trust base | Link |
|---|---|---|---|
| OEIS A087280 (long-standing comment) | $n<10^{10}$ | not specified | [A087280](https://oeis.org/A087280) |
| P. Idén (Jun 2026) | $24<n\le 10^{12}$ | segmented sieve, C code | [Zenodo](https://doi.org/10.5281/zenodo.21134668) |
| S. Hughes (Jun 2026) | $n\le\approx 6.16\times10^{17}$ | search over a reported 41-class modular reduction; Python checker | [GitHub](https://github.com/scottdhughes/erdos647-proof-chain) |
| Hughes and another contributor (as cited) | $n\lesssim 9.17\times10^{18}$ | modular reduction; Lean part uses `native_decide` | cited in arXiv:2608.17880 |
| D. Veljjanoski (Sep 2026) | $24<n\le10^{22}$ | GPU sieve; author calls it *uncertified* | [GitHub](https://github.com/veljjanoski/erdos647) |
| I. Mian, S. Siddique (Aug 2026) | $24<n\le10^{9}$ | **Lean 4 kernel-checked**, standard axioms only | [arXiv:2608.17880](https://arxiv.org/abs/2608.17880) |
| Forum contributor (Oct 2026) | $24<n\le10^{13}$ | Lean 4 kernel-checked sparse sieve certificate | [forum thread](https://www.erdosproblems.com/forum/thread/647) |

> A finite search cannot prove non-existence. These results only say where a solution cannot be.

### B.4 Reported structural reductions (unrefereed)
From the [forum thread](https://www.erdosproblems.com/forum/thread/647) (Jan–Oct 2026). To be independently verified:

1. Any solution $n>84$ satisfies $2520\mid n$ (S. Dutta). B. Alexeev pointed out a gap in a follow-up coprimality step, which was partly repaired.
2. $n=2520N$ with $N$ in one of 41 residue classes mod $46189=11\cdot13\cdot17\cdot19$. Reported as Lean-verified (S. Hughes).
3. "Prime-chain" families: small shifts force several linear forms in $n$ to be prime simultaneously, which gives two prime 7-tuple families (S. Hughes, K. Kitamura).
4. Density bounds via Brun's sieve: $\#\{n\le x\}\ll x/(\log x)^7$, later $x\exp(-(\log\log x)^{2-o(1)})$ (S. Hughes). These are **density-zero, not non-existence** results.
5. Observation: infinitely many solutions of this shape would give infinitely many Sophie Germain primes.
6. Heuristic: no finite table of such sieve stages can prove non-existence, because the divisor budget never excludes $n\equiv0\pmod L$.

### B.5 Withdrawn or refuted claims
- **Jan 2026:** a claimed proof of non-existence via "domination intervals" of record values of $m+\tau(m)$, with a Lean formalization. T. Tao noted that the asymptotic step ($n>69$) was unjustified and was assumed as an axiom in the Lean code. Described as withdrawn in arXiv:2608.17880.

### B.6 Formalization
- Lean statement: [google-deepmind/formal-conjectures `ErdosProblems/647.lean`](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/647.lean).

---

## C. Open questions for this project (to address in later sessions)
- Verify or refute reductions B.4(1)–(4) independently.
- Do a systematic search of the refereed literature.
- Read the primary Erdős sources ([Er79], [Er79d]) directly and confirm the wording.
