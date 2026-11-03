### Exercise 2. Distance as the Length of a Vector

Given points $A = (1, 2, 3)$ and $B = (4, -2, 6)$.

1. Construct $\vec{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate distance formula.
4. Explain why both calculations give the same result.

---

### Solution

#### Step 1. Construct $\vec{AB}$

The displacement vector $\vec{AB}$ from point $A$ to point $B$ is found by subtracting the coordinates of the initial point $A$ from the terminal point $B$:

$$
\begin{aligned}
\vec{AB} &= B - A \\
        &= 
\begin{pmatrix}
4 - 1 \\
-2 - 2 \\
6 - 3 \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
3 \\
-4 \\
3 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute the length of $\vec{AB}$

The length (norm or magnitude) of a vector $v = (v_1, v_2, v_3)^T$ is calculated using:

$$
\|\vec{AB}\| = \sqrt{v_1^2 + v_2^2 + v_3^2}
$$

Substituting the components of $\vec{AB} = (3, -4, 3)^T$:

$$
\begin{aligned}
\|\vec{AB}\| &= \sqrt{3^2 + (-4)^2 + 3^2} \\
             &= \sqrt{9 + 16 + 9} \\
             &= \sqrt{34}
\end{aligned}
$$

---

#### Step 3. Compute the distance between $A$ and $B$ using the coordinate formula

The distance $d(A, B)$ between points $A(x_1, y_1, z_1)$ and $B(x_2, y_2, z_2)$ in $\mathbb{R}^3$ is given by the Euclidean distance formula:

$$
d(A, B) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}
$$

Substituting the coordinates of $A(1, 2, 3)$ and $B(4, -2, 6)$:

$$
\begin{aligned}
d(A, B) &= \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} \\
        &= \sqrt{(3)^2 + (-4)^2 + (3)^2} \\
        &= \sqrt{9 + 16 + 9} \\
        &= \sqrt{34}
\end{aligned}
$$

---

#### Step 4. Explain why both calculations give the same result

Both calculations yield the exact same value ($\sqrt{34}$) because they represent the exact same geometric property:

1. **Equivalence of Terms:** The vector $\vec{AB}$ holds the directional differences along each coordinate axis: $\Delta x = x_2 - x_1$, $\Delta y = y_2 - y_1$, and $\Delta z = z_2 - z_1$.
2. **Pythagorean Theorem:** The Euclidean distance formula is simply the 3D Pythagorean theorem applied to point coordinates. The magnitude of a vector $\|\vec{AB}\|$ is also the 3D Pythagorean theorem applied to the vector's components $(\Delta x, \Delta y, \Delta z)$.

Thus, the geometric distance between two points in Euclidean space is defined precisely as the length of the displacement vector connecting them: $d(A, B) = \|\vec{AB}\|$.