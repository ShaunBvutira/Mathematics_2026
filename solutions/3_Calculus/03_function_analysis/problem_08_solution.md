### Problem 8. The Second Derivative

#### Question

For

$$f(x) = x^4 - 4x^2$$

find the local extrema, intervals of convexity and concavity, and inflection points. Sketch the graph and mark all the identified features on it.

---

### Solution

#### Step 1. Domain, Symmetry, and Intercepts

- **Domain:** Since $f(x) = x^4 - 4x^2$ is a polynomial, it is defined and infinitely differentiable everywhere on $\mathbb{R} = (-\infty, +\infty)$.
- **Symmetry:** Since $f(-x) = (-x)^4 - 4(-x)^2 = x^4 - 4x^2 = f(x)$, the function is **even**, meaning its graph is symmetric about the $y$-axis.
- **Intercepts:**
  - **$y$-intercept:** $f(0) = 0 \implies (0, 0)$.
  - **$x$-intercepts (zeros):** Factor $f(x) = x^2(x^2 - 4) = x^2(x + 2)(x - 2) = 0$, giving:

    $$x = -2 \implies (-2, 0), \qquad x = 0 \implies (0, 0) \text{ (double root)}, \qquad x = 2 \implies (2, 0)$$

---

#### Step 2. First Derivative and Local Extrema

Compute the first derivative $f'(x)$ and factor it completely:

$$\begin{aligned} f'(x) &= \frac{d}{dx}(x^4 - 4x^2) \\ &= 4x^3 - 8x \\ &= 4x(x^2 - 2) \\ &= 4x(x + \sqrt{2})(x - \sqrt{2}) \end{aligned}$$

1. **Critical Points:**
   Set $f'(x) = 0$:

   $$4x(x^2 - 2) = 0 \implies x_1 = -\sqrt{2}, \quad x_2 = 0, \quad x_3 = \sqrt{2}$$

2. **Compute the Second Derivative $f''(x)$:**

   $$\begin{aligned} f''(x) &= \frac{d}{dx}(4x^3 - 8x) \\ &= 12x^2 - 8 \\ &= 4(3x^2 - 2) \end{aligned}$$

3. **Classify the Critical Points via the Second Derivative Test:**
   - **At $x = -\sqrt{2}$:**
     $$f''(-\sqrt{2}) = 12(-\sqrt{2})^2 - 8 = 24 - 8 = 16 > 0 \implies \text{Local minimum}$$
     $$f(-\sqrt{2}) = (-\sqrt{2})^4 - 4(-\sqrt{2})^2 = 4 - 8 = -4 \implies \text{Point } (-\sqrt{2}, -4)$$
   - **At $x = 0$:**
     $$f''(0) = 12(0)^2 - 8 = -8 < 0 \implies \text{Local maximum}$$
     $$f(0) = 0^4 - 4(0)^2 = 0 \implies \text{Point } (0, 0)$$
   - **At $x = \sqrt{2}$:**
     $$f''(\sqrt{2}) = 12(\sqrt{2})^2 - 8 = 24 - 8 = 16 > 0 \implies \text{Local minimum}$$
     $$f(\sqrt{2}) = (\sqrt{2})^4 - 4(\sqrt{2})^2 = 4 - 8 = -4 \implies \text{Point } (\sqrt{2}, -4)$$

   *(Since $\lim_{x \to \pm\infty} f(x) = +\infty$, both local minima $(-\sqrt{2}, -4)$ and $(\sqrt{2}, -4)$ are also **global minima** with minimum value $-4$.)*

---

#### Step 3. Intervals of Convexity and Concavity, and Inflection Points

Set the second derivative $f''(x) = 4(3x^2 - 2)$ equal to zero to find candidate inflection points:

$$\begin{aligned} 4(3x^2 - 2) &= 0 \\ 3x^2 &= 2 \\ x^2 &= \frac{2}{3} \implies x = \pm\sqrt{\frac{2}{3}} = \pm\frac{\sqrt{6}}{3} \approx \pm 0.816 \end{aligned}$$

The points $x = -\frac{\sqrt{6}}{3}$ and $x = \frac{\sqrt{6}}{3}$ divide $(-\infty, +\infty)$ into three open intervals. Test the sign of $f''(x) = 12x^2 - 8$ on each interval:

| Interval | Test Point | Value of $f''(x) = 12x^2 - 8$ | Sign of $f''(x)$ | Curvature of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- |
| $\left(-\infty, -\frac{\sqrt{6}}{3}\right)$ | $x = -1$ | $12(-1)^2 - 8 = +4$ | **$f''(x) > 0$** | **Convex (concave up)** |
| $\left(-\frac{\sqrt{6}}{3}, \frac{\sqrt{6}}{3}\right)$ | $x = 0$ | $12(0)^2 - 8 = -8$ | **$f''(x) < 0$** | **Concave (concave down)** |
| $\left(\frac{\sqrt{6}}{3}, +\infty\right)$ | $x = 1$ | $12(1)^2 - 8 = +4$ | **$f''(x) > 0$** | **Convex (concave up)** |

**Summary of Convexity / Concavity:**
- **$f(x)$ is convex (concave up)** on $\left(-\infty, -\frac{\sqrt{6}}{3}\right]$ and on $\left[\frac{\sqrt{6}}{3}, +\infty\right)$.
- **$f(x)$ is concave (concave down)** on $\left[-\frac{\sqrt{6}}{3}, \frac{\sqrt{6}}{3}\right]$.

**Inflection Points:**
Because $f''(x)$ changes sign across both $x = -\frac{\sqrt{6}}{3}$ and $x = \frac{\sqrt{6}}{3}$, both points are genuine **inflection points**. Evaluate their common $y$-coordinate:

$$f\!\left(\pm\sqrt{\frac{2}{3}}\right) = \left(\frac{2}{3}\right)^2 - 4\left(\frac{2}{3}\right) = \frac{4}{9} - \frac{8}{3} = \frac{4 - 24}{9} = -\frac{20}{9} \approx -2.22$$

Thus, the two **inflection points** are:

$$I_1\left(-\frac{\sqrt{6}}{3}, -\frac{20}{9}\right) \qquad \text{and} \qquad I_2\left(\frac{\sqrt{6}}{3}, -\frac{20}{9}\right)$$

---

#### Step 4. Graph Sketch with All Marked Features

```text
           y
           ^
         2 |
         1 |
  ---------+---*-----------------*-----------------*-------> x
          -3  (-2,0)           (0,0)             (2,0)    3
        -1 |    \          Local Max            /
           |     \          /     \            /
     -20/9 |      \   I_1  *       *  I_2     /
        -3 |       \      /         \        /
        -4 |        *----'           '------*
               (-sqrt(2), -4)          (sqrt(2), -4)
                 Global Min              Global Min