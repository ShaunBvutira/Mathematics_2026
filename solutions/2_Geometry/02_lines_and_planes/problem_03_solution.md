### Exercise 3. Plane Through a Point with a Given Normal Vector

Find the equation of the plane through $P = (1, -2, 3)$ and perpendicular to $n = (2, 1, -1)^T$. Check the result by substituting the point $P$ and explain the role of the normal vector.

---

### Solution

#### Step 1. Construct the scalar equation of the plane

The standard form of a plane through a point $P(x_0, y_0, z_0)$ with normal vector $n = (A, B, C)^T$ is defined by the orthogonality condition:

$$
n \cdot \begin{pmatrix} x - x_0 \\ y - y_0 \\ z - z_0 \end{pmatrix} = 0
$$

Substitute the given point $P(1, -2, 3)$ and normal vector $n = (2, 1, -1)^T$:

$$
2(x - 1) + 1(y - (-2)) + (-1)(z - 3) = 0
$$

Expand the expression:

$$
2(x - 1) + 1(y + 2) - 1(z - 3) = 0
$$

$$
2x - 2 + y + 2 - z + 3 = 0
$$

Simplify constants:

$$
2x + y - z + 3 = 0
$$

Or in standard general form:

$$
2x + y - z = -3
$$

---

#### Step 2. Check the result by substituting point $P$

Substitute $x = 1$, $y = -2$, and $z = 3$ into $2x + y - z + 3 = 0$:

$$
\begin{aligned}
\text{LHS} &= 2(1) + (-2) - (3) + 3 \\
          &= 2 - 2 - 3 + 3 \\
          &= 0 \quad \checkmark
\end{aligned}
$$

Since the left-hand side evaluates to $0$, point $P$ lies on the plane.

---

#### Step 3. Explain the role of the normal vector

1. **Defines Orientation:** The normal vector $n = (2, 1, -1)^T$ is perpendicular to every single displacement vector that lies within the plane. It dictates the orientation of the plane in 3D space ($\mathbb{R}^3$).
2. **Coefficient Extraction:** The components of the normal vector $(A, B, C) = (2, 1, -1)$ directly become the coefficients of the variables $(x, y, z)$ in the general equation $Ax + By + Cz + D = 0$.
3. **Uniqueness:** While a single point $P$ leaves an infinite number of possible planes swiveling around it, specifying a normal vector $n$ locks the plane's spatial angle, uniquely determining a single flat surface in 3D space.