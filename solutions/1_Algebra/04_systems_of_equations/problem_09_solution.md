### Exercise 9. A System from a Sum Condition

Find numbers $x, y$ satisfying

$$
\begin{cases}
x + y = 10, \\
2x + 5y = 32.
\end{cases}
$$

Solve the system and explain geometrically why the solution is unique.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the linear system in augmented matrix form:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}
$$

---

#### Step 2. Perform Gaussian elimination

Eliminate the $x$-variable from the second row by performing $R_2 \leftarrow R_2 - 2R_1$:

- Row 2 calculation: $(2 - 2(1), 5 - 2(1) \mid 32 - 2(10)) = (0, 3 \mid 12)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}
$$

---

#### Step 3. Back-substitution

Convert the upper-triangular matrix back into algebraic equations:

1. **Second row:**
   $$
   3y = 12 \implies y = 4
   $$

2. **First row:**
   $$
   x + y = 10 \implies x + 4 = 10 \implies x = 6
   $$

The unique solution is:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
4 \\
\end{pmatrix}
$$

---

#### Step 4. Geometric explanation of uniqueness

Each linear equation in two variables represents a straight line in the 2D Cartesian plane ($\mathbb{R}^2$):

- **Line 1 ($L_1$):** $y = -x + 10$ (Slope $m_1 = -1$, $y$-intercept $(0, 10)$)
- **Line 2 ($L_2$):** $y = -\frac{2}{5}x + \frac{32}{5}$ (Slope $m_2 = -\frac{2}{5}$, $y$-intercept $(0, 6.4)$)

**Why the solution is unique:**
1. **Different Slopes:** The slopes of the two lines are distinct ($m_1 = -1 \neq -\frac{2}{5} = m_2$), which means the lines are non-parallel.
2. **Determinant Criterion:** The determinant of the coefficient matrix $A$ is non-zero:
   $$
   \det A = 
   \begin{vmatrix}
   1 & 1 \\
   2 & 5 \\
   \end{vmatrix}
   = (1)(5) - (1)(2) = 3 \neq 0
   $$

Because the two non-parallel lines lie in the same plane, they must intersect at **exactly one single point**, $(6, 4)$. Thus, the system has a unique solution.