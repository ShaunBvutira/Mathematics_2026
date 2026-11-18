### Problem 4. A Quotient and Domain Control

#### Question

For

$$
f(x) = \frac{x^2 + 1}{x - 1}
$$

determine the domain, compute the derivative, simplify the result, and explain why the restriction $x \neq 1$ remains important.

---

### Solution

#### Step 1. Determine the domain of $f(x)$

Since $f(x) = \frac{x^2 + 1}{x - 1}$ is a rational function, it is defined for all real numbers $x \in \mathbb{R}$ except where the denominator equals zero:

$$
x - 1 = 0 \implies x = 1
$$

Thus, the domain of $f(x)$ is:

$$
D_f = \mathbb{R} \setminus \{1\} = (-\infty, 1) \cup (1, +\infty)
$$

---

#### Step 2. Compute the derivative using the Quotient Rule

Identify the numerator $u(x)$ and denominator $v(x)$ along with their derivatives:

$$
u(x) = x^2 + 1 \implies u'(x) = 2x
$$

$$
v(x) = x - 1 \implies v'(x) = 1
$$

Apply the Quotient Rule $\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^2}$:

$$
\begin{aligned}
f'(x)
&= \frac{u'(x)v(x) - u(x)v'(x)}{[v(x)]^2} \\
&= \frac{(2x)(x - 1) - (x^2 + 1)(1)}{(x - 1)^2}
\end{aligned}
$$

---

#### Step 3. Simplify the numerator

Expand the products in the numerator and combine like terms (leaving the denominator in factored form $(x - 1)^2$):

$$
\begin{aligned}
f'(x)
&= \frac{2x^2 - 2x - x^2 - 1}{(x - 1)^2} \\
&= \frac{x^2 - 2x - 1}{(x - 1)^2}
\end{aligned}
$$

*(Note: The quadratic numerator $x^2 - 2x - 1$ has roots $x = 1 \pm \sqrt{2}$, neither of which equals $1$, so no common factor $(x - 1)$ cancels out.)*

Thus, the simplified derivative is:

$$
f'(x) = \frac{x^2 - 2x - 1}{(x - 1)^2}, \qquad x \neq 1
$$

---

#### Step 4. Explain why the restriction $x \neq 1$ remains important

1. **Zero Denominator in $f'(x)$:**
   In the derivative formula $f'(x) = \frac{x^2 - 2x - 1}{(x - 1)^2}$, substituting $x = 1$ yields $\frac{-2}{0}$, which is undefined. The domain of $f'(x)$ is therefore $D_{f'} = \mathbb{R} \setminus \{1\}$, matching $D_f$.
2. **Non-Differentiability at a Discontinuity:**
   A function can only have a derivative at points where it is defined and continuous. At $x = 1$, $f(x)$ has an infinite discontinuity (a **vertical asymptote** along the line $x = 1$, since $\lim_{x \to 1^-} f(x) = -\infty$ and $\lim_{x \to 1^+} f(x) = +\infty$), so no tangent line exists there.
3. **Sign Analysis Across Intervals:**
   Because $(x - 1)^2 > 0$ for all $x \neq 1$, the sign of $f'(x)$ matches the sign of the numerator $x^2 - 2x - 1 = (x - (1 - \sqrt{2}))(x - (1 + \sqrt{2}))$. However, $x = 1$ splits the domain into two separate intervals $(-\infty, 1)$ and $(1, +\infty)$:
   - $f'(x) > 0$ on $(-\infty, 1 - \sqrt{2})$ and $(1 + \sqrt{2}, +\infty)$ ($f$ increases),
   - $f'(x) < 0$ on $(1 - \sqrt{2}, 1)$ and $(1, 1 + \sqrt{2})$ ($f$ decreases).
   
   Forgetting the restriction $x \neq 1$ would falsely suggest that $f(x)$ decreases continuously across the entire interval $(1 - \sqrt{2}, 1 + \sqrt{2})$, ignoring the vertical asymptote break at $x = 1$.