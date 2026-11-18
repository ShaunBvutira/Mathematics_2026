### Exercise 4. Powers and Oscillation

#### Question

Analyze

$$
\left(\frac{2}{3}\right)^n, \qquad \left(\frac{3}{2}\right)^n, \qquad (-1)^n, \qquad \frac{(-1)^n}{n}.
$$

For each sequence, describe the type of behavior and justify your answer.

---

### Solution

#### 1. Sequence: $a_n = \left(\frac{2}{3}\right)^n$

- **Type of Behavior:** **Monotonically decreasing and convergent** to $0$.
- **Justification:**
  - Because the base $r = \frac{2}{3}$ satisfies $0 < r < 1$, multiplying by $\frac{2}{3}$ at each step shrinks the value strictly toward zero:

    $$
    \frac{2}{3} > \left(\frac{2}{3}\right)^2 > \left(\frac{2}{3}\right)^3 > \dots > 0
    $$

  - By the standard geometric sequence limit theorem ($\lim_{n \to \infty} r^n = 0$ whenever $|r| < 1$):

    $$
    \lim_{n \to \infty} \left(\frac{2}{3}\right)^n = 0
    $$

---

#### 2. Sequence: $b_n = \left(\frac{3}{2}\right)^n$

- **Type of Behavior:** **Monotonically increasing and divergent to $+\infty$** (unbounded growth).
- **Justification:**
  - Because the base $r = \frac{3}{2} = 1.5 > 1$, each successive term increases by $50\%$:

    $$
    \frac{3}{2} < \left(\frac{3}{2}\right)^2 < \left(\frac{3}{2}\right)^3 < \dots
    $$

  - Writing $\frac{3}{2} = 1 + \frac{1}{2}$ and applying Bernoulli's inequality gives $\left(1 + \frac{1}{2}\right)^n \ge 1 + \frac{n}{2}$ for all $n \ge 1$. Since $1 + \frac{n}{2} \to +\infty$ as $n \to \infty$:

    $$
    \lim_{n \to \infty} \left(\frac{3}{2}\right)^n = +\infty
    $$

---

#### 3. Sequence: $c_n = (-1)^n$

- **Type of Behavior:** **Bounded, non-convergent (divergent by oscillation)**.
- **Justification:**
  - The terms alternate indefinitely between $-1$ and $1$:

    $$
    c_1 = -1, \quad c_2 = 1, \quad c_3 = -1, \quad c_4 = 1, \dots
    $$

  - **Even-indexed subsequence:** $\lim_{k \to \infty} c_{2k} = \lim_{k \to \infty} 1 = 1$.
  - **Odd-indexed subsequence:** $\lim_{k \to \infty} c_{2k+1} = \lim_{k \to \infty} (-1) = -1$.
  - Because two subsequences converge to different limits ($1 \neq -1$), the sequence fails to approach a single value and **diverges** (even though it remains bounded within $[-1, 1]$).

---

#### 4. Sequence: $d_n = \frac{(-1)^n}{n}$

- **Type of Behavior:** **Damped oscillation, convergent to $0$** (alternating in sign while shrinking in magnitude).
- **Justification:**
  - The numerator $(-1)^n$ causes the signs to alternate ($-1, +\frac{1}{2}, -\frac{1}{3}, +\frac{1}{4}, \dots$), while the denominator $n$ forces the absolute value $|d_n| = \frac{1}{n}$ to decay toward $0$.
  - **Squeeze Theorem Proof:** For all $n \ge 1$, the sequence is trapped between two bounding sequences:

    $$
    -\frac{1}{n} \le \frac{(-1)^n}{n} \le \frac{1}{n}
    $$

  - Since $\lim_{n \to \infty} \left(-\frac{1}{n}\right) = 0$ and $\lim_{n \to \infty} \frac{1}{n} = 0$, the Squeeze Theorem guarantees:

    $$
    \lim_{n \to \infty} \frac{(-1)^n}{n} = 0
    $$

---

### Summary Table

| Sequence | Behavior Classification | Limit ($n \to \infty$) | Key Reason |
| :--- | :--- | :--- | :--- |
| $\left(\frac{2}{3}\right)^n$ | Monotonic decay, convergent | $0$ | Geometric base $\|r\| = \frac{2}{3} < 1$ |
| $\left(\frac{3}{2}\right)^n$ | Monotonic growth, divergent | $+\infty$ | Geometric base $r = \frac{3}{2} > 1$ |
| $(-1)^n$ | Bounded oscillation, divergent | Does not exist | Subsequences approach $-1$ and $1$ |
| $\frac{(-1)^n}{n}$ | Damped oscillation, convergent | $0$ | Squeezed between $-\frac{1}{n}$ and $\frac{1}{n}$ |