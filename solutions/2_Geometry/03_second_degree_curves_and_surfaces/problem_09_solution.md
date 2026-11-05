### Exercise 9. Ellipsoid and Its Cross-Sections

Consider the equation of the ellipsoid:

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{z^2}{16} = 1
$$

Give the semi-axis lengths, describe the cross-section $z = 0$, and explain how the cross-sections $z = c$ change for $|c| < 4$.

---

### Solution

#### Step 1. Determine the semi-axis lengths

Comparing $\frac{x^2}{9} + \frac{y^2}{4} + \frac{z^2}{16} = 1$ with the canonical equation of an ellipsoid centered at the origin:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c_z^2} = 1
$$

1. **Semi-axis along $x$ ($a$):**
   $$
   a^2 = 9 \implies a = \sqrt{9} = 3
   $$

2. **Semi-axis along $y$ ($b$):**
   $$
   b^2 = 4 \implies b = \sqrt{4} = 2
   $$

3. **Semi-axis along $z$ ($c_z$):**
   $$
   c_z^2 = 16 \implies c_z = \sqrt{16} = 4
   $$

The semi-axis lengths are $a = 3$, $b = 2$, and $c_z = 4$.

---

#### Step 2. Describe the cross-section at $z = 0$

Substitute $z = 0$ directly into the equation of the ellipsoid:

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{0^2}{16} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
$$

- **Type of Curve:** An **ellipse** in the $xy$-plane ($\mathbb{R}^2$).
- **Key Features:**
  - **Center:** $(0, 0, 0)$
  - **Semi-major axis:** $a = 3$ along the $x$-axis (vertices at $(\pm 3, 0, 0)$).
  - **Semi-minor axis:** $b = 2$ along the $y$-axis (co-vertices at $(0, \pm 2, 0)$).

This represents the maximum central horizontal cross-section (the equatorial plane slice) of the ellipsoid.

---

#### Step 3. Analyze cross-sections $z = c$ for $|c| < 4$

Substitute $z = c$ (where $-4 < c < 4$) into the original equation:

$$
\frac{x^2}{9} + \frac{y^2}{4} + \frac{c^2}{16} = 1
$$

Rearrange to isolate the $x$ and $y$ terms on the left-hand side:

$$
\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}
$$

Since $|c| < 4$, we have $c^2 < 16$, which guarantees that $1 - \frac{c^2}{16} > 0$. Divide both sides by $\left(1 - \frac{c^2}{16}\right)$ to write the equation in standard canonical form for an ellipse:

$$
\frac{x^2}{9\left(1 - \frac{c^2}{16}\right)} + \frac{y^2}{4\left(1 - \frac{c^2}{16}\right)} = 1
$$

---

#### Step 4. Geometric evolution of the cross-sections as $|c|$ changes

1. **Shape:** For every plane $z = c$ with $|c| < 4$, the cross-section is a **horizontal ellipse** parallel to the $xy$-plane.
2. **Semi-axes as Functions of $c$:**
   - Effective semi-axis along $x$: $a(c) = 3\sqrt{1 - \frac{c^2}{16}}$
   - Effective semi-axis along $y$: $b(c) = 2\sqrt{1 - \frac{c^2}{16}}$
3. **Aspect Ratio:** The ratio of the semi-axes remains constant for all cross-sections:

   $$
   \frac{a(c)}{b(c)} = \frac{3\sqrt{1 - \frac{c^2}{16}}}{2\sqrt{1 - \frac{c^2}{16}}} = \frac{3}{2}
   $$

   Thus, all cross-sectional ellipses are geometrically similar.

4. **Variation with height $|c|$:**
   - **At $c = 0$ (Equator):** The scale factor $\sqrt{1 - \frac{c^2}{16}} = 1$ is at its maximum, yielding the largest ellipse with semi-axes $3$ and $2$.
   - **As $|c|$ increases toward $4$:** The scaling factor $\sqrt{1 - \frac{c^2}{16}}$ smoothly decreases toward $0$, causing the cross-sectional ellipses to shrink symmetrically in size.
   - **At $|c| = 4$ (Poles):** The scale factor becomes $0$, and the cross-section collapses into single boundary points (the top and bottom poles at $(0, 0, 4)$ and $(0, 0, -4)$).