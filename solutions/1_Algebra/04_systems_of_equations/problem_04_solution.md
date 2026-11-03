### Exercise 4. Infinitely Many Solutions

Solve

$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the linear system in augmented matrix form:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

---

#### Step 2. Perform Gaussian elimination

**Step 2.1:** Eliminate $x$ from the second and third rows using $R_1$.

Perform $R_2 \leftarrow R_2 - 2 R_1$:

- Row 2 calculation: $(2 - 2(1), 2 - 2(1), 2 - 2(1) \mid 4 - 2(2)) = (0, 0, 0 \mid 0)$

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, -1 - 1, 1 - 1 \mid 0 - 2) = (0, -2, 0 \mid -2)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

---

**Step 2.2:** Swap Row 2 and Row 3 to bring the non-zero row up ($R_2 \leftrightarrow R_3$):

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

---

**Step 2.3:** Scale Row 2 by multiplying by $-\frac{1}{2}$ ($R_2 \leftarrow -\frac{1}{2} R_2$):

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 1 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

---

#### Step 3. Identify basic and free variables

Convert the non-zero rows back to algebraic equations:

1. **Second row:**
   $$
   y = 1
   $$

2. **First row:**
   $$
   x + y + z = 2
   $$

The pivot columns are column 1 (for $x$) and column 2 (for $y$). Column 3 (for $z$) has no pivot. 

- **Basic variables:** $x, y$
- **Free variable:** $z$

---

#### Step 4. Express the solution in parametric form

Let $z = t$, where $t \in \mathbb{R}$ is a free parameter.

Substitute $y = 1$ and $z = t$ into the first equation to solve for $x$:

$$
x + 1 + t = 2 \implies x = 1 - t
$$

Thus, the parametric solution is:

$$
\begin{cases}
x = 1 - t, \\
y = 1, \\
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
=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix},
\quad t \in \mathbb{R}
$$

---

#### Step 5. Check a specific point for a chosen parameter value

Choose parameter value $t = 2$:

- $x = 1 - 2 = -1$
- $y = 1$
- $z = 2$

Point to verify: $(x, y, z) = (-1, 1, 2)$.

Substitute into all three original equations:

1. **Equation 1 ($x + y + z = 2$):**
   $$
   -1 + 1 + 2 = 2 \quad \checkmark \quad (2 = 2)
   $$

2. **Equation 2 ($2x + 2y + 2z = 4$):**
   $$
   2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4 \quad \checkmark \quad (4 = 4)
   $$

3. **Equation 3 ($x - y + z = 0$):**
   $$
   -1 - 1 + 2 = 0 \quad \checkmark \quad (0 = 0)
   $$

All three equations hold true, confirming the parametric solution is correct.