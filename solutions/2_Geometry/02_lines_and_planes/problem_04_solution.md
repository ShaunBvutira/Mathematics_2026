### Exercise 4. Plane Through Three Points

Find the equation of the plane through $A = (1, 0, 0)$, $B = (0, 1, 0)$, and $C = (0, 0, 1)$. First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

---

### Solution

#### Step 1. Construct two vectors lying in the plane

Find displacement vectors $\vec{AB}$ and $\vec{AC}$ using the given points:

$$
\vec{AB} = B - A = 
\begin{pmatrix}
0 - 1 \\
1 - 0 \\
0 - 0 \\
\end{pmatrix}
=
\begin{pmatrix}
-1 \\
1 \\
0 \\
\end{pmatrix}
$$

$$
\vec{AC} = C - A = 
\begin{pmatrix}
0 - 1 \\
0 - 0 \\
1 - 0 \\
\end{pmatrix}
=
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix}
$$

---

#### Step 2. Compute a normal vector using the cross product

The normal vector $n$ to the plane is perpendicular to both $\vec{AB}$ and $\vec{AC}$, which is given by their cross product $\vec{AB} \times \vec{AC}$:

$$
n = \vec{AB} \times \vec{AC} = 
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
-1 & 1 & 0 \\
-1 & 0 & 1 \\
\end{vmatrix}
$$

Expanding along the first row:

$$
\begin{aligned}
n &= \hat{i} \begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix} - \hat{j} \begin{vmatrix} -1 & 0 \\ -1 & 1 \end{vmatrix} + \hat{k} \begin{vmatrix} -1 & 1 \\ -1 & 0 \end{vmatrix} \\
  &= \hat{i}(1 - 0) - \hat{j}(-1 - 0) + \hat{k}(0 - (-1)) \\
  &= 1\hat{i} + 1\hat{j} + 1\hat{k}
\end{aligned}
$$

Thus, the normal vector is:

$$
n = 
\begin{pmatrix}
1 \\
1 \\
1 \\
\end{pmatrix}
$$

---

#### Step 3. Construct the general equation of the plane

Using the normal vector $n = (1, 1, 1)^T$ and point $A(1, 0, 0)$ in $n \cdot (r - A) = 0$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0
$$

$$
x - 1 + y + z = 0
$$

Rearranging into standard general form:

$$
x + y + z = 1
$$

---

#### Step 4. Check the equation on all three points

Substitute the coordinates of $A$, $B$, and $C$ into $x + y + z = 1$:

1. **Check Point $A(1, 0, 0)$:**
   $$
   1 + 0 + 0 = 1 \quad \checkmark
   $$

2. **Check Point $B(0, 1, 0)$:**
   $$
   0 + 1 + 0 = 1 \quad \checkmark
   $$

3. **Check Point $C(0, 0, 1)$:**
   $$
   0 + 0 + 1 = 1 \quad \checkmark
   $$

All three points satisfy the equation, confirming that $x + y + z = 1$ is the correct plane equation.