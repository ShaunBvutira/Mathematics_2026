### Exercise 7. A Line Relative to a Plane

Given line $L$ and plane $\Pi$:

$$
L: \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix}, \quad t \in \mathbb{R}
$$

$$
\Pi: x + y + z = 2
$$

Determine whether the line intersects the plane at one point, is parallel to it, or lies entirely within it. Explain the role of the dot product of the direction vector and the normal vector.

---

### Solution

#### Step 1. Extract vectors and compute the dot product

1. **Identify direction vector $v$ of line $L$:**
   $$
   v = \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix}
   $$

2. **Identify normal vector $n$ of plane $\Pi$:**
   Extract coefficients of $x, y, z$ from $x + y + z = 2$:
   $$
   n = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}
   $$

3. **Compute the dot product $v \cdot n$:**
   $$
   v \cdot n = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0
   $$

Since $v \cdot n = 0$, the line's direction vector $v$ is orthogonal to the plane's normal vector $n$. This means the line $L$ is **parallel to the plane** $\Pi$ (it does not cross the plane at a single point).

---

#### Step 2. Determine if $L$ lies within $\Pi$ or is strictly parallel outside $\Pi$

To check whether line $L$ lies entirely within plane $\Pi$, test if any point on $L$ satisfies the equation of $\Pi$.

Take point $P_0(1, 1, 0)$ on line $L$ (corresponding to $t = 0$) and substitute its coordinates into $\Pi: x + y + z = 2$:

$$
1 + 1 + 0 = 2 \quad \checkmark
$$

Since the point $P_0(1, 1, 0)$ satisfies the plane's equation, and the direction of the line runs parallel to the plane, **line $L$ lies entirely within plane $\Pi$**.

---

#### Step 3. Algebraic verification using parametric substitution

Substitute the parametric coordinates of $L$ ($x = 1 + t$, $y = 1 - t$, $z = 0$) directly into the plane equation $x + y + z = 2$:

$$
(1 + t) + (1 - t) + 0 = 2
$$

$$
2 + 0t = 2 \implies 2 = 2
$$

This identity holds true for **all** $t \in \mathbb{R}$, confirming that every single point on line $L$ is a point on plane $\Pi$.

---

#### Step 4. Explain the role of the dot product $v \cdot n$

The dot product $v \cdot n$ between the line's direction vector $v$ and the plane's normal vector $n$ serves as the core test for sspatial orientation:

1. **If $v \cdot n \neq 0$:** The direction vector is not perpendicular to the normal vector. The line is not parallel to the plane and must cross it at **exactly one intersection point**.
2. **If $v \cdot n = 0$:** The line direction is perpendicular to the normal vector $n$. Because $n$ is perpendicular to the plane itself, a vector perpendicular to $n$ must run parallel to the plane surface. This narrows the relative position down to two possibilities:
   - **Lies entirely within the plane:** If at least one point of the line satisfies the plane equation (infinitely many common points).
   - **Strictly parallel outside the plane:** If no point on the line satisfies the plane equation (zero common points).