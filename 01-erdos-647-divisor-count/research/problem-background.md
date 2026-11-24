# Erdős #647: Problem Background

*Compiled 2026-11-24. Sources are linked inline. Items marked **unverified** could not be confirmed from primary sources.*

## 1. Statement

From [erdosproblems.com/647](https://www.erdosproblems.com/647), unchanged in mathematical content:

> Let $\tau(n)$ count the number of divisors of $n$. Is there some $n>24$ such that
> $$\max_{m<n}(m+\tau(m))\le n+2?$$

Here $m$ ranges over the positive integers $m<n$.

**Equivalent form.** Put $m=n-k$. The condition is
$$\tau(n-k)\le k+2\qquad(1\le k\le n-1).$$
In particular $\tau(n-1)\le 3$ (so $n-1$ is $1$, a prime, or a prime squared), $\tau(n-2)\le 4$, $\tau(n-3)\le 5$, and so on.

**Excess function.** Let $\Delta(n)=\max_{1\le m<n}(m+\tau(m))-n$ ([OEIS A400986](https://oeis.org/A400986)). The question is whether $\Delta(n)\le 2$ for some $n>24$.

**Why $n+2$.** The site notes that $\max(\tau(n-1)+n-1,\ \tau(n-2)+n-2)\ge n+2$. This is elementary for $n\ge 7$: whichever of $n-1, n-2$ is even has at least 3 divisors (if $\ge 4$) or at least 4 divisors (if $\ge 6$). So $\Delta(n)\ge 2$ for all $n\ge 7$, and the problem asks whether this minimum value is ever attained again after $24$.

**Small cases.** From the published OEIS data: $\Delta(n)\le 2$ for $n\in\{2,3,4,5,6,8,10,12,24\}$ within $n\le 24$. [A087280](https://oeis.org/A087280) lists $5, 8, 10, 12, 24$ as the solutions of the equality $\max_{m<n}(m+\tau(m))=n+2$.

## 2. Origin and history

- **Proposers:** Erdős and Selfridge (attribution on erdosproblems.com).
- **Earliest printed sources found:** P. Erdős, *Some unconventional problems in number theory*, Math. Mag. **52**(2) (1979), 67–70, Problem 4 on p. 68 (per OEIS A087280); and the paper with the same title in Acta Math. Acad. Sci. Hungar. (1979), 71–80.
- **Later appearances:** Erdős, *A survey of problems in combinatorial number theory*, Ann. Discrete Math. **6** (1980), 89–115, p. 107; *Some unsolved problems in geometry, number theory and combinatorics*, Eureka (1992), 44–48; *Some problems in number theory*, Octogon Math. Mag. (1995), 3–5; R. K. Guy, *Unsolved Problems in Number Theory*, 3rd ed. (2004), §B8.
- **Unverified:** any earlier discussion before 1979. The original texts were not read directly; statements are taken from erdosproblems.com and OEIS.

### Erdős's expectations (as reported on erdosproblems.com)

1. In [Er79], Erdős said it is "extremely doubtful" that infinitely many such $n$ exist, and suggested $\lim_{n\to\infty}\max_{m<n}(\tau(m)+m-n)=\infty$.
2. In [Er79d], he said it "seems certain" that for every $k$ there are infinitely many $n$ with $\max_{n-k<m<n}(m+\tau(m))\le n+2$, but that this is "hopeless with our present methods". He noted it follows from Schinzel's Hypothesis H.

### Related problems

Terence Tao noted that, since $\tau(m)\approx 2^{\omega(m)}$, #647 is similar to but slightly weaker than the first part of [#679](https://www.erdosproblems.com/679), and much stronger than [#413](https://www.erdosproblems.com/413) and [#248](https://www.erdosproblems.com/248).

## 3. Prize

| Question | Finding | Source |
|---|---|---|
| Is a prize listed? | Yes: **£25**, shown on the site as **$44** at approximate 1992 exchange rates | [erdosproblems.com/647](https://www.erdosproblems.com/647); [teorth database](https://github.com/teorth/erdosproblems) (`prize: "£25"`) |
| What is it for? | Erdős offered it "for an example of such an $n>24$" in [Er92e], adding "I am being rather stingy but we old people are stingy." | erdosproblems.com/647 |
| Who administers it? | Erdős prizes are now awarded by the **Combinatorics Foundation**, administered by **Steve Butler**. The website owner has no involvement. | [erdosproblems.com/faq](https://www.erdosproblems.com/faq) |
| Conditions | Awarded only after **publication in a reputable journal**, with documentation that Erdős offered the amount. Eligible solvers contact Steve Butler. | erdosproblems.com/faq |
| Claimed? | No example is known, so it has presumably not been claimed. **Unverified:** no record from the administrator was consulted. | |
| Disproof eligible? | **Unverified.** The reported offer is for an *example*. Nothing found says whether a non-existence proof qualifies. | |

## 4. Current status

- **Open.** The community database ([teorth/erdosproblems](https://github.com/teorth/erdosproblems), `data/problems.yaml`) labels it **verifiable** (open, but provable by a finite example if the answer is yes). The label was last updated 2025-08-31.
- erdosproblems.com stopped displaying statuses on 6 Oct 2026 ([*Changes*](https://www.erdosproblems.com/forum/thread/blog:9)). The problem page was last edited 7 Apr 2026.
- No $n>24$ is known. Computations by others, all **unrefereed**, report no solution up to $10^{22}$. See [literature-review.md](literature-review.md).
- A January 2026 claimed non-existence proof was shown to have an unjustified asymptotic step, which was assumed as an axiom in its Lean code. It is described as withdrawn.

## 5. Recommended citation

> T. F. Bloom, *Erdős Problem #647*, https://www.erdosproblems.com/647, accessed 2026-11-24.

Cite Erdős's original papers for the problem itself.
