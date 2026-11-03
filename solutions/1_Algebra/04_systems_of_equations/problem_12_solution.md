### Exercise 12. Homogeneous System

Solve

$$
\begin{cases}
x + 2y - z = 0, \\
2x + 4y - 2z = 0, \\
x - y + 2z = 0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0, 0, 0)$ always satisfies a homogeneous system.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid 0]$

Write the homogeneous linear system in augmented matrix form:

$$
[A \mid 0] = 
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}
$$

---

#### Step 2. Perform Gaussian elimination

**Step 2.1:** Eliminate $x$ from the second and third rows using $R_1$.

Perform $R_2 \leftarrow R_2 - 2R_1$:

- Row 2 calculation: $(2 - 2(1), 4 - 2(2), -2 - 2(-1) \mid 0 - 2(0)) = (0, 0, 0 \mid 0)$

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, -1 - 2, 2 - (-1) \mid 0 - 0) = (0, -3, 3 \mid 0)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}
$$

---

**Step 2.2:** Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) to place the non-zero row above:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

---

**Step 2.3:** Scale Row 2 by multiplying by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3} R_2$):

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 1 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

---

#### Step 3. Identify basic and free variables

Convert the non-zero rows back to algebraic equations:

1. **Second row:**
   $$
   y - z = 0 \implies y = z
   $$

2. **First row:**
   $$
   x + 2y - z = 0
   $$

The pivot columns are column 1 (for $x$) and column 2 (for $y$). Column 3 (for $z$) has no pivot.

- **Basic variables:** $x, y$
- **Free variable:** $z$

---

#### Step 4. Express the solution in parametric form

Let $z = t$, where $t \in \mathbb{R}$ is a free parameter.

Substitute $y = t$ and $z = t$ into the first equation to solve for $x$:

$$
x + 2(t) - t = 0 \implies x + t = 0 \implies x = -t
$$

Thus, the parametric solution is:

$$
\begin{cases}
x = -t, \\
y = t, \\
z = t,
\end{cases}
\quad t \in \mathbb{R}
$$

Or in vector form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
= t
\begin{pmatrix}
-1 \\
1 \\
1 \\
\end{pmatrix},
\quad t \in \mathbb{R}
$$

---

#### Step 5. Explain why $(0, 0, 0)$ always satisfies a homogeneous system

A general linear system is called **homogeneous** if its right-hand side constant vector is the zero vector ($Ax = 0$):

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n &= 0 \\
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n &= 0 \\
&\;\;\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n &= 0
\end{aligned}
$$

Substituting the zero vector $x = (0, 0, \dots, 0)^T$ into the system yields:

$$
a_{i1}(0) + a_{i2}(0) + \dots + a_{in}(0) = 0 + 0 + \dots + 0 = 0
$$

for every row $i = 1, 2, \dots, m$. 

Because $A \cdot 0 = 0$ is an identity for matrix multiplication regardless of the entries in $A$, the zero vector $(0, 0, \dots, 0)^T$ is **always** a valid solution (called the **trivial solution**) for any homogeneous system. 

*(In our parametric solution, setting $t = 0$ gives $(x, y, z) = (0, 0, 0)$).*