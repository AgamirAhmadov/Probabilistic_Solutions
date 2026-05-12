# Task 1 — Discrete Distribution Given by a PMF Table

## Given PMF Table

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 1. Random Experiment

We consider an experiment where one outcome is selected from a finite set of outcomes with known probabilities.

---

# 2. Sample Space

One possible sample space is:

```math
\Omega = \{\omega_1,\omega_2,\omega_3,\omega_4,\omega_5\}
```

---

# 3. Elementary Outcomes and Probabilities

| Outcome | Probability |
|---|---|
| \( \omega_1 \) | 0.10 |
| \( \omega_2 \) | 0.25 |
| \( \omega_3 \) | 0.30 |
| \( \omega_4 \) | 0.20 |
| \( \omega_5 \) | 0.15 |

---

# 4. Random Variable \(X\)

Define:

```math
X(\omega_1)=-2
```

```math
X(\omega_2)=0
```

```math
X(\omega_3)=1
```

```math
X(\omega_4)=3
```

```math
X(\omega_5)=5
```

Thus:

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 5. Support of \(X\)

```math
Supp(X)=\{-2,0,1,3,5\}
```

The support contains all possible values of the random variable.

---

# 6. Verification of the Probability Distribution

A valid probability distribution must satisfy:

- Every probability is between 0 and 1.
- The total sum must equal 1.

Check:

```math
0.10+0.25+0.30+0.20+0.15=1
```

Therefore, this is a valid probability distribution.

---

# 7. Probability Mass Function (PMF)

```math
p(x)=P(X=x)
```

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| p(x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 8. PMF Graph

```text
Probability

0.30 |                 █
0.25 |         █       █
0.20 |         █       █       █
0.15 |         █       █       █       █
0.10 | █       █       █       █       █
0.05 | █       █       █       █       █
0.00 +-----------------------------------------
        -2      0       1       3       5
```

The highest probability occurs at:

```math
x=1
```

because:

```math
P(X=1)=0.30
```

---

# 9. Cumulative Distribution Function (CDF)

The cumulative distribution function is:

```math
F(x)=P(X\le x)
```

Compute cumulative probabilities:

| Interval | F(x) |
|---|---|
| \(x<-2\) | 0 |
| \(-2\le x<0\) | 0.10 |
| \(0\le x<1\) | 0.35 |
| \(1\le x<3\) | 0.65 |
| \(3\le x<5\) | 0.85 |
| \(x\ge5\) | 1 |

Therefore:

````math
F(x)=
\begin{cases}
0, & x<-2 \\
0.10, & -2\le x<0 \\
0.35, & 0\le x<1 \\
0.65, & 1\le x<3 \\
0.85, & 3\le x<5 \\
1, & x\ge5
\end{cases}
