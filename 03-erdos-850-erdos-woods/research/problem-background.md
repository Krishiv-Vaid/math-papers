# Erdős #850: Problem Background (Erdős–Woods Conjecture)

*Compiled 2026-11-24. Items marked **unverified** could not be confirmed from primary sources. This is documentation only. No attempt at the problem has been made.*

## 1. Statement

From [erdosproblems.com/850](https://www.erdosproblems.com/850), unchanged in mathematical content:

> Can there exist two distinct integers $x$ and $y$ such that $x, y$ have the same prime factors, $x+1, y+1$ have the same prime factors, and $x+2, y+2$ also have the same prime factors?

**Definitions.** Write $\operatorname{rad}(n)=\prod_{p\mid n}p$. The question asks whether there are positive integers $x\ne y$ with
$$\operatorname{rad}(x+i)=\operatorname{rad}(y+i)\qquad (i=0,1,2).$$
The site's curator has clarified that $x, y$ are positive integers, as is implicit in multiplicative problems of this kind.

**Name.** The problem is sometimes called the **Erdős–Woods conjecture**. Erdős expected the answer to be no.

## 2. Origin and history

- **Sources:** [Er63, Problem 60] P. Erdős, *Quelques problèmes de théorie des nombres*, Monographies de L'Enseignement Mathématique, No. 6 (1963), 81–135 (MR 158847); [Er80f] P. Erdős, *Research Problems: How many pairs of products of consecutive integers have the same prime factors?*, Amer. Math. Monthly (1980), 391–392 (MR 1539384); [Er96b] P. Erdős, *Some problems I presented or planned to present in my short talk*, in Analytic Number Theory, Vol. 1 (Allerton Park, IL, 1995), 1996, 333–335 (MR 1399346).
- **Woods:** Alan R. Woods studied a general form of this question in his PhD thesis (*Some problems in logic and number theory, and their connections*, University of Manchester, 1981), in connection with the decidability of arithmetic with successor and coprimality. **The thesis was not consulted directly. This attribution is based on secondary sources.**
- R. K. Guy, *Unsolved Problems in Number Theory*, 3rd ed. (Springer, 2004), Problem **B19** discusses it.

## 3. Known results

1. **Two consecutive values have infinitely many solutions.** For pairs $x,y$ and $x+1,y+1$ alone, one can take $x=2(2^r-1)$ and $y=x(x+2)$. Erdős also asked whether there are other examples.
2. **Mąkowski's sporadic example** [Ma68: A. Mąkowski, *On a problem of Erdős*, Enseign. Math. (2) (1968), 193, MR 258733]: $x=75=3\cdot5^2$, $y=1215=3^5\cdot5$, with $76=2^2\cdot19$ and $1216=2^6\cdot19$. It was found independently by M. Bolan and by A. Dubickas, who set it in the 2024 Lithuanian team selection test. **No other examples are known.** See [OEIS A343101](https://oeis.org/A343101).
3. **Conditional answer:** T. N. Shorey and R. Tijdeman proved that the **explicit *abc* conjecture** (in a form due to Baker) implies the Erdős–Woods conjecture for each $k\ge 3$, and in particular a negative answer to #850. Reference: *Arithmetic properties of blocks of consecutive integers*, in J. Sander, J. Steuding, R. Steuding (eds.), *From Arithmetic to Zeta-Functions*, Springer, 2016, 455–471, [doi:10.1007/978-3-319-28203-9_27](https://doi.org/10.1007/978-3-319-28203-9_27); [arXiv:1612.05438](https://arxiv.org/abs/1612.05438).
4. **Related work:** R. Balasubramanian, T. N. Shorey, M. Waldschmidt, *On the maximal length of two sequences of consecutive integers with the same prime divisors*, Acta Math. Hungar. **54** (1989), 225–236, [doi:10.1007/BF01952052](https://doi.org/10.1007/BF01952052). The main theorem has not yet been reviewed for this project.
5. The two-term case appeared as Problem 1 of the 3rd Benelux Mathematical Olympiad (2011).
6. **Related but distinct:** *Erdős–Woods numbers* (lengths $k$ of intervals $[a,a+k]$ in which every element shares a factor with an endpoint) come from the same circle of ideas; see D. L. Dowe, J. Austral. Math. Soc. Ser. A **47** (1989), 84–89. They are **not** the subject of #850.

## 4. Prize

**None listed.** The database records `prize: "no"`.

## 5. Current status

- **Open.** Database label **verifiable** ([teorth/erdosproblems](https://github.com/teorth/erdosproblems), last updated 2026-10-26). An explicit pair $(x,y)$ would settle it affirmatively.
- **Formal statement:** [formal-conjectures `ErdosProblems/850.lean`](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/850.lean).
- The database notes an AI-assisted Lean formalization (by C. Y. Ren) of the *known* facts: the infinite two-term family and Mąkowski's pair. It states explicitly that the three-term question remains open.
- See also [Erdős #677](https://www.erdosproblems.com/677).

## 6. To do (literature stage)

- Read Shorey–Tijdeman (arXiv:1612.05438) and Balasubramanian–Shorey–Waldschmidt (1989) for exact statements.
- Consult Woods's thesis.
- Find what unconditional results exist on $\operatorname{rad}(x+i)=\operatorname{rad}(y+i)$ for $i=0,1,2$.

## Citation

> T. F. Bloom, *Erdős Problem #850*, https://www.erdosproblems.com/850, accessed 2026-11-24.
