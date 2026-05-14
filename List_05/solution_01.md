# Task 1 — Discrete Distribution Given by a PMF Table

## Given PMF Table

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 1. Construct one possible finite probability space Ω and define a random variable X on Ω whose PMF is the one given in the table.

## Solution

One possible sample space is:

```text
Ω = {ω1, ω2, ω3, ω4, ω5}
```

Assign probabilities:

| Outcome | Probability |
|---|---|
| ω1 | 0.10 |
| ω2 | 0.25 |
| ω3 | 0.30 |
| ω4 | 0.20 |
| ω5 | 0.15 |

Define the random variable X:

```text
X(ω1) = -2
X(ω2) = 0
X(ω3) = 1
X(ω4) = 3
X(ω5) = 5
```

Thus the PMF becomes:

| x | -2 | 0 | 1 | 3 | 5 |
|---|---|---|---|---|---|
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

# 2. Verify whether the listed probabilities form a valid probability distribution.

## Solution

A valid probability distribution must satisfy:

- Every probability is between 0 and 1.
- The total probability must equal 1.

Check:

```text
0.10 + 0.25 + 0.30 + 0.20 + 0.15 = 1
```

Therefore, the probabilities form a valid probability distribution.

---

# 3. Draw the graph of the probability mass function.

## Solution

The PMF graph is:

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

The largest probability occurs at:

```text
x = 1
```

because:

```text
P(X = 1) = 0.30
```

---

# 4. Construct the cumulative distribution function F(x).

## Solution

The cumulative distribution function is defined as:

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

# 5. Draw the graph of the CDF.

## Solution

The CDF graph is:

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

# 6. Explain how the jumps of the CDF are related to the values of the PMF.

## Solution

For a discrete random variable:

```text
P(X = x) = F(x) - F(x⁻)
```

where:

```text
F(x⁻)
```

is the value immediately before the jump.

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

# 7. Compute several probabilities using the table.

## Solution

### Exact Probability

```text
P(X = 1) = 0.30
```

---

### Less Than or Equal

```text
P(X ≤ 1)
= 0.10 + 0.25 + 0.30
= 0.65
```

Using the CDF:

```text
F(1) = 0.65
```

---

### Strictly Less Than

```text
P(X < 1)
= 0.10 + 0.25
= 0.35
```

Using the CDF:

```text
F(1⁻) = 0.35
```

---

### Interval Probability

```text
P(0 < X ≤ 3)
= 0.30 + 0.20
= 0.50
```

Using the CDF:

```text
F(3) - F(0)
= 0.85 - 0.35
= 0.50
```

---

### Greater Than or Equal

```text
P(X ≥ 1)
= 0.30 + 0.20 + 0.15
= 0.65
```

Using the CDF:

```text
1 - F(1⁻)
= 1 - 0.35
= 0.65
```

---

# 8. Compare the results obtained directly from the PMF with those read from the CDF.

## Solution

| Probability Type | PMF Method | CDF Method |
|---|---|---|
| P(X = a) | Direct lookup | Jump size |
| P(X ≤ a) | Sum probabilities | F(a) |
| P(X < a) | Sum smaller probabilities | F(a⁻) |
| P(a < X ≤ b) | Sum selected values | Difference of CDF values |

Both methods produce the same results.

The PMF is useful for exact probabilities, while the CDF is often more convenient for interval probabilities.


---
