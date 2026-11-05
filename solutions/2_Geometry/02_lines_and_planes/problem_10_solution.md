### Exercise 10. Projection of a Point onto a Plane

Find the orthogonal projection of $P = (2, 1, 3)$ onto the plane $x + y + z = 3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

---

### Solution

#### Step 1. Construct the perpendicular line passing through $P$

The normal vector to the plane $x + y + z = 3$ is:

$$
n = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}
$$

The line $L$ passing through point $P(2, 1, 3)$ and perpendicular to the plane follows the direction of $n$:

$$
L: \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \\ 3 \end{pmatrix} + t \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}
$$

Written component-wise:

$$
\begin{cases}
x = 2 + t, \\
y = 1 + t, \\
z = 3 + t.
\end{cases}
$$

---

#### Step 2. Find the orthogonal projection $P_{\text{proj}}$

The orthogonal projection $P_{\text{proj}}$ is the intersection point of line $L$ with the plane $x + y + z = 3$.

1. **Substitute the parametric equations into the plane equation:**

$$
(2 + t) + (1 + t) + (3 + t) = 3
$$

$$
6 + 3t = 3 \implies 3t = -3 \implies t = -1
$$

2. **Compute coordinates of $P_{\text{proj}}$ using $t = -1$:**

$$
\begin{cases}
x = 2 + (-1) = 1, \\
y = 1 + (-1) = 0, \\
z = 3 + (-1) = 2.
\end{cases}
$$

Thus, the orthogonal projection is **$P_{\text{proj}} = (1, 0, 2)$**.

---

#### Step 3. Find the reflection point $P'$ across the plane

The reflection point $P'$ lies along the same line $L$ at double the parameter distance to the projection point ($t_{\text{ref}} = 2t = -2$):

$$
P' = P + 2(P_{\text{proj}} - P)
$$

Substitute $t = -2$ into the parametric equations of line $L$:

$$
\begin{cases}
x = 2 + (-2) = 0, \\
y = 1 + (-2) = -1, \\
z = 3 + (-2) = 1.
\end{cases}
$$

Thus, the reflection point is **$P' = (0, -1, 1)$**.

---

#### Step 4. Verify that the midpoint of segment $PP'$ lies on the plane

Calculate the midpoint $M$ of the line segment joining $P(2, 1, 3)$ and its reflection $P'(0, -1, 1)$:

$$
M = \left( \frac{x_P + x_{P'}}{2}, \frac{y_P + y_{P'}}{2}, \frac{z_P + z_{P'}}{2} \right) = \left( \frac{2 + 0}{2}, \frac{1 + (-1)}{2}, \frac{3 + 1}{2} \right) = (1, 0, 2)
$$

Observe that $M = P_{\text{proj}} = (1, 0, 2)$. Substitute $M(1, 0, 2)$ into the plane equation $x + y + z = 3$:

$$
1 + 0 + 2 = 3 \quad \checkmark
$$

The midpoint $M$ satisfies the plane equation, confirming both the orthogonal projection and reflection points are calculated correctly.