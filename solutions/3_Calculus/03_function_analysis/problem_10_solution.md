### Problem 10. Complete Function Analysis

#### Question

Perform a complete analysis of

$$f(x) = \frac{x}{x^2 + 1}.$$

Include the domain, symmetry, zeros, limits, monotonicity, extrema, and convexity. Finally, produce a sketch based only on this information.

---

### Solution

#### 1. Domain

Since $x^2 + 1 \ge 1 > 0$ for all real numbers $x$, the denominator is never zero. Therefore, $f(x)$ is defined and infinitely differentiable everywhere on $\mathbb{R}$:

$$D_f = (-\infty, +\infty)$$

---

#### 2. Symmetry

Evaluate $f(-x)$:

$$f(-x) = \frac{-x}{(-x)^2 + 1} = -\frac{x}{x^2 + 1} = -f(x)$$

Because $f(-x) = -f(x)$ for all $x \in \mathbb{R}$, $f$ is an **odd function**, meaning its graph is **symmetric with respect to the origin $(0, 0)$**.

---

#### 3. Zeros, $y$-Intercept, and Sign of $f(x)$

- **Zeros ($x$-intercepts):**
  $$f(x) = 0 \iff \frac{x}{x^2 + 1} = 0 \iff x = 0$$
  The unique zero is **$x = 0$**, giving the intercept **$(0, 0)$**.
- **$y$-intercept:** $f(0) = 0$, also at **$(0, 0)$**.
- **Sign of $f(x)$:** Since $x^2 + 1 > 0$ for all $x \in \mathbb{R}$, the sign of $f(x)$ matches the sign of $x$:
  - $f(x) < 0$ on $(-\infty, 0)$,
  - $f(x) > 0$ on $(0, +\infty)$.

---

#### 4. Limits and Asymptotes

- **Vertical asymptotes:** None, because $f(x)$ is continuous on all of $(-\infty, +\infty)$.
- **Limits at infinity (horizontal asymptotes):**
  Divide numerator and denominator by $x^2$:

  $$\lim_{x \to \pm\infty} \frac{x}{x^2 + 1} = \lim_{x \to \pm\infty} \frac{\frac{1}{x}}{1 + \frac{1}{x^2}} = \frac{0}{1 + 0} = 0$$

  Thus, the $x$-axis (**$y = 0$**) is a **horizontal asymptote** on both ends:
  - As $x \to -\infty$, $f(x) \to 0^-$ (approaches $0$ from below).
  - As $x \to +\infty$, $f(x) \to 0^+$ (approaches $0$ from above).

---

#### 5. First Derivative, Monotonicity, and Extrema

Apply the Quotient Rule $\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^2}$ with $u(x) = x$ ($u'(x) = 1$) and $v(x) = x^2 + 1$ ($v'(x) = 2x$):

$$\begin{aligned} f'(x) &= \frac{(1)(x^2 + 1) - x(2x)}{(x^2 + 1)^2} \\ &= \frac{1 - x^2}{(x^2 + 1)^2} \\ &= \frac{(1 - x)(1 + x)}{(x^2 + 1)^2} \end{aligned}$$

1. **Critical Points:**
   Set $f'(x) = 0$:

   $$1 - x^2 = 0 \implies x_1 = -1, \quad x_2 = 1$$

2. **Sign Analysis of $f'(x)$ and Monotonicity:**
   Since $(x^2 + 1)^2 > 0$ for all $x \in \mathbb{R}$, the sign of $f'(x)$ is determined entirely by $1 - x^2$:

| Interval | Test Point | Sign of $(1 - x^2)$ | Sign of $f'(x)$ | Behavior of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- |
| $(-\infty, -1)$ | $x = -2$ | $-$ | **$f'(x) < 0$** | **Strictly decreasing** |
| $(-1, 1)$ | $x = 0$ | $+$ | **$f'(x) > 0$** | **Strictly increasing** |
| $(1, +\infty)$ | $x = 2$ | $-$ | **$f'(x) < 0$** | **Strictly decreasing** |

   - **$f(x)$ is strictly decreasing** on $(-\infty, -1]$ and on $[1, +\infty)$.
   - **$f(x)$ is strictly increasing** on $[-1, 1]$.

3. **Local and Global Extrema:**
   - **At $x = -1$:** $f'(x)$ changes sign from $-$ to $+$, giving a **local minimum**. Because $f(x) < 0$ on $(-\infty, 0)$ and $\lim_{x \to -\infty} f(x) = 0$, this is also the **global (absolute) minimum**:

     $$f_{\min} = f(-1) = \frac{-1}{(-1)^2 + 1} = -\frac{1}{2} \quad \text{at } \left(-1, -\frac{1}{2}\right)$$

   - **At $x = 1$:** $f'(x)$ changes sign from $+$ to $-$, giving a **local maximum**. Because $f(x) > 0$ on $(0, +\infty)$ and $\lim_{x \to +\infty} f(x) = 0$, this is also the **global (absolute) maximum**:

     $$f_{\max} = f(1) = \frac{1}{1^2 + 1} = \frac{1}{2} \quad \text{at } \left(1, \frac{1}{2}\right)$$

---

#### 6. Second Derivative, Convexity, and Inflection Points

Differentiate $f'(x) = \frac{1 - x^2}{(x^2 + 1)^2}$ using the Quotient Rule and Chain Rule:

$$\begin{aligned} f''(x) &= \frac{(-2x)(x^2 + 1)^2 - (1 - x^2) \cdot 2(x^2 + 1)(2x)}{(x^2 + 1)^4} \\ &= \frac{2x(x^2 + 1)\bigl[-(x^2 + 1) - 2(1 - x^2)\bigr]}{(x^2 + 1)^4} \\ &= \frac{2x(-x^2 - 1 - 2 + 2x^2)}{(x^2 + 1)^3} \\ &= \frac{2x(x^2 - 3)}{(x^2 + 1)^3} \\ &= \frac{2x(x + \sqrt{3})(x - \sqrt{3})}{(x^2 + 1)^3} \end{aligned}$$

1. **Candidate Inflection Points:**
   Set $f''(x) = 0$:

   $$2x(x^2 - 3) = 0 \implies x_1 = -\sqrt{3}, \quad x_2 = 0, \quad x_3 = \sqrt{3}$$

2. **Sign Analysis of $f''(x)$ and Curvature Intervals:**
   Since $(x^2 + 1)^3 > 0$ for all $x \in \mathbb{R}$, the sign of $f''(x)$ matches the sign of $2x(x^2 - 3)$:

| Interval | Test Point | Sign of $2x$ | Sign of $(x^2 - 3)$ | Sign of $f''(x)$ | Curvature of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $(-\infty, -\sqrt{3})$ | $x = -2$ | $-$ | $+$ | **$f''(x) < 0$** | **Concave (concave down)** |
| $(-\sqrt{3}, 0)$ | $x = -1$ | $-$ | $-$ | **$f''(x) > 0$** | **Convex (concave up)** |
| $(0, \sqrt{3})$ | $x = 1$ | $+$ | $-$ | **$f''(x) < 0$** | **Concave (concave down)** |
| $(\sqrt{3}, +\infty)$ | $x = 2$ | $+$ | $+$ | **$f''(x) > 0$** | **Convex (concave up)** |

   - **$f(x)$ is concave (concave down)** on $(-\infty, -\sqrt{3}]$ and on $[0, \sqrt{3}]$.
   - **$f(x)$ is convex (concave up)** on $[-\sqrt{3}, 0]$ and on $[\sqrt{3}, +\infty)$.

3. **Inflection Points:**
   Because $f''(x)$ changes sign across all three zeros ($-\sqrt{3}, 0, \sqrt{3}$), all three are **inflection points**:
   - $I_1\left(-\sqrt{3}, -\frac{\sqrt{3}}{4}\right) \approx (-1.73, -0.43)$
   - $I_2(0, 0)$ (where the tangent slope is $f'(0) = 1$)
   - $I_3\left(\sqrt{3}, \frac{\sqrt{3}}{4}\right) \approx (1.73, 0.43)$

---

#### 7. Graph Sketch Based on the Analysis

```text
                y
                ^
          1/2 --|                  * Global Max (1, 1/2)
     sqrt(3)/4 -|                 / \   * I_3 (sqrt(3), sqrt(3)/4)
                |                /   \___
  --------------+---------------*-----------------------> x (y = 0, Asymptote)
         -sqrt(3)  -1          (0,0)    1   sqrt(3)
                |          ___/  I_2
    -sqrt(3)/4 -|   I_1 * /
         -1/2 --|        * Global Min (-1, -1/2)