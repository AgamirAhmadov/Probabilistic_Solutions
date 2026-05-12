# Task 1 — Discrete Distribution Given by a PMF Table

## Introduction

Consider a discrete random variable \(X\) whose probability mass function (PMF) is given by the following table.

| \(x\) | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| \(P(X=x)\) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 1. Random Experiment

We consider an experiment where one outcome is selected from a finite set of possible outcomes with specified probabilities.

---

# 2. Sample Space \( \Omega \)

One possible sample space is:

\[
\Omega = \{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}
\]

---

# 3. Elementary Outcomes

The elementary outcomes are:

\[
\omega_1,\omega_2,\omega_3,\omega_4,\omega_5
\]

Assign probabilities:

| Outcome | Probability |
|---|---|
| \( \omega_1 \) | 0.10 |
| \( \omega_2 \) | 0.25 |
| \( \omega_3 \) | 0.30 |
| \( \omega_4 \) | 0.20 |
| \( \omega_5 \) | 0.15 |

---

# 4. Random Variable \(X\)

Define the random variable:

\[
X(\omega_1)=-2
\]

\[
X(\omega_2)=0
\]

\[
X(\omega_3)=1
\]

\[
X(\omega_4)=3
\]

\[
X(\omega_5)=5
\]

Thus the PMF becomes:

| \(x\) | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| \(P(X=x)\) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 5. Support of \(X\)

The support of the random variable is:

\[
\text{Supp}(X)=\{-2,0,1,3,5\}
\]

The support contains all values that the random variable can take.

---

# 6. Verification of the Probability Distribution

A valid probability distribution must satisfy:

1. Every probability is between 0 and 1.
2. The total probability must equal 1.

Check the sum:

\[
0.10+0.25+0.30+0.20+0.15 = 1.00
\]

Therefore, the table defines a valid probability distribution.

---

# 7. Probability Mass Function (PMF)

The PMF is:

\[
p(x)=P(X=x)
\]

| \(x\) | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| \(p(x)\) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 8. PMF Graph

## Visual Representation

```text
Probability
0.30 ┤                 █
0.25 ┤         █       █
0.20 ┤         █       █       █
0.15 ┤         █       █       █       █
0.10 ┤ █       █       █       █       █
0.05 ┤ █       █       █       █       █
0.00 └────────────────────────────────────────
        -2      0       1       3       5
```

The largest probability occurs at:

\[
x=1
\]

since:

\[
P(X=1)=0.30
\]

---

# 9. Cumulative Distribution Function (CDF)

The cumulative distribution function is:

\[
F(x)=P(X\le x)
\]

Compute cumulative probabilities:

| Interval | \(F(x)\) |
|---|---|
| \(x<-2\) | 0 |
| \(-2\le x<0\) | 0.10 |
| \(0\le x<1\) | 0.35 |
| \(1\le x<3\) | 0.65 |
| \(3\le x<5\) | 0.85 |
| \(x\ge5\) | 1 |

Therefore:

\[
F(x)=
\begin{cases}
0, & x<-2 \\
0.10, & -2\le x<0 \\
0.35, & 0\le x<1 \\
0.65, & 1\le x<3 \\
0.85, & 3\le x<5 \\
1, & x\ge5
\end{cases}
\]

---

# 10. CDF Graph

```text
1.00 ┤                                   ┌──────────
0.85 ┤                           ┌───────┘
0.65 ┤                   ┌───────┘
0.35 ┤           ┌───────┘
0.10 ┤   ┌───────┘
0.00 └───┴────────┴────────┴────────┴────────────
      -2        0        1        3        5
```

The CDF is a step function.

---

# 11. Relationship Between PMF and CDF

For a discrete random variable:

\[
P(X=x)=F(x)-F(x^-)
\]

where:

\[
F(x^-)
\]

is the value of the CDF immediately before the jump.

Thus:

- the CDF changes only at support points,
- and the jump size equals the PMF value.

Example:

At \(x=1\):

\[
F(1)-F(1^-)=0.65-0.35=0.30
\]

Therefore:

\[
P(X=1)=0.30
\]

---

# 12. Probability Calculations

## Example 1 — Exact Probability

\[
P(X=1)=0.30
\]

---

## Example 2 — Less Than or Equal

\[
P(X\le1)
\]

\[
=0.10+0.25+0.30
\]

\[
=0.65
\]

Using the CDF:

\[
F(1)=0.65
\]

---

## Example 3 — Strictly Less Than

\[
P(X<1)
\]

\[
=0.10+0.25
\]

\[
=0.35
\]

Using the CDF:

\[
F(1^-)=0.35
\]

---

## Example 4 — Interval Probability

\[
P(0<X\le3)
\]

Possible values:

\[
1,3
\]

Thus:

\[
0.30+0.20=0.50
\]

Using the CDF:

\[
F(3)-F(0)=0.85-0.35=0.50
\]

---

## Example 5 — Greater Than or Equal

\[
P(X\ge1)
\]

\[
=0.30+0.20+0.15
\]

\[
=0.65
\]

Using the CDF:

\[
1-F(1^-)=1-0.35=0.65
\]

---

# 13. Comparison of PMF and CDF Methods

| Probability Type | PMF Method | CDF Method |
|---|---|---|
| \(P(X=a)\) | Direct lookup | Jump size |
| \(P(X\le a)\) | Sum probabilities | \(F(a)\) |
| \(P(X<a)\) | Sum smaller values | \(F(a^-)\) |
| Interval probabilities | Sum selected probabilities | Difference of CDF values |

The CDF is often more convenient for interval probabilities.

---

# 14. Interactive Application Idea

A small Python or HTML/JavaScript application could allow the user to:

- choose values of \(x\),
- display the PMF graph,
- display the CDF graph,
- compute probabilities interactively,
- compare PMF-based and CDF-based calculations.

Such an application helps visualize how probability accumulates in a discrete distribution.

---

# Conclusion

This task demonstrates how a discrete probability distribution can be represented using both:

- the Probability Mass Function (PMF),
- and the Cumulative Distribution Function (CDF).

The PMF describes the probability assigned to each exact value, while the CDF shows the accumulated probability up to a given point.

The jumps in the CDF correspond exactly to the probabilities in the PMF.
