### Exercise 13. Does Every Equation Add New Information?

Consider the system

$$
\begin{cases}
x_1 + x_2 = 10, \\
x_2 + x_3 = 8, \\
x_1 - x_3 = 2.
\end{cases}
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the system as an augmented matrix:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}
$$

---

#### Step 2. Perform Gaussian elimination

**Step 2.1:** Eliminate $x_1$ from the third row using $R_1$.

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, 0 - 1, -1 - 0 \mid 2 - 10) = (0, -1, -1 \mid -8)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}
$$

---

**Step 2.2:** Eliminate $x_2$ from the third row using $R_2$.

Perform $R_3 \leftarrow R_3 + R_2$:

- Row 3 calculation: $(0 + 0, -1 + 1, -1 + 1 \mid -8 + 8) = (0, 0, 0 \mid 0)$

The matrix is now in row echelon form:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

---

#### Step 3. Identify basic and free variables and write in parametric form

The pivot columns are column 1 (for $x_1$) and column 2 (for $x_2$). Column 3 (for $x_3$) has no pivot.

- **Basic variables:** $x_1, x_2$
- **Free variable:** $x_3$

Let $x_3 = t$, where $t \in \mathbb{R}$ is a free parameter.

1. **From Row 2:**
   $$
   x_2 + x_3 = 8 \implies x_2 = 8 - t
   $$

2. **From Row 1:**
   $$
   x_1 + x_2 = 10 \implies x_1 + (8 - t) = 10 \implies x_1 = 2 + t
   $$

Thus, the parametric solution is:

$$
\begin{cases}
x_1 = 2 + t, \\
x_2 = 8 - t, \\
x_3 = t,
\end{cases}
\quad t \in \mathbb{R}
$$

Or in vector form:

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
8 \\
0 \\
\end{pmatrix}
+ t
\begin{pmatrix}
1 \\
-1 \\
1 \\
\end{pmatrix},
\quad t \in \mathbb{R}
$$

---

#### Step 4. Demonstrate linear dependence of the equations

The appearance of the all-zero row $[0 \ 0 \ 0 \mid 0]$ during elimination shows that the third equation is **redundant** (linearly dependent on the first two). It does **not** add new geometric restrictions to the solution set.

To explicitly show how Equation 3 follows directly from Equations 1 and 2:

Let the three equations be denoted as:

$$
E_1: x_1 + x_2 = 10
$$

$$
E_2: x_2 + x_3 = 8
$$

$$
E_3: x_1 - x_3 = 2
$$

Subtract $E_2$ from $E_1$:

$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8
$$

$$
x_1 - x_3 = 2
$$

Which is precisely $E_3$. 

Since $E_3 = E_1 - E_2$, the third equation is a direct linear combination of the first two and adds no new information. The solution set is fully determined by any two of the three equations.