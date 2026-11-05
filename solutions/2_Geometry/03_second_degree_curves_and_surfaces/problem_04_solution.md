### Exercise 4. Parabola

For the equation

$$
y^2 = 12x
$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x = 3$ and use them to make a sketch.

---

### Solution

#### Step 1. Identify the key structural features

Comparing $y^2 = 12x$ with the standard canonical form of a horizontal parabola $y^2 = 4px$:

1. **Vertex:** 
   The equation has no shift terms $(y - k)^2 = 4p(x - h)$, so the vertex is at the origin:

   $$
   V = (0, 0)
   $$

2. **Focal Parameter ($p$):**
   $$
   4p = 12 \implies p = 3
   $$
   - **Focus:** $F = (p, 0) = (3, 0)$
   - **Directrix:** $x = -p \implies x = -3$

3. **Axis of Symmetry:** 
   Because $y$ is squared, the parabola is symmetric with respect to replacing $y$ with $-y$. The axis of symmetry is the horizontal **$x$-axis** ($y = 0$).

4. **Opening Direction:** 
   Since $4p = 12 > 0$ and $x = \frac{y^2}{12} \ge 0$, $x$ takes non-negative values. Thus, the parabola opens to the **right** (along the positive $x$-axis).

---

#### Step 2. Calculate points for $x = 3$

Substitute $x = 3$ into $y^2 = 12x$:

$$
y^2 = 12(3) = 36
$$

Solve for $y$:

$$
y = \pm\sqrt{36} = \pm 6
$$

This gives two symmetric reference points at $x = 3$:

$$
P_1 = (3, 6), \quad P_2 = (3, -6)
$$

*(Note: The segment connecting $(3, 6)$ and $(3, -6)$ passes directly through the focus $(3, 0)$ and represents the focal focal width/latus rectum, which has length $|4p| = 12$.)*

---

#### Step 3. Additional Reference Points

To ensure an accurate curve, evaluate for $x = 13$:

$$
y^2 = 12\left(\frac{1}{3}\right) = 4 \implies y = \pm 2 \implies \left(\frac{1}{3}, 2\right), \left(\frac{1}{3}, -2\right)
$$

---

#### Step 4. Sketch / Visual Description

- **Vertex:** Place the vertex point at $(0, 0)$.
- **Key Guide Points:** Plot $(3, 6)$ in the first quadrant and $(3, -6)$ in the fourth quadrant.
- **Focus & Directrix:** Mark the focus at $(3, 0)$ on the $x$-axis inside the curve, and draw a vertical dashed line at $x = -3$ behind the vertex.
- **Curve:** Draw a smooth, symmetrical U-shaped curve that turns at $(0,0)$, opens to the right around the $x$-axis, passes through $(3, 6)$ and $(3, -6)$, and expands outward as $x \to +\infty$.