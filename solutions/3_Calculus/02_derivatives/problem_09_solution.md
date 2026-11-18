### Problem 9. A Logarithm and the Chain Rule

#### Question

For

$$
f(x) = \ln(x^2 + 1)
$$

compute the derivative. Then determine the sign of $f'(x)$ for $x < 0$, $x = 0$, and $x > 0$, and describe qualitatively how the function behaves around zero.

---

### Solution

#### Step 1. Check the domain and identify the inner and outer functions

Since $x^2 + 1 \ge 1 > 0$ for all $x \in \mathbb{R}$, the function $f(x) = \ln(x^2 + 1)$ is defined and differentiable everywhere on $(-\infty, +\infty)$.

Decompose $f(x) = g(u(x))$ into two layers:
- **Outer function:** $g(u) = \ln(u)$, with derivative $g'(u) = \frac{1}{u}$
- **Inner function:** $u(x) = x^2 + 1$, with derivative $u'(x) = 2x$

---

#### Step 2. Apply the Chain Rule to compute $f'(x)$

Using the Chain Rule $\frac{d}{dx}[g(u(x))] = g'(u(x)) \cdot u'(x)$:

$$
\begin{aligned}
f'(x)
&= \frac{1}{u(x)} \cdot u'(x) \\
&= \frac{1}{x^2 + 1} \cdot 2x \\
&= \frac{2x}{x^2 + 1}
\end{aligned}
$$

Thus, the derivative is:

$$
f'(x) = \frac{2x}{x^2 + 1}
$$

---

#### Step 3. Determine the sign of $f'(x)$ for $x < 0$, $x = 0$, and $x > 0$

Observe that the denominator $x^2 + 1$ is strictly positive ($x^2 + 1 \ge 1 > 0$) for every real number $x$. Therefore, the sign of $f'(x) = \frac{2x}{x^2 + 1}$ is determined entirely by the sign of the numerator $2x$:

1. **For $x < 0$:**
   The numerator $2x < 0$ while the denominator $x^2 + 1 > 0$, so:

   $$
   f'(x) < 0 \quad \text{(negative)}
   $$

2. **For $x = 0$:**
   The numerator $2(0) = 0$ while the denominator $0^2 + 1 = 1 > 0$, so:

   $$
   f'(0) = 0 \quad \text{(zero)}
   $$

3. **For $x > 0$:**
   The numerator $2x > 0$ while the denominator $x^2 + 1 > 0$, so:

   $$
   f'(x) > 0 \quad \text{(positive)}
   $$

---

#### Step 4. Qualitative behavior of $f(x)$ around $x = 0$

- **Decreasing to the left of zero ($x < 0$):** Because $f'(x) < 0$ on $(-\infty, 0)$, the graph of $f(x)$ slopes downward as $x$ approaches $0$ from the left.
- **Horizontal tangent and global minimum at $(0, 0)$:** At $x = 0$, $f(0) = \ln(0^2 + 1) = \ln(1) = 0$ and $f'(0) = 0$. The tangent line at the origin is horizontal ($y = 0$), and because $f'(x)$ changes sign from negative to positive across $x = 0$ (and $x^2 + 1 \ge 1 \implies \ln(x^2 + 1) \ge 0$), the point $(0, 0)$ is a **local and global minimum** (a smooth valley bottom).
- **Increasing to the right of zero ($x > 0$):** Because $f'(x) > 0$ on $(0, +\infty)$, the graph slopes upward after passing through the origin.
- **Symmetry:** Because $f(-x) = \ln((-x)^2 + 1) = \ln(x^2 + 1) = f(x)$, the function is **even**, meaning its graph is symmetric with respect to the $y$-axis as it curves smoothly upward on both sides of $(0, 0)$.