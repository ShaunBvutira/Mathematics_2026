### Exercise 6. Projection and Perpendicular Component

Given $u = (4, 2)^T$ and $v = (1, 1)^T$:

1. Find the projection of $u$ onto $v$ ($\mathrm{proj}_v u$).
2. Compute the residual vector $r = u - \mathrm{proj}_v u$.
3. Verify that $r \cdot v = 0$ and explain the result geometrically.

---

### Solution

#### Step 1. Compute the orthogonal projection $\mathrm{proj}_v u$

The vector projection of $u$ onto $v$ is given by the formula:

$$
\mathrm{proj}_v u = \left( \frac{u \cdot v}{\|v\|^2} \right) v
$$

1. **Compute dot product $u \cdot v$:**
   $$
   u \cdot v = (4)(1) + (2)(1) = 4 + 2 = 6
   $$

2. **Compute $\|v\|^2$:**
   $$
   \|v\|^2 = 1^2 + 1^2 = 1 + 1 = 2
   $$

3. **Calculate $\mathrm{proj}_v u$:**
   $$
   \mathrm{proj}_v u = \left( \frac{6}{2} \right) \begin{pmatrix} 1 \\ 1 \end{pmatrix} = 3 \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 3 \\ 3 \end{pmatrix}
   $$

---

#### Step 2. Compute the residual vector $r = u - \mathrm{proj}_v u$

Subtract the projection vector from $u$:

$$
r = u - \mathrm{proj}_v u = \begin{pmatrix} 4 \\ 2 \end{pmatrix} - \begin{pmatrix} 3 \\ 3 \end{pmatrix} = \begin{pmatrix} 4 - 3 \\ 2 - 3 \end{pmatrix} = \begin{pmatrix} 1 \\ -1 \end{pmatrix}
$$

---

#### Step 3. Verify $r \cdot v = 0$

Compute the dot product of $r$ and $v$:

$$
r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0
$$

Since $r \cdot v = 0$, the vector $r$ is orthogonal to $v$.

---

#### Step 4. Geometric Explanation

This result reflects the fundamental **orthogonal decomposition** of vector $u$ with respect to vector $v$:

$$
u = \mathrm{proj}_v u + r
$$

1. **Parallel Component ($\mathrm{proj}_v u$):** The projection vector $(3, 3)^T$ represents the component of $u$ that lies directly along the line defined by $v$. It is the shadow cast by $u$ onto the span of $v$.
2. **Perpendicular Component ($r$):** The residual vector $(1, -1)^T$ represents the component of $u$ that is strictly perpendicular (orthogonal) to $v$.
3. **Right Triangle:** The three vectors $u$, $\mathrm{proj}_v u$, and $r$ form a right-angled triangle where $u$ acts as the hypotenuse, $\mathrm{proj}_v u$ is the base along $v$, and $r$ is the altitude connecting the tip of $\mathrm{proj}_v u$ perpendicularly to the tip of $u$.