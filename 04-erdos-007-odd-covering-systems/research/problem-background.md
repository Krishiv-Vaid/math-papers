# Erdős #7: Problem Background (Odd Covering Problem)

*Compiled 2026-11-24. Items marked **unverified** could not be confirmed from primary sources. This is documentation only. No attempt at the problem has been made.*

## 1. Statement

From [erdosproblems.com/7](https://www.erdosproblems.com/7), unchanged in mathematical content:

> Is there a distinct covering system all of whose moduli are odd?

### Definitions

- A **covering system** is a finite collection of congruence classes $a_1 \bmod n_1,\ \dots,\ a_k \bmod n_k$ whose union is all of $\mathbb Z$.
- It is **distinct** if the moduli are pairwise distinct and all exceed $1$: $1<n_1<n_2<\dots<n_k$.
- The question asks whether such a system can have **every $n_i$ odd**.

**Classical example (with even moduli).** $\{0\bmod 2,\ 0\bmod 3,\ 1\bmod 4,\ 5\bmod 6,\ 7\bmod 12\}$ is a distinct covering system. It uses even moduli, so it is not an example for #7.

## 2. Origin and history

- **Covering systems** were introduced by Erdős in 1950: P. Erdős, *On integers of the form $2^k+p$ and some related problems*, Summa Brasil. Math. **2** (1950), 113–123.
- **The odd covering question** was asked by **Erdős and Selfridge**, sometimes also with **Schinzel**. They also asked the stronger question of whether all moduli can be odd *and squarefree*.
- **Erdős sources** (per erdosproblems.com): [Er57] Michigan Math. J. (1957) 291–300; [Er61]; [Er65]; [Er65b]; [Er73]; [ErGr80]; [Er82e]; [Er90]; [Er95, p. 166]; [Er96b]; [Er97]; [Er97c]; [Er97e]. Full titles are in the site's bibliography.
- **Selfridge's reduction** (reported by Schinzel, [Sc67] A. Schinzel, *Reducibility of polynomials and covering systems of congruences*, Acta Arith. **13** (1967/68), 91–101): an odd covering exists if a covering exists whose moduli form an antichain under divisibility. The latter has since been shown not to exist ([Erdős #586](https://www.erdosproblems.com/586)), so this route gives nothing.

## 3. Prize

| Offer | Details | Source |
|---|---|---|
| Erdős: **$25** | for a proof that **no** odd covering exists (Erdős believed one does exist) | M. Filaseta, K. Ford, S. Konyagin, Illinois J. Math. **44** (2000), 633–643 [FFK00], as quoted on erdosproblems.com/7 |
| Selfridge: **$300**, later **$2000** | for the first **explicit example** of an odd covering. FFK00 report that Selfridge raised it to $2000 in private communication. **No award was promised for a non-constructive existence proof.** | FFK00 |

**Administration.** Erdős prizes are now awarded by the Combinatorics Foundation (administered by Steve Butler), only after publication in a reputable journal ([erdosproblems.com/faq](https://www.erdosproblems.com/faq)). **Unverified:** whether anyone now honours Selfridge's separate offer. Selfridge died in 2010.

## 4. Known results

### Refereed
1. **Hough–Nielsen (2019):** every distinct covering system has a modulus divisible by 2 or by 3. So a hypothetical odd covering must use a modulus divisible by 3. R. D. Hough, P. P. Nielsen, *Covering systems with restricted divisibility*, Duke Math. J. **168** (2019), 3261–3295.
2. **Balister–Bollobás–Morris–Sahasrabudhe–Tiba (2022):** there is **no** distinct covering system with all moduli odd **and squarefree**, which answers the stronger question negatively. They also give a simpler proof of Hough–Nielsen, and show that **if an odd covering exists, the lcm of its moduli is divisible by 9 or 15.** *On the Erdős covering problem: the density of the uncovered set*, Invent. Math. **228** (2022), 377–414.
3. **Background:** R. Hough, *Solution of the minimum modulus problem for covering systems*, Ann. of Math. (2) **181** (2015), 361–382. This resolves Erdős's minimum-modulus problem ([#2](https://www.erdosproblems.com/2)) and is the starting point of the "distortion method".

### Preprints and other unrefereed reports
- X. Dai, H. Li, J. Li, S. Yi, *On the moduli of distinct covering systems*, [arXiv:2611.15110](https://arxiv.org/abs/2611.15110) (Nov 2026). The abstract claims that the lcm of an odd distinct covering must be divisible by **45**, and that its minimum modulus is at most **9**.
- I. Mian, S. Siddique, [arXiv:2607.25628](https://arxiv.org/abs/2607.25628) (Jul 2026): Lean 4, kernel-checked, showing any odd distinct covering has lcm $>10000$. The authors note the mathematical content is known (folklore abundancy argument plus finite checks).
- C. Bispels et al., [arXiv:2507.16135](https://arxiv.org/abs/2507.16135) (Jul 2025): studies a **variant** in which one odd modulus may repeat.
- **Folklore:** the lcm $L$ of a distinct covering satisfies $\sigma(L)\ge 2L$, i.e. it is abundant or perfect. An odd example therefore needs $L\ge 945$.
- Forum reports (unrefereed): lcm $\ge 11{,}486{,}475$ via closed-form certificates, and $\omega(\mathrm{lcm})\ge 9$ in a series of preprints. See the [thread](https://www.erdosproblems.com/forum/thread/7).

### Failed or unaccepted claims
- **Jan 2026:** a hybrid Lean/informal "candidate solution" with two axioms. Reviewers on the forum identified unjustified steps.
- **May 2026:** a claimed short proof by "sieve monotonicity" from BBMST. One of its Lean axioms was shown to be false, and the site's curator judged the approach fundamentally flawed.

## 5. Current status

- **Open.** Database label **verifiable** ([teorth/erdosproblems](https://github.com/teorth/erdosproblems), last updated 2025-08-31). An explicit odd covering would settle it, and would also win Selfridge's offer if it is honoured.
- **Formal statement:** [formal-conjectures `ErdosProblems/7.lean`](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/7.lean).
- Related: [#586](https://www.erdosproblems.com/586), [#2](https://www.erdosproblems.com/2).

## 6. To do (literature stage)

- Read BBMST (2022) §1 and Hough–Nielsen (2019) for exact theorem statements.
- Check the claims of arXiv:2611.15110 once it has been reviewed.
- Collect the full bibliographic details of the Erdős sources.

## Citation

> T. F. Bloom, *Erdős Problem #7*, https://www.erdosproblems.com/7, accessed 2026-11-24.
