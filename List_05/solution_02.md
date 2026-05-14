# LIst 5 Task 2 — Discrete Distribution Given by a CDF Table

## Given CDF Table

| x | -1 | 0 | 2 | 4 | 6 |
|---|---|---|---|---|---|
| F(x) | 0.15 | 0.35 | 0.60 | 0.85 | 1.00 |

---

# 1. Construct one possible finite probability space Ω and define a random variable X on Ω whose CDF is the one given in the table.

## Solution

One possible sample space is:

```text
Ω = {ω1, ω2, ω3, ω4, ω5}
```

Define the random variable:

```text
X(ω1) = -1
X(ω2) = 0
X(ω3) = 2
X(ω4) = 4
X(ω5) = 6
```

The cumulative probabilities are:

| x | F(x) |
|---|---|
| -1 | 0.15 |
| 0 | 0.35 |
| 2 | 0.60 |
| 4 | 0.85 |
| 6 | 1.00 |

---

# 2. Reconstruct the PMF from the jumps of the CDF.

## Solution

For a discrete random variable:

```text
P(X = x) = F(x) - F(x⁻)
```

The jump size at each point gives the probability at that value.

Compute the jumps:

| x | Calculation | P(X=x) |
|---|---|---|
| -1 | 0.15 - 0 | 0.15 |
| 0 | 0.35 - 0.15 | 0.20 |
| 2 | 0.60 - 0.35 | 0.25 |
| 4 | 0.85 - 0.60 | 0.25 |
| 6 | 1.00 - 0.85 | 0.15 |

Thus the PMF is:

| x | -1 | 0 | 2 | 4 | 6 |
|---|---|---|---|---|---|
| P(X=x) | 0.15 | 0.20 | 0.25 | 0.25 | 0.15 |

---

# 3. Draw the graph of the PMF.

## Solution

```text
Probability

0.25 |                 █       █
0.20 |         █       █       █
0.15 | █       █       █       █       █
0.10 | █       █       █       █       █
0.05 | █       █       █       █       █
0.00 +-----------------------------------------
        -1      0       2       4       6
```

The highest probabilities occur at:

```text
x = 2 and x = 4
```

because:

```text
P(X=2)=0.25
P(X=4)=0.25
```

---

# 4. Redraw the CDF carefully, emphasizing its stepwise character.

## Solution

The CDF is:

| Interval | F(x) |
|---|---|
| x < -1 | 0 |
| -1 ≤ x < 0 | 0.15 |
| 0 ≤ x < 2 | 0.35 |
| 2 ≤ x < 4 | 0.60 |
| 4 ≤ x < 6 | 0.85 |
| x ≥ 6 | 1.00 |

---

## CDF Graph

```text
1.00 |                                   ┌──────────
0.85 |                           ┌───────┘
0.60 |                   ┌───────┘
0.35 |           ┌───────┘
0.15 |   ┌───────┘
0.00 +───┴────────┴────────┴────────┴────────────
       -1        0        2        4        6
```

The CDF is a step function because the distribution is discrete.

---

# 5. Identify all points at which the CDF jumps.

## Solution

The CDF jumps at:

```text
x = -1, 0, 2, 4, 6
```

These are exactly the values in the support of X.

---

# 6. Explain why the jump size at a point equals the probability of that value.

## Solution

For discrete distributions:

```text
P(X=x)=F(x)-F(x⁻)
```

The CDF accumulates probability from left to right.

Whenever probability is added at a point, the graph jumps upward.

Example at x = 2:

```text
F(2)-F(2⁻)
= 0.60 - 0.35
= 0.25
```

Therefore:

```text
P(X=2)=0.25
```

The jump size equals the probability at that point.

---

# 7. Compute several probabilities using the CDF.

## Solution

### Less Than or Equal

```text
P(X ≤ 2)=F(2)=0.60
```

---

### Strictly Less Than

```text
P(X < 2)=F(2⁻)=0.35
```

---

### Exact Probability

```text
P(X=2)
=F(2)-F(2⁻)
=0.60-0.35
=0.25
```

---

### Interval Probability

```text
P(0 < X ≤ 4)
```

Possible values:

```text
2 and 4
```

Thus:

```text
0.25 + 0.25 = 0.50
```

Using the CDF:

```text
F(4)-F(0)
=0.85-0.35
=0.50
```

---

### Greater Than

```text
P(X > 2)
```

Possible values:

```text
4 and 6
```

Thus:

```text
0.25 + 0.15 = 0.40
```

Using the CDF:

```text
1-F(2)
=1-0.60
=0.40
```

---

# 8. Compare this task with Task 1 and explain what information is immediate from the PMF and what information is immediate from the CDF.

## Solution

| PMF | CDF |
|---|---|
| Gives exact probabilities directly | Gives cumulative probabilities directly |
| Easy for P(X=a) | Easy for P(X≤a) |
| Bar graph | Step graph |
| Probabilities at points | Running total of probabilities |

In Task 1, the PMF was given directly and the CDF had to be constructed.

In Task 2, the CDF was given directly and the PMF had to be reconstructed from the jumps.

Both representations describe the same probability distribution.

---

# 9. If possible, extend the application from Task 1 so that it also accepts input in CDF form.

## Solution

The application from Task 1 can be extended by:

- allowing the user to input cumulative probabilities,
- automatically computing PMF values from CDF jumps,
- displaying both PMF and CDF graphs,
- validating whether the CDF is nondecreasing,
- checking whether the final value equals 1.

---

# Conclusion

This task demonstrates how a discrete distribution can be reconstructed from its cumulative distribution function.

The CDF provides accumulated probabilities, while the PMF can be obtained from the jump sizes of the CDF.

Both forms represent the same distribution but emphasize different aspects of probability.
