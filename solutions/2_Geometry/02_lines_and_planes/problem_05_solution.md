### Exercise 5. Relative Position of Two Lines

Analyze the position of lines $L_1$ and $L_2$:

$$
L_1: \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\ 2 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}
$$

$$
L_2: \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} + s \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix}, \quad s \in \mathbb{R}
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

---

### Solution

#### Step 1. Check for parallelism (Direction Vectors)

Extract the direction vectors $v_1$ and $v_2$ of lines $L_1$ and $L_2$:

$$
v_1 = \begin{pmatrix} 1 \\ 2 \\ 1 \end{pmatrix}, \quad v_2 = \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix}
$$

Check if $v_1$ is a scalar multiple of $v_2$ ($v_1 = k v_2$):

- For the $x$-component: $1 = k(0)$, which is impossible.

Since $v_1$ and $v_2$ are not parallel, the lines $L_1$ and $L_2$ are **not parallel**. They are either **intersecting** or **skew**.

---

#### Step 2. Test for an intersection point

Equate the parametric components of $L_1$ and $L_2$ to find parameters $t$ and $s$:

$$
\begin{cases}
1 + t = 2, & \text{(Equation 1)} \\
1 + 2t = s, & \text{(Equation 2)} \\
t = 1 - s. & \text{(Equation 3)}
\end{cases}
$$

1. **Solve Equation 1 for $t$:**
   $$
   1 + t = 2 \implies t = 1
   $$

2. **Substitute $t = 1$ into Equation 2 to find $s$:**
   $$
   1 + 2(1) = s \implies s = 3
   $$

3. **Check consistency in Equation 3 using $t = 1$ and $s = 3$:**
   $$
   \text{LHS} = t = 1
   $$
   $$
   \text{RHS} = 1 - s = 1 - 3 = -2
   $$

   $$
   1 \neq -2
   $$

The system of equations is **inconsistent** (there are no parameter values $t$ and $s$ that satisfy all three component equations simultaneously). Therefore, the lines do not intersect.

---

#### Step 3. Classification and Justification

- **Classification:** Lines $L_1$ and $L_2$ are **skew lines**.
- **Justification:**
  1. **Not Parallel:** Their direction vectors $v_1 = (1, 2, 1)^T$ and $v_2 = (0, 1, -1)^T$ are linearly independent (not scalar multiples of each other).
  2. **No Intersection:** Equating their parametric equations yields a system with no solution, meaning they do not share any common points in 3D space ($\mathbb{R}^3$).

By definition, two non-parallel, non-intersecting lines in 3D space are skew.