### Exercise 2. Gaussian Elimination — One Solution

Solve using Gaussian elimination:

$$
\begin{cases}
x + y + z = 6, \\
2x - y + z = 3, \\
x + 2y - z = 2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the linear system as an augmented matrix:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

---

#### Step 2. Row reduce to upper triangular form (Row Echelon Form)

**Step 2.1:** Eliminate $x$ from the second and third rows using $R_1$.

Perform $R_2 \leftarrow R_2 - 2 R_1$:

- Row 2 calculation: $(2 - 2(1), -1 - 2(1), 1 - 2(1) \mid 3 - 2(6)) = (0, -3, -1 \mid -9)$

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, 2 - 1, -1 - 1 \mid 2 - 6) = (0, 1, -2 \mid -4)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

---

**Step 2.2:** Swap Row 2 and Row 3 to obtain a pivot of $1$ in column 2 ($R_2 \leftrightarrow R_3$).

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

---

**Step 2.3:** Eliminate $y$ from the third row using the new $R_2$.

Perform $R_3 \leftarrow R_3 + 3 R_2$:

- Row 3 calculation: $(0 + 3(0), -3 + 3(1), -1 + 3(-2) \mid -9 + 3(-4)) = (0, 0, -7 \mid -21)$

The matrix is now in row echelon form:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

---

#### Step 3. Back-substitution

Convert the upper triangular system back into equations:

1. **Third equation:**
   $$
   -7z = -21 \implies z = \frac{-21}{-7} = 3
   $$

2. **Second equation:**
   $$
   y - 2z = -4 \implies y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
   $$

3. **First equation:**
   $$
   x + y + z = 6 \implies x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1
   $$

Thus, the unique solution vector is:

$$
x = 
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=
\begin{pmatrix}
1 \\
2 \\
3 \\
\end{pmatrix}
$$

---

#### Step 4. Check consistency by substitution

Substitute $x = 1$, $y = 2$, and $z = 3$ back into all three original equations:

1. **Equation 1:**
   $$
   1 + 2 + 3 = 6 \quad \checkmark \quad (6 = 6)
   $$

2. **Equation 2:**
   $$
   2(1) - 2 + 3 = 2 - 2 + 3 = 3 \quad \checkmark \quad (3 = 3)
   $$

3. **Equation 3:**
   $$
   1 + 2(2) - 3 = 1 + 4 - 3 = 2 \quad \checkmark \quad (2 = 2)
   $$

All three equations are satisfied, confirming the solution is correct and consistent.