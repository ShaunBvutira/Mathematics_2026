### Exercise 4. Parabola

For the equation

$$
y^2 = 12x,
$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x = 3$ and use them to make a sketch.

---

### Solution

#### Step 1. Identify the key structural features

Compare $y^2 = 12x$ with the canonical equation of a horizontal parabola $y^2 = 4px$:

1. **Vertex:**
   There are no translation terms in $(y - k)^2 = 4p(x - h)$, so the vertex sits at the origin:

   $$
   V = (0, 0)
   $$

2. **Focal Parameter ($p$), Focus, and Directrix:**

   $$
   4p = 12 \implies p = 3
   $$

   - **Focus:** $F = (p, 0) = (3, 0)$
   - **Directrix:** $x = -p \implies x = -3$

3. **Axis of Symmetry:**
   Because $y$ appears only as $y^2$, replacing $y$ with $-y$ leaves the equation unchanged. Therefore, the parabola is symmetric across the horizontal **$x$-axis** ($y = 0$).

4. **Opening Direction:**
   Since $y^2 \ge 0$ for all real $y$, we must have $12x \ge 0 \implies x \ge 0$. With $p = 3 > 0$, the parabola opens to the **right** along the positive $x$-axis.

---

#### Step 2. Find points on the parabola for $x = 3$

Substitute $x = 3$ into $y^2 = 12x$:

$$
y^2 = 12(3) = 36
$$

Take the square root of both sides:

$$
y = \pm\sqrt{36} = \pm 6
$$

This yields two symmetric guide points on the parabola at $x = 3$:

$$
P_1 = (3, 6), \quad P_2 = (3, -6)
$$

*(Note: The vertical chord connecting $P_1(3, 6)$ and $P_2(3, -6)$ passes directly through the focus $F(3, 0)$ and has total length $|4p| = 12$, known as the latus rectum.)*

---

#### Step 3. Additional helper points for accuracy

Evaluate at $x = \frac{1}{3}$ (i.e., $x = 1/3$) to capture the curvature near the vertex:

$$
y^2 = 12\left(\frac{1}{3}\right) = 4 \implies y = \pm 2 \implies \left(\frac{1}{3}, 2\right), \quad \left(\frac{1}{3}, -2\right)
$$

---

#### Step 4. Sketch and geometric layout

To draw the sketch on the Cartesian plane:
- **Vertex:** Plot the turning point at the origin $V(0, 0)$.
- **Guide Points:** Plot $P_1(3, 6)$ in Quadrant I and $P_2(3, -6)$ in Quadrant IV, along with $\left(\frac{1}{3}, 2\right)$ and $\left(\frac{1}{3}, -2\right)$ closer to the origin.
- **Focus & Directrix:** Mark the focus at $F(3, 0)$ on the positive $x$-axis (halfway between $P_1$ and $P_2$) and draw a dashed vertical line at $x = -3$ behind the vertex.
- **Curve:** Draw a smooth, U-shaped curve starting at $V(0, 0)$, symmetric about the $x$-axis, opening rightward through $(3, 6)$ and $(3, -6)$, and widening indefinitely as $x \to +\infty$.