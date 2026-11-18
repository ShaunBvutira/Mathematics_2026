### Problem 6. Average Value of a Function

#### Question

Compute the average value of the function

$$f(x) = x^2$$

on the interval $[0, 3]$.

Find a point $c \in [0, 3]$ for which $f(c)$ is equal to this average value, and interpret the result geometrically.

---

### Solution

#### Step 1. Compute the Average Value of $f(x) = x^2$ on $[0, 3]$

The average value $f_{\text{avg}}$ of a continuous function $f$ on a closed interval $[a, b]$ is defined by:

$$f_{\text{avg}} = \frac{1}{b - a} \int_{a}^{b} f(x) \, dx$$

Substitute $f(x) = x^2$, $a = 0$, and $b = 3$:

$$\begin{aligned} f_{\text{avg}} &= \frac{1}{3 - 0} \int_{0}^{3} x^2 \, dx \\ &= \frac{1}{3} \left[ \frac{x^3}{3} \right]_{0}^{3} \\ &= \frac{1}{3} \left( \frac{3^3}{3} - \frac{0^3}{3} \right) \\ &= \frac{1}{3} \left( \frac{27}{3} - 0 \right) \\ &= \frac{1}{3} \cdot 9 \\ &= 3 \end{aligned}$$

Thus, the average value of $f(x) = x^2$ on $[0, 3]$ is **$3$**.

---

#### Step 2. Find a Point $c \in [0, 3]$ Such That $f(c) = f_{\text{avg}}$

By the **Mean Value Theorem for Integrals**, because $f(x) = x^2$ is continuous on $[0, 3]$, there exists at least one number $c \in [0, 3]$ where the function attains its average value:

$$\begin{aligned} f(c) &= f_{\text{avg}} \\ c^2 &= 3 \\ c &= \pm\sqrt{3} \end{aligned}$$

Check which solution lies inside the interval $[0, 3]$:
- $c_1 = -\sqrt{3} \approx -1.732 \notin [0, 3]$ (rejected, outside the interval).
- $c_2 = \sqrt{3} \approx 1.732 \in [0, 3]$ (valid, since $1 < \sqrt{3} < 2 < 3$).

Therefore, the unique point in $[0, 3]$ is:

$$c = \sqrt{3} \approx 1.732$$

---

#### Step 3. Geometric Interpretation

1. **Equal-Area Rectangle:**
   The definite integral $\int_{0}^{3} x^2 \, dx = 9$ represents the area of the curved region bounded above by the parabola $y = x^2$, below by the $x$-axis, and on the sides by $x = 0$ and $x = 3$.
   - Constructing a rectangle over the same base $[0, 3]$ (width $3 - 0 = 3$) with constant height $f_{\text{avg}} = 3$ produces a rectangle of area:

     $$A_{\text{rect}} = \text{width} \times \text{height} = 3 \times 3 = 9$$

   - Geometrically, the average value $f_{\text{avg}} = 3$ is the exact height needed to "level out" the curved region under $y = x^2$ into a rectangle of the **same base and identical area ($9$)**.

2. **Area Balance Across $y = 3$:**
   The horizontal line $y = 3$ intersects the parabola $y = x^2$ precisely at the point $(\sqrt{3}, 3)$:
   - On $[0, \sqrt{3})$, the parabola lies **below** the line $y = 3$, leaving a deficit area between $y = 3$ and $y = x^2$.
   - On $(\sqrt{3}, 3]$, the parabola rises **above** the line $y = 3$, creating an excess area above $y = 3$.
   - Because $3$ is the average height, the excess area on $[\sqrt{3}, 3]$ exactly fills in the deficit area on $[0, \sqrt{3}]$.

```text
      y
      ^
    9 |                   * (3, 9)
      |                  / |
      |                 /  |  <-- Excess area above y = 3
    3 |----------------+---*  (y = f_avg = 3)
      |   Deficit --> / .  |
      |     area     /  .  |
  ----+-------------*---+---------> x
      0          sqrt(3)   3