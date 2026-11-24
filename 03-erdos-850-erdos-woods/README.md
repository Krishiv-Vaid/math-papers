# Erdős Problem #850: The Erdős–Woods Conjecture

**Status: open** (checked 2026-11-24) · **Prize:** none listed · *Documentation stage. Not yet investigated.*

| | |
|---|---|
| Source | [erdosproblems.com/850](https://www.erdosproblems.com/850) |
| Proposers | P. Erdős; general form studied by A. R. Woods (1981) |
| Area | Number theory, prime factors of consecutive integers |
| Formal statement | [formal-conjectures/ErdosProblems/850.lean](https://github.com/google-deepmind/formal-conjectures/blob/main/FormalConjectures/ErdosProblems/850.lean) |
| OEIS | [A343101](https://oeis.org/A343101) |

## The problem

Can there exist two distinct positive integers $x\neq y$ such that $x, y$ have the same prime factors, $x+1, y+1$ have the same prime factors, and $x+2, y+2$ have the same prime factors? Equivalently, is

$$\operatorname{rad}(x+i)=\operatorname{rad}(y+i)\quad (i=0,1,2)$$

possible with $x\ne y$? A negative answer follows from an explicit form of the *abc* conjecture (Shorey–Tijdeman).

## Contents

| Path | Contents |
|---|---|
| [`research/problem-background.md`](research/problem-background.md) | Statement, history, known results, status |
| [`paper/`](paper/) | Paper (not started) |

Follow the layout of [`../01-erdos-647-divisor-count`](../01-erdos-647-divisor-count/) when the project becomes active.
