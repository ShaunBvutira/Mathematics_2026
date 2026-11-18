### Problem 9. Definite Integral and Geometric Area

#### Question

Computes

$$\int_{-1}^{2} x \, dx.$$

Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

---

### Solution

#### Step 1. Compute the Definite Integral $\int_{-1}^{2} x \, dx$

Find an antiderivative of $f(x) = x$:

$$F(x) = \int x \, dx = \frac{x^2}{2}$$

Apply the Fundamental Theorem of Calculus (Newton–Leibniz formula) $\int_{a}^{b} f(x) \, dx = F(b) - F(a)$ over $[-1, 2]$:

$$\begin{aligned} \int_{-1}^{2} x \, dx &= \left[ \frac{x^2}{2} \right]_{-1}^{2} \\ &= \frac{2^2}{2} - \frac{(-1)^2}{2} \\ &= \frac{4}{2} - \frac{1}{2} \\ &= \frac{3}{2} = 1.5 \end{aligned}$$

Thus, the value of the definite integral is **$\frac{3}{2}$**.

---

#### Step 2. Split the Interval at the Zero of $f(x)$

Examine the sign of $f(x) = x$ on $[-1, 2]$:
- The zero occurs at $x = 0$.
- **On $[-1, 0)$:** $f(x) = x < 0$, so the graph lies **below** the $x$-axis.
- **On $(0, 2]$:** $f(x) = x > 0$, so the graph lies **above** the $x$-axis.

```text
          y
          ^
        2 |         /|
          |        / |
        1 |       /  |  A_above = 2
          |      /   |  (above x-axis)
  --------+-----*----+------------> x
       -1 |    /0    2
       -1 |   /
          |--/   A_below = 1/2
          |      (below x-axis)