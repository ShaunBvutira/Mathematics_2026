### Problem 3. A Rational Function

#### Question

Analyze the domain, zeros, asymptotes, and monotonicity of

$$f(x) = \frac{x + 1}{x - 2}.$$

Finally, sketch a graph consistent with all the information obtained.

---

### Solution

#### Step 1. Domain of $f(x)$

Since $f(x) = \frac{x + 1}{x - 2}$ is a rational function, it is defined for all real numbers except where the denominator equals zero:

$$x - 2 = 0 \implies x = 2$$

Thus, the domain of $f(x)$ is:

$$D_f = \mathbb{R} \setminus \{2\} = (-\infty, 2) \cup (2, +\infty)$$

---

#### Step 2. Zeros and $y$-Intercept

1. **Zero ($x$-intercept):**
   Set $f(x) = 0$ (which occurs where the numerator equals zero and the denominator is non-zero):

   $$\frac{x + 1}{x - 2} = 0 \implies x + 1 = 0 \implies x = -1$$

   Since $-1 \in D_f$, the function has a single zero at **$x = -1$**, giving the $x$-intercept **$(-1, 0)$**.

2. **$y$-intercept:**
   Evaluate $f(0)$:

   $$f(0) = \frac{0 + 1}{0 - 2} = -\frac{1}{2}$$

   The graph crosses the $y$-axis at **$\left(0, -\frac{1}{2}\right)$**.

---

#### Step 3. Asymptotes

1. **Vertical Asymptote:**
   Examine the one-sided limits as $x$ approaches the excluded point $x = 2$:
   - As $x \to 2^-$: the numerator $x + 1 \to 3 > 0$, while the denominator $x - 2 \to 0^-$, so:

     $$\lim_{x \to 2^-} \frac{x + 1}{x - 2} = -\infty$$

   - As $x \to 2^+$: the numerator $x + 1 \to 3 > 0$, while the denominator $x - 2 \to 0^+$, so:

     $$\lim_{x \to 2^+} \frac{x + 1}{x - 2} = +\infty$$

   Therefore, the vertical line **$x = 2$** is a **vertical asymptote**.

2. **Horizontal Asymptote:**
   Compute the limits as $x \to \pm\infty$ by dividing numerator and denominator by $x$:

   $$\lim_{x \to \pm\infty} \frac{x + 1}{x - 2} = \lim_{x \to \pm\infty} \frac{1 + \frac{1}{x}}{1 - \frac{2}{x}} = \frac{1 + 0}{1 - 0} = 1$$

   Therefore, the horizontal line **$y = 1$** is a **horizontal asymptote** (on both the left and the right).

3. **Oblique (Slant) Asymptote:**
   None, because a horizontal asymptote exists as $x \to \pm\infty$.

---

#### Step 4. First Derivative and Monotonicity

Apply the Quotient Rule $\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^2}$ with $u(x) = x + 1$ ($u'(x) = 1$) and $v(x) = x - 2$ ($v'(x) = 1$):

$$\begin{aligned} f'(x) &= \frac{(1)(x - 2) - (x + 1)(1)}{(x - 2)^2} \\ &= \frac{x - 2 - x - 1}{(x - 2)^2} \\ &= -\frac{3}{(x - 2)^2}, \qquad x \neq 2 \end{aligned}$$

*(Alternatively, using polynomial division $f(x) = 1 + \frac{3}{x - 2}$ immediately differentiates to $f'(x) = -\frac{3}{(x - 2)^2}$.)*

**Sign Analysis and Monotonicity:**
- For every $x \in D_f = (-\infty, 2) \cup (2, +\infty)$, the denominator $(x - 2)^2 > 0$, while the numerator is $-3 < 0$.
- Consequently, **$f'(x) < 0$ everywhere on its domain**.
- Because $x = 2$ splits the domain into two separate intervals, $f(x)$ is:
  - **Strictly decreasing on $(-\infty, 2)$**, and
  - **Strictly decreasing on $(2, +\infty)$**.
- **Extrema:** Since $f'(x) \neq 0$ for all $x \in D_f$ and $f'(x)$ never changes sign, the function has **no critical points and no local or global extrema**.

---

#### Step 5. Graph Sketch

To plot the hyperbola accurately, note the transformed form $f(x) = 1 + \frac{3}{x - 2}$ (the standard hyperbola $y = \frac{3}{x}$ shifted $2$ units right and $1$ unit up) and check a few points on the right branch such as $(3, 4)$ and $(5, 2)$:

```text
          y
          ^
        4 |             |  * (3, 4)
        3 |             | /
        2 |             |/   * (5, 2)
  y = 1 --+-------------+-------------- (Horizontal Asymptote)
        0 |      *      |
  --------+------(-1,0)-+-------------> x
       -1 |       \  *  |   2
       -2 |        \ (0,-0.5)
       -3 |         \   |
       -4 |          |  |
                        x = 2 (Vertical Asymptote)