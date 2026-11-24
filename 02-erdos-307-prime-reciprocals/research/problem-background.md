# Erdős #307: Problem Background

*Compiled 2026-11-24. Items marked **unverified** could not be confirmed from primary sources. This is documentation only. No attempt at the problem has been made.*

## 1. Statement

From [erdosproblems.com/307](https://www.erdosproblems.com/307), unchanged in mathematical content:

> Are there two finite sets of primes $P, Q$ such that
> $$1=\Bigl(\sum_{p\in P}\frac1p\Bigr)\Bigl(\sum_{q\in Q}\frac1q\Bigr)?$$

**Definitions.** $P$ and $Q$ are finite, non-empty sets of prime numbers. The question asks for an exact rational identity.

## 2. Origin and history

- **Proposer:** asked by **E. J. Barbeau** [Ba76], and included by Erdős and Graham in their problem book [ErGr80].
- **Sources:**
  - [Ba76] E. J. Barbeau, *Computer challenge corner: Problem 477: A brute force program*, J. Recreational Math. (1976). **Volume and issue unverified.**
  - [ErGr80] P. Erdős, R. L. Graham, *Old and New Problems and Results in Combinatorial Number Theory*, Monographies de L'Enseignement Mathématique **28**, Université de Genève, 1980 (MR 0592420). **Page number not verified.**
- The site notes that the problem has also been discussed on MathOverflow. **Thread not located.**

## 3. Known results and remarks

All of the following are recorded on erdosproblems.com/307 or in its archived discussion thread.

1. **Elementary constraints (stated as "easy to see" on the site).** If $P, Q$ are sets of primes giving a solution, then $P\cap Q=\varnothing$ and $\sum_{p\in P\cup Q}1/p\ge 2$. Consequently $|P\cup Q|\ge 60$.
2. **Weakened ("coprime") version.** Barbeau also asked what happens if the elements of $P$ (and of $Q$) are only required to be pairwise coprime, not prime. S. Cambie found examples, e.g.
   $$1=\Bigl(1+\tfrac15\Bigr)\Bigl(\tfrac12+\tfrac13\Bigr),\qquad 1=\Bigl(1+\tfrac1{41}\Bigr)\Bigl(\tfrac12+\tfrac13+\tfrac17\Bigr).$$
   Further examples posted in the forum include $\bigl(1+\tfrac1{1805}\bigr)\bigl(\tfrac12+\tfrac13+\tfrac17+\tfrac1{43}\bigr)=1$ and $(P,Q)=(\{1,3,11,331\},\{2,5,1559\})$.
3. **No examples are known** of the weakened version with $1\notin P\cup Q$.
4. A forum comment notes that, when $1$ is allowed, every *primary pseudoperfect number* gives a solution of the weakened version.

## 4. Prize

**None listed.** The database records `prize: "no"`, and no prize appears on the problem page.

## 5. Current status

- **Open.** Database label **verifiable** ([teorth/erdosproblems](https://github.com/teorth/erdosproblems), last updated 2025-09-09). An explicit pair $(P,Q)$ would settle it affirmatively.
- **Formal statement:** [formal-conjectures `ErdosProblems/307.lean`](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/307.lean).
- An AI-generated "proof" posted in November 2025 was shown in the forum to contain an invalid step.

## 6. To do (literature stage)

- Locate Barbeau's original problem and any published follow-up in *J. Recreational Math.*
- Locate the MathOverflow thread.
- Search for refereed work on products of sums of prime reciprocals.

## Citation

> T. F. Bloom, *Erdős Problem #307*, https://www.erdosproblems.com/307, accessed 2026-11-24.
