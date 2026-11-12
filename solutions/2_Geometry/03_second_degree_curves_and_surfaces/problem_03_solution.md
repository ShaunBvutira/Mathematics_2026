### Exercise 3. Ellipse

For the equation

$$
\frac{x^2}{25} + \frac{y^2}{9} = 1,
$$

find the semi-axis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

---

### Solution

#### Step 1. Determine the semi-axis lengths

Compare $\frac{x^2}{25} + \frac{y^2}{9} = 1$ with the canonical equation of an ellipse centered at the origin:

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

1. **Horizontal semi-axis ($a$):**
   $$
   a^2 = 25 \implies a = \sqrt{25} = 5
   $$

2. **Vertical semi-axis ($b$):**
   $$
   b^2 = 9 \implies b = \sqrt{9} = 3
   $$

The semi-major axis length is **$5$** and the semi-minor axis length is **$3$**.

---

#### Step 2. Find the intercepts with the coordinate axes

1. **$x$-intercepts (set $y = 0$):**
   $$
   \frac{x^2}{25} + \frac{0^2}{9} = 1 \implies x^2 = 25 \implies x = \pm 5
   $$
   The $x$-intercepts (vertices) are **$(5, 0)$** and **$(-5, 0)$**.

2. **$y$-intercepts (set $x = 0$):**
   $$
   \frac{0^2}{25} + \frac{y^2}{9} = 1 \implies y^2 = 9 \implies y = \pm 3
   $$
   The $y$-intercepts (co-vertices) are **$(0, 3)$** and **$(0, -3)$**.

---

#### Step 3. Focal distance and foci

Compute the focal distance $c$ using $c^2 = a^2 - b^2$:

$$
c = \sqrt{25 - 9} = \sqrt{16} = 4
$$

The foci lie along the major $x$-axis at **$F_1(-4, 0)$** and **$F_2(4, 0)$**.

---

#### Step 4. Sketch and geometric layout

To draw the sketch on the Cartesian plane:
- **Center:** Plot the center at the origin $(0, 0)$.
- **Vertices and Co-vertices:** Plot the horizontal endpoints at $(-5, 0)$ and $(5, 0)$, and the vertical endpoints at $(0, -3)$ and $(0, 3)$.
- **Foci:** Mark the two focal points on the horizontal axis at $(-4, 0)$ and $(4, 0)$.
- **Curve:** Connect the four intercepts with a smooth, symmetrical oval that has a total horizontal width of $2a = 10$ units and a total vertical height of $2b = 6$ units.

---

#### Step 5. Axis stretching explanation

- **Axis of greater stretch:** The ellipse is more stretched along the **$x$-axis** (horizontally).
- **How this is visible in the equation:**
  In the canonical equation $\frac{x^2}{25} + \frac{y^2}{9} = 1$, the denominator beneath $x^2$ ($25$) is larger than the denominator beneath $y^2$ ($9$). Because $x$ is divided by a larger number, $x$ can reach larger magnitudes ($\pm\sqrt{25} = \pm 5$) than $y$ ($\pm\sqrt{9} = \pm 3$) while keeping the sum equal to $1$. In general, the variable with the larger denominator in the canonical equation gives the longer semi-axis ($a = \sqrt{25} = 5 > b = \sqrt{9} = 3$), directly identifying the direction of the major axis.