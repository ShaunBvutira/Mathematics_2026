### Exercise 10. Triangle Area from Vectors

Given points $A = (0, 0, 0)$, $B = (2, 1, 0)$, and $C = (1, 3, 2)$:

1. Construct the displacement vectors $\vec{AB}$ and $\vec{AC}$.
2. Compute the area of the parallelogram spanned by $\vec{AB}$ and $\vec{AC}$ using the cross product.
3. Find the area of triangle $ABC$.
4. Explain the factor $\frac{1}{2}$ geometrically.

---

### Solution

#### Step 1. Construct $\vec{AB}$ and $\vec{AC}$

Subtract the coordinates of the initial point $A(0, 0, 0)$ from $B$ and $C$:

$$
\vec{AB} = B - A = 
\begin{pmatrix} 2 - 0 \\ 1 - 0 \\ 0 - 0 \end{pmatrix} = 
\begin{pmatrix} 2 \\ 1 \\ 0 \end{pmatrix}
$$

$$
\vec{AC} = C - A = 
\begin{pmatrix} 1 - 0 \\ 3 - 0 \\ 2 - 0 \end{pmatrix} = 
\begin{pmatrix} 1 \\ 3 \\ 2 \end{pmatrix}
$$

---

#### Step 2. Compute the cross product $\vec{AB} \times \vec{AC}$ and the parallelogram area

Calculate the cross product using the determinant of the matrix:

$$
\vec{AB} \times \vec{AC} = 
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
2 & 1 & 0 \\
1 & 3 & 2 \\
\end{vmatrix}
$$

Expanding along the first row:

$$
\begin{aligned}
\vec{AB} \times \vec{AC} &= \hat{i} \begin{vmatrix} 1 & 0 \\ 3 & 2 \end{vmatrix} - \hat{j} \begin{vmatrix} 2 & 0 \\ 1 & 2 \end{vmatrix} + \hat{k} \begin{vmatrix} 2 & 1 \\ 1 & 3 \end{vmatrix} \\
&= \hat{i}(1 \cdot 2 - 0 \cdot 3) - \hat{j}(2 \cdot 2 - 0 \cdot 1) + \hat{k}(2 \cdot 3 - 1 \cdot 1) \\
&= 2\hat{i} - 4\hat{j} + 5\hat{k} = \begin{pmatrix} 2 \\ -4 \\ 5 \end{pmatrix}
\end{aligned}
$$

The magnitude (length) of the cross product gives the area of the parallelogram spanned by $\vec{AB}$ and $\vec{AC}$:

$$
\begin{aligned}
\text{Area}_{\text{parallelogram}} &= \|\vec{AB} \times \vec{AC}\| \\
&= \sqrt{2^2 + (-4)^2 + 5^2} \\
&= \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5} \approx 6.708
\end{aligned}
$$

---

#### Step 3. Find the area of triangle $ABC$

The area of the triangle formed by $A$, $B$, and $C$ is half the area of the parallelogram:

$$
\text{Area}_{\text{triangle}} = \frac{1}{2} \|\vec{AB} \times \vec{AC}\| = \frac{\sqrt{45}}{2} = \frac{3\sqrt{5}}{2} \approx 3.354
$$

---

#### Step 4. Explain the factor $\frac{1}{2}$ geometrically

1. **Parallelogram Spanned by Vectors:** The cross product magnitude $\|\vec{AB} \times \vec{AC}\|$ measures the full area of the four-sided parallelogram formed by placing a duplicate of $\vec{AC}$ at the tip of $\vec{AB}$ and a duplicate of $\vec{AB}$ at the tip of $\vec{AC}$.
2. **Division into Congruent Triangles:** The diagonal segment $BC$ (or vector connecting $B$ and $C$) splits this entire parallelogram directly into two congruent, non-overlapping triangles of identical area.
3. **Half Area:** Because triangle $ABC$ makes up exactly one of these two identical halves, its area is precisely $\frac{1}{2}$ of the area of the full parallelogram.