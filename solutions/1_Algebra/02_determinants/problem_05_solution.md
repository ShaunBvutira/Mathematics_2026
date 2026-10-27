### Exercise 5. Row Operations

For

$$
A = 
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

---

### Solution

#### Step 1. Row operation properties of determinants

- **Adding a multiple of one row to another row ($R_i \leftarrow R_i + c R_j$):** The determinant does not change ($\det A' = \det A$).
- **Swapping two rows ($R_i \leftrightarrow R_j$):** The determinant is multiplied by $-1$ ($\det A' = -\det A$).
- **Multiplying a row by a scalar $c$ ($R_i \leftarrow c R_i$):** The determinant is multiplied by $c$ ($\det A' = c \det A$).

---

#### Step 2. Create zeros in the first column

To simplify matrix $A$, use the first row to create zeros under the top-left entry:

1. Perform $R_2 \leftarrow R_2 - 2 R_1$:
   - Row 2 calculation: $(2 - 2(1), 1 - 2(2), 0 - 2(3)) = (0, -3, -6)$

2. Perform $R_3 \leftarrow R_3 + R_1$:
   - Row 3 calculation: $(-1 + 1, 4 + 2, 2 + 3) = (0, 6, 5)$

The new matrix is:

$$
A_1 = 
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

**Determinant status:** Since row addition/subtraction operations do not alter the determinant, $\det A = \det A_1$.

---

#### Step 3. Create a zero in the second column below the pivot

Now, use Row 2 of $A_1$ to eliminate the entry below it in Row 3:

Perform $R_3 \leftarrow R_3 + 2 R_2$:
- Row 3 calculation: $(0 + 2(0), 6 + 2(-3), 5 + 2(-6)) = (0, 0, -7)$

The new upper triangular matrix is:

$$
A_2 = 
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

**Determinant status:** Adding a scalar multiple of Row 2 to Row 3 does not change the determinant. Therefore:

$$
\det A = \det A_1 = \det A_2
$$

---

#### Step 4. Compute the determinant of the upper triangular matrix

Matrix $A_2$ is in upper triangular form. The determinant of a triangular matrix is the product of its main diagonal entries:

$$
\begin{aligned}
\det A_2 &= (1) \cdot (-3) \cdot (-7) \\
         &= 21
\end{aligned}
$$

Since no row operations changed the determinant throughout the process:

$$
\det A = 21
$$