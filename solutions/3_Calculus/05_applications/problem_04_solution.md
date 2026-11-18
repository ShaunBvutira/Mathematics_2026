### Problem 4. Area Between Curves

#### Question

Find the area of the region bounded by the graphs

$$y = x$$

and

$$y = x^2.$$

First find the intersection points and justify which function is greater on the relevant interval.

---

### Solution

#### Step 1. Find the Intersection Points of the Two Curves

To locate the points where the line $y = x$ and the parabola $y = x^2$ meet, set their $y$-values equal to each other:

$$\begin{aligned} x^2 &= x \\ x^2 - x &= 0 \\ x(x - 1) &= 0 \end{aligned}$$

This gives two $x$-coordinates:

$$x_1 = 0 \qquad \text{and} \qquad x_2 = 1$$

Substitute both values back into $y = x$ (or $y = x^2$) to obtain the full coordinates of the intersection points:
- At $x = 0$: $y = 0 \implies (0, 0)$
- At $x = 1$: $y = 1 \implies (1, 1)$

Thus, the bounded region lies over the closed interval **$[0, 1]$**.

---

#### Step 2. Justify Which Function Is Greater on $[0, 1]$

Compare $f(x) = x$ and $g(x) = x^2$ on the interior of the interval $(0, 1)$:

1. **Algebraic Comparison:**
   For every $x \in (0, 1)$, both $x > 0$ and $1 - x > 0$. Their difference is:

   $$x - x^2 = x(1 - x) > 0 \implies x > x^2 \qquad \text{for all } x \in (0, 1)$$

   *(Equivalently, multiplying both sides of $0 < x < 1$ by the positive number $x$ preserves the inequality and yields $x^2 < x$.)*

2. **Test-Point Verification:**
   Because the two continuous curves intersect only at $x = 0$ and $x = 1$, their relative order cannot switch inside $(0, 1)$. Evaluating at $x = \frac{1}{2} \in (0, 1)$ confirms:

   $$y_{\text{line}}\!\left(\frac{1}{2}\right) = \frac{1}{2} = 0.50 > y_{\text{parabola}}\!\left(\frac{1}{2}\right) = \left(\frac{1}{2}\right)^2 = \frac{1}{4} = 0.25$$

Therefore, on the interval $[0, 1]$:
- **Upper curve:** $y_{\text{top}} = x$
- **Lower curve:** $y_{\text{bottom}} = x^2$

```text
      y
      ^
    1 |         * (1, 1)
      |       / |
      |      /  |  <-- y = x (upper curve)
  1/2 |     / . |
      |    / .  |  <-- y = x^2 (lower curve)
  ----+---*-----+----------> x
      | (0,0)   1