### Exercise 7. Limit at a Point and Canceling a Factor

#### Question

Compute

$$
\lim_{x \to 3} \frac{x^2 - 4x + 3}{x - 3}.
$$

Explain why the value of the function at $x = 3$ is not needed to compute the limit.

---

### Solution

#### Step 1. Check direct substitution (identify the indeterminate form)

Substitute $x = 3$ into the numerator and denominator separately:
- **Numerator:** $3^2 - 4(3) + 3 = 9 - 12 + 3 = 0$
- **Denominator:** $3 - 3 = 0$

Because both approach $0$, the expression yields the indeterminate form $\frac{0}{0}$ and is undefined at $x = 3$.

---

#### Step 2. Factor the numerator and cancel the common factor

Factor the quadratic expression $x^2 - 4x + 3$ by finding two numbers that multiply to $3$ and add to $-4$ (namely $-1$ and $-3$):

$$
x^2 - 4x + 3 = (x - 1)(x - 3)
$$

Rewrite the limit and cancel the common factor $(x - 3)$, which is valid because $x \to 3$ implies $x \neq 3$ (so $x - 3 \neq 0$):

$$
\begin{aligned}
\lim_{x \to 3} \frac{x^2 - 4x + 3}{x - 3}
&= \lim_{x \to 3} \frac{(x - 1)(x - 3)}{x - 3} \\
&= \lim_{x \to 3} (x - 1)
\end{aligned}
$$

---

#### Step 3. Evaluate the simplified limit

Now that the discontinuity has been removed, apply direct substitution to the linear function $x - 1$:

$$
\lim_{x \to 3} (x - 1) = 3 - 1 = 2
$$

The limit of the function as $x \to 3$ is **$2$**.

---

#### Step 4. Explanation of why the function value at $x = 3$ is not needed

1. **Definition of a Limit ($0 < |x - 3| < \delta$):** A limit describes the behavior of $f(x)$ as $x$ gets arbitrarily *close* to $3$, explicitly excluding $x = 3$ itself. In the formal $\varepsilon$-$\delta$ definition, the condition $0 < |x - 3| < \delta$ ensures we only ever evaluate $f(x)$ at inputs $x \neq 3$.
2. **Equality on a Punctured Neighborhood:** For every real number $x \neq 3$, the factor $(x - 3)$ is non-zero, so the original rational function $f(x) = \frac{x^2 - 4x + 3}{x - 3}$ and the simplified linear function $g(x) = x - 1$ produce the **exact same outputs**. Since two functions that agree everywhere near $x = 3$ (except possibly at $x = 3$) must have the same limit, $\lim_{x \to 3} f(x) = \lim_{x \to 3} g(x) = 2$.
3. **Geometric Meaning (Removable Discontinuity):** The graph of $y = \frac{x^2 - 4x + 3}{x - 3}$ is identical to the straight line $y = x - 1$, except it has an open "hole" at the point $(3, 2)$. Whether that hole is left empty ($f(3)$ undefined) or filled in at a different height (say $f(3) = 10$), the curve still approaches height $y = 2$ from both sides as $x \to 3$.