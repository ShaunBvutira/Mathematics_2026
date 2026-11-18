### Exercise 5. The Classical Limit Leading to the Number $e$

#### Question

Compute

$$
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n.
$$

Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

---

### Solution

#### Step 1. Identify the limit

By the fundamental analytical definition of Euler's number $e$:

$$
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e \approx 2.718281828459\dots
$$

Notice that the expression presents the indeterminate form $1^\infty$:
- The base $1 + \frac{1}{n} \to 1$ as $n \to \infty$, which pushes the expression toward $1$.
- Simultaneously, the exponent $n \to +\infty$, which pushes any base strictly greater than $1$ toward $+\infty$.
- These two competing effects balance out at the finite irrational constant **$e$**.

---

#### Step 2. Calculate values for increasing $n$

Let $a_n = \left(1 + \frac{1}{n}\right)^n$. Evaluating $a_n$ across several powers of $10$:

| $n$ | Formula $\left(1 + \frac{1}{n}\right)^n$ | Decimal Approximation | Distance from $e$ ($e - a_n$) |
| :--- | :--- | :--- | :--- |
| $1$ | $(1 + 1)^1$ | $2.000000$ | $0.718282$ |
| $2$ | $(1 + 0.5)^2$ | $2.250000$ | $0.468282$ |
| $10$ | $(1 + 0.1)^{10}$ | $2.593742$ | $0.124539$ |
| $100$ | $(1 + 0.01)^{100}$ | $2.704814$ | $0.013468$ |
| $1{,}000$ | $(1 + 0.001)^{1{,}000}$ | $2.716924$ | $0.001358$ |
| $10{,}000$ | $(1 + 0.0001)^{10{,}000}$ | $2.718146$ | $0.000136$ |
| $100{,}000$ | $(1 + 0.00001)^{100{,}000}$ | $2.718268$ | $0.000014$ |

---

#### Step 3. Compare the observed behavior with the limit value

1. **Monotonic Increase from Below:** Every computed term is strictly less than $e \approx 2.718282$, and each increase in $n$ produces a strictly larger value ($a_1 < a_2 < a_{10} < a_{100} < \dots < e$).
2. **Diminishing Growth Steps:** Initially, the sequence jumps rapidly (from $2$ to $2.25$ to $2.5937$), but as $n$ grows larger, successive increments shrink dramatically—stabilizing digit by digit from left to right ($2.7 \to 2.71 \to 2.718 \to 2.7182$).
3. **Rate of Convergence:** The error $e - a_n$ is roughly $\frac{e}{2n}$, meaning multiplying $n$ by $10$ reduces the gap to $e$ by approximately a factor of $10$ (gaining roughly one new accurate decimal place per order of magnitude in $n$).

---

#### Step 4. Explain why a few values do not constitute a proof

Computing a finite table of values only provides empirical evidence, never a mathematical proof, for four fundamental reasons:

1. **Limits Govern Infinite Tails, Not Finite Prefixes:** By definition, $\lim_{n \to \infty} a_n = L$ requires that for *every* tolerance $\varepsilon > 0$, there exists an index $N$ such that $|a_n - L| < \varepsilon$ for **all** $n > N$. Checking $n = 10$ or $n = 100{,}000$ tells us nothing with certainty about what happens for $n > 10^{100}$.
2. **A Sequence Could Diverge or Drift Later:** A sequence can appear to level off over millions of terms and still diverge slowly to $+\infty$ (for example, $b_n = 2.71828 + \frac{\ln(\ln n)}{10^6}$ looks virtually constant for huge $n$, yet $\lim_{n \to \infty} b_n = +\infty$).
3. **A Sequence Could Approach a Slightly Different Limit:** Numerical values alone cannot distinguish whether the true limit is $e \approx 2.7182818\dots$ or a nearby number such as $2.7182820$, nor can finite decimal evaluations prove that the sequence is bounded above (e.g., $a_n < 3$ for all $n$).
4. **Finite Floating-Point Precision Breaks Down:** In practice, evaluating $\left(1 + \frac{1}{n}\right)^n$ numerically for very large $n$ (such as $n = 10^{16}$) causes standard computer arithmetic to round $1 + \frac{1}{n}$ to $1.0$, falsely outputting $1.0^{10^{16}} = 1$ instead of $e$. A rigorous proof requires analytical tools—such as the Binomial Theorem combined with the Monotone Convergence Theorem (showing $a_n$ is strictly increasing and bounded above by $3$).