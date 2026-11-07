# A Goldbach-Type Problem for the Unitary Möbius Function

[English](README.md) | [简体中文](README.zh-CN.md)

This repository hosts the English manuscript of a study of additive sign patterns for the **unitary Möbius function**. The project investigates how the prime-factor structure of two positive integers interacts with the constraint that their sum is a prescribed integer.

**Contributors:** 田草林 (Tian Caolin) and 杨晨曦 (Yang Chenxi).

## Read the paper

[A Goldbach-Type Problem for the Unitary Möbius Function (PDF)](paper_english.pdf)

The PDF contains the definitions, theorem statements, proofs, references, and appendices describing finite verification. The results summarized below are those stated in the manuscript.

## Mathematical setting

Let $\omega(n)$ be the number of **distinct** prime factors of a positive integer $n$, with $\omega(1)=0$, and define

$$
g(n)=(-1)^{\omega(n)}.
$$

For $s,t\in\lbrace-1,+1\rbrace$, the ordered representation count is

$$
R_{st}(N)=\operatorname{card}\left\lbrace 1\le a<N:g(a)=s,\ g(N-a)=t\right\rbrace.
$$

The question is whether, and how often, each of the four sign patterns occurs among decompositions $N=a+(N-a)$. Representations are ordered: swapping the summands generally gives a different representation.

The function $g$ is multiplicative but not completely multiplicative. It differs from the Liouville function, which counts prime factors with multiplicity, and from the ordinary Möbius function, which vanishes on integers divisible by a prime square.

## Main results

### 1. Quantitative bounds for every sufficiently large integer

The manuscript proves that, for all sufficiently large $N$,

$$
R_{--}(N),R_{++}(N)\ge\frac{N}{128(\log N)^3},
\qquad
R_{-+}(N)=R_{+-}(N)\ge\frac{N}{64(\log N)^3}.
$$

Here $\log$ is the natural logarithm. The starting point for these quantitative bounds is not evaluated numerically in the manuscript; the explicit existence result below is a separate theorem.

### 2. Explicit existence and complete exceptional sets

For every integer $N\ge18$, all four ordered sign patterns occur. The complete exceptional sets for integers $N\ge2$ are:

| Pattern | Integers $N$ for which the representation count is zero |
|---|---|
| $(-1,-1)$ | $2,3$ |
| $(-1,+1)$ and $(+1,-1)$ | $2,7$ |
| $(+1,+1)$ | $3,4,5,6,8,9,10,14,17$ |

Thus the optimal common eventual threshold is $18$. The individual eventual thresholds are $4$ for the negative-negative pattern, $8$ for the mixed patterns, and $18$ for the positive-positive pattern. These are eventual thresholds, not assertions that every smaller integer is exceptional.

### 3. One-quarter asymptotics for almost all integers

The manuscript establishes

$$
R_{st}(N)=\frac N4+o(N)
$$

for almost all target integers, with a stronger quantitative exceptional-set estimate in the paper. A pointwise one-quarter asymptotic for **every** sufficiently large integer is not proved.

### 4. Questions for the ordinary Möbius function

The paper also studies the nine additive sign patterns arising from $\mu(n)\in\lbrace-1,0,+1\rbrace$. It distinguishes unconditional estimates for patterns involving zero from the unresolved correlation questions governing pointwise asymptotics for the four nonzero patterns.

## Approach and significance

The arguments combine arithmetic identities and integer decompositions, mean-value and exponential-sum estimates, rigidity of missing sign patterns, finite covering chains, and finite integer verification. For explicit existence, the proof separates the infinite range $N\ge100000$ from an exhaustive check of $2\le N<100000$.

The project connects multiplicative structure with additive representation problems. Its explicit classification gives exact small exceptions and sharp eventual existence thresholds, while the quantitative and almost-all results describe how frequently representations occur. It also highlights why density information alone does not settle an additive representation problem.

This is a Goldbach-**type** problem for arithmetic sign sets, not a proof of the classical Goldbach conjecture. A summand with $g(n)=-1$ need not be prime.

## Repository contents and scope

```text
.
├── README.md          English project overview
├── README.zh-CN.md    Chinese project overview
├── paper_english.pdf  English manuscript
└── .gitignore         Source/build-artifact exclusion rules
```

This version is a **manuscript distribution repository**. It does not include Lean source files, executable verification programs, or the complete certificate datasets described in the paper. Their description in the manuscript should not be read as a claim that they are bundled here; consult the manuscript's links for related materials.

LaTeX source files and compilation intermediates are deliberately excluded from version control through `.gitignore`. The compiled manuscript PDF is included. No LaTeX or Lean installation is required to read this repository.

## Contributors

- **田草林 / Tian Caolin**
- **杨晨曦 / Yang Chenxi**

For mathematical details and literature references, please consult the [manuscript](paper_english.pdf).
