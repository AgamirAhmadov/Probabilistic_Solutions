# List 5 Task 1 — Discrete Distribution Given by a PMF Table

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

```text
Ω = {ω1, ω2, ω3, ω4, ω5}
```

---

# 3. Elementary Outcomes and Probabilities

| Outcome | Probability |
|---|---|
| ω1 | 0.10 |
| ω2 | 0.25 |
| ω3 | 0.30 |
| ω4 | 0.20 |
| ω5 | 0.15 |

---

# 4. Random Variable X

Define:

```text
X(ω1) = -2
X(ω2) = 0
X(ω3) = 1
X(ω4) = 3
X(ω5) = 5
```

Thus:

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 5. Support of X

```text
Supp(X) = {-2, 0, 1, 3, 5}
```

The support contains all possible values of the random variable.

---

# 6. Verification of the Probability Distribution

A valid probability distribution must satisfy:

- Every probability is between 0 and 1.
- The total sum must equal 1.

Check:

```text
0.10 + 0.25 + 0.30 + 0.20 + 0.15 = 1
```

Therefore, this is a valid probability distribution.

---

# 7. Probability Mass Function (PMF)

The PMF is:

```text
p(x) = P(X = x)
```

## PMF Graph

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

```text
x = 1
```

because:

```text
P(X = 1) = 0.30
```

---

# 8. Cumulative Distribution Function (CDF)

The cumulative distribution function is:

```text
F(x) = P(X ≤ x)
```

Compute cumulative probabilities:

| Interval | F(x) |
|---|---|
| x < -2 | 0 |
| -2 ≤ x < 0 | 0.10 |
| 0 ≤ x < 1 | 0.35 |
| 1 ≤ x < 3 | 0.65 |
| 3 ≤ x < 5 | 0.85 |
| x ≥ 5 | 1 |

---

## CDF Graph

```text
1.00 |                                   ┌──────────
0.85 |                           ┌───────┘
0.65 |                   ┌───────┘
0.35 |           ┌───────┘
0.10 |   ┌───────┘
0.00 +───┴────────┴────────┴────────┴────────────
       -2        0        1        3        5
```

The CDF is a step function.

---

# 9. Relationship Between PMF and CDF

For a discrete random variable:

```text
P(X = x) = F(x) - F(x⁻)
```

where:

```text
F(x⁻)
```

is the value just before the jump.

The jump size equals the probability at that point.

Example:

```text
F(1) - F(1⁻) = 0.65 - 0.35 = 0.30
```

Therefore:

```text
P(X = 1) = 0.30
```

---

# 10. Probability Calculations

## Example 1 — Exact Probability

```text
P(X = 1) = 0.30
```

---

## Example 2 — Less Than or Equal

```text
P(X ≤ 1) = 0.10 + 0.25 + 0.30 = 0.65
```

Using the CDF:

```text
F(1) = 0.65
```

---

## Example 3 — Strictly Less Than

```text
P(X < 1) = 0.10 + 0.25 = 0.35
```

Using the CDF:

```text
F(1⁻) = 0.35
```

---

## Example 4 — Interval Probability

```text
P(0 < X ≤ 3) = 0.30 + 0.20 = 0.50
```

Using the CDF:

```text
F(3) - F(0) = 0.85 - 0.35 = 0.50
```

---

## Example 5 — Greater Than or Equal

```text
P(X ≥ 1) = 0.30 + 0.20 + 0.15 = 0.65
```

Using the CDF:

```text
1 - F(1⁻) = 1 - 0.35 = 0.65
```

---

# 11. Comparison of PMF and CDF

| Probability Type | PMF Method | CDF Method |
|---|---|---|
| P(X = a) | Direct lookup | Jump size |
| P(X ≤ a) | Sum probabilities | F(a) |
| P(X < a) | Sum smaller probabilities | F(a⁻) |
| Interval probability | Sum selected values | Difference of CDF values |

The CDF is often more convenient for interval probabilities.

---

# 12. Interactive Application Idea

A small Python or HTML/JavaScript application could allow the user to:

- display the PMF graph,
- display the CDF graph,
- compute probabilities interactively,
- modify probabilities,
- compare PMF and CDF visually.

---

# Conclusion

This task demonstrates how a discrete probability distribution can be represented using:

- the Probability Mass Function (PMF),
- and the Cumulative Distribution Function (CDF).

The PMF gives probabilities for exact values, while the CDF shows accumulated probability up to a given point.

The jumps of the CDF are exactly equal to the PMF probabilities.
