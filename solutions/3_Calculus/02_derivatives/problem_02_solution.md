### Problem 2. Powers, Roots, and the Domain

#### Question

For

$$
f(x) = 2\sqrt{x} - \frac{3}{x^2} + x^{3/2}
$$

1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

---

### Solution

#### 1. Rewrite the function using powers

Convert the radical $\sqrt{x}$ into a fractional exponent ($x^{1/2}$) and the reciprocal term $\frac{3}{x^2}$ into a negative exponent ($3x^{-2}$):

$$
f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}
$$

---

#### 2. Determine the domain of $f(x)$

Examine each term in $f(x)$ over the real numbers $\mathbb{R}$:
- **$2\sqrt{x} = 2x^{1/2}$:** Requires the radicand to be non-negative: $x \ge 0$.
- **$-\frac{3}{x^2} = -3x^{-2}$:** Requires the denominator to be non-zero: $x^2 \neq 0 \implies x \neq 0$.
- **$x^{3/2} = (\sqrt{x})^3$:** Requires $x \ge 0$.

Intersecting all conditions ($x \ge 0$ and $x \neq 0$) restricts $x$ to strictly positive real numbers:

$$
D_f = (0, +\infty)
$$

---

#### 3. Compute the derivative $f'(x)$

Apply the power rule $\frac{d}{dx}(x^n) = nx^{n-1}$ term by term to $f(x) = 2x^{1/2} - 3x^{-2} + x^{3/2}$:

$$
\begin{aligned}
f'(x)
&= 2 \cdot \left(\frac{1}{2}x^{\frac{1}{2} - 1}\right) - 3 \cdot \left(-2x^{-2 - 1}\right) + \frac{3}{2}x^{\frac{3}{2} - 1} \\
&= x^{-1/2} + 6x^{-3} + \frac{3}{2}x^{1/2}
\end{aligned}
$$

Rewriting in radical and fraction form:

$$
f'(x) = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}
$$

---

#### 4. Compare the domain of $f(x)$ with the domain of $f'(x)$

Examine the domain restrictions of $f'(x) = \frac{1}{\sqrt{x}} + \frac{6}{x^3} + \frac{3}{2}\sqrt{x}$:
- **$\frac{1}{\sqrt{x}}$:** Requires $x > 0$ (both $x \ge 0$ for the root and $x \neq 0$ for the denominator).
- **$\frac{6}{x^3}$:** Requires $x \neq 0$.
- **$\frac{3}{2}\sqrt{x}$:** Requires $x \ge 0$.

Intersecting these conditions gives the domain of the derivative:

$$
D_{f'} = (0, +\infty)
$$

**Comparison:**
- **Exact Equality ($D_{f'} = D_f = (0, +\infty)$):** Here, the domain of the derivative is identical to the domain of the original function.
- **Why no endpoint was lost:** Normally, differentiating $\sqrt{x}$ or $x^{3/2}$ shrinks their natural domain from $[0, +\infty)$ to $(0, +\infty)$ because $\frac{1}{\sqrt{x}}$ is undefined at $x = 0$ (vertical tangent). However, because $f(x)$ already contained the term $-\frac{3}{x^2}$, the point $x = 0$ was already excluded from $D_f$. Since $f(x)$ is smooth and differentiable at every point in $(0, +\infty)$, no additional points are lost when differentiating.