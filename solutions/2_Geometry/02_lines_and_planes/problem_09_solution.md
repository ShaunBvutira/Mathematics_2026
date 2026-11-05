### Exercise 9. Distances

Compute:

1. The distance from $P = (2, 3)$ to the line $3x + 4y - 10 = 0$.
2. The distance from $Q = (2, -1, 3)$ to the plane $2x - 2y + z - 4 = 0$.

Compare the two formulas and explain their common connection with the normal direction.

---

### Solution

#### Step 1. Compute the distance from point $P(2, 3)$ to the line $3x + 4y - 10 = 0$

The formula for the perpendicular distance $d$ from a point $(x_0, y_0)$ to a line $Ax + By + C = 0$ in $\mathbb{R}^2$ is:

$$
d = \frac{|A x_0 + B y_0 + C|}{\sqrt{A^2 + B^2}}
$$

1. **Identify components:**
   - Point: $(x_0, y_0) = (2, 3)$
   - Line coefficients: $A = 3$, $B = 4$, $C = -10$

2. **Substitute into distance formula:**

$$
\begin{aligned}
d &= \frac{|3(2) + 4(3) - 10|}{\sqrt{3^2 + 4^2}} \\
  &= \frac{|6 + 12 - 10|}{\sqrt{9 + 16}} \\
  &= \frac{|8|}{\sqrt{25}} \\
  &= \frac{8}{5} = 1.6
\end{aligned}
$$

---

#### Step 2. Compute the distance from point $Q(2, -1, 3)$ to the plane $2x - 2y + z - 4 = 0$

The formula for the perpendicular distance $d$ from a point $(x_0, y_0, z_0)$ to a plane $Ax + By + Cz + D = 0$ in $\mathbb{R}^3$ is:

$$
d = \frac{|A x_0 + B y_0 + C z_0 + D|}{\sqrt{A^2 + B^2 + C^2}}
$$

1. **Identify components:**
   - Point: $(x_0, y_0, z_0) = (2, -1, 3)$
   - Plane coefficients: $A = 2$, $B = -2$, $C = 1$, $D = -4$

2. **Substitute into distance formula:**

$$
\begin{aligned}
d &= \frac{|2(2) + (-2)(-1) + 1(3) - 4|}{\sqrt{2^2 + (-2)^2 + 1^2}} \\
  &= \frac{|4 + 2 + 3 - 4|}{\sqrt{4 + 4 + 1}} \\
  &= \frac{|5|}{\sqrt{9}} \\
  &= \frac{5}{3} \approx 1.667
\end{aligned}
$$

---

#### Step 3. Compare formulas and explain their common connection with the normal direction

1. **Structural Comparison:**
   - **Line in $\mathbb{R}^2$:** $d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$
   - **Plane in $\mathbb{R}^3$:** $d = \frac{|Ax_0 + By_0 + Cz_0 + D|}{\sqrt{A^2 + B^2 + C^2}}$

   Both formulas take the general implicit equation evaluated at the target point in the numerator, divided by the norm (length) of the corresponding normal vector in the denominator.

2. **Connection with the Normal Direction:**
   - **Projection onto Normal Vector:** The shortest distance from a point to a line or plane is measured along the line perpendicular to that surface—which is precisely the direction of the normal vector $n$ ($n = (A, B)^T$ in 2D, $n = (A, B, C)^T$ in 3D).
   - **Scalar Projection Derivation:** If $P_0$ is any point lying on the line/plane and $X$ is the external point, the displacement vector is $v = X - P_0$. The perpendicular distance is the magnitude of the scalar projection of $v$ onto the unit normal vector $e = \frac{n}{\|n\|}$:

$$
d = |v \cdot e| = \frac{|(X - P_0) \cdot n|}{\|n\|} = \frac{|Ax_0 + By_0 + \dots + D|}{\|n\|}
$$

Thus, both formulas are identical scalar projection calculations onto the unit normal vector of the hyperplane.