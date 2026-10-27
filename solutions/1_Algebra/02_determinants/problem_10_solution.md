### Exercise 10. Detecting Dependence

Without carrying out a full determinant calculation, explain why

$$
\det 
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}
= 0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

---

### Solution

#### Step 1. Identify row dependence

Let the rows of the matrix be:

$$
\begin{aligned}
R_1 &= \begin{pmatrix} 1 & 2 & 3 \end{pmatrix} \\
R_2 &= \begin{pmatrix} 2 & 4 & 6 \end{pmatrix} \\
R_3 &= \begin{pmatrix} 0 & 1 & 5 \end{pmatrix}
\end{aligned}
$$

Comparing Row 1 and Row 2, Row 2 is an exact scalar multiple of Row 1:

$$
R_2 = 2 R_1
$$

This linear relation ($R_2 - 2 R_1 = 0$) shows that the rows of the matrix are **linearly dependent**.

---

#### Step 2. Relate row dependence to the determinant

**Property of Determinants:** If one row of a square matrix is a scalar multiple of another row (or if the rows are linearly dependent), the determinant of the matrix is equal to zero.

To see why:
If we perform the row operation $R_2 \leftarrow R_2 - 2 R_1$ (which does not change the determinant), Row 2 becomes a row of all zeros:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}
$$

Expanding along the second row containing all zeros yields:

$$
\det = 0
$$

---

#### Step 3. Connect dependence with noninvertibility

A square matrix $A$ is invertible if and only if its rows (and columns) are linearly independent, which is equivalent to $\det A \neq 0$.

Because Row 2 is proportional to Row 1:
1. The rows span a subspace of dimension strictly less than 3 (the matrix does not have full row rank).
2. The linear system $A x = 0$ has non-trivial solutions (the nullity is greater than 0).
3. The determinant $\det A = 0$.

Therefore, the matrix cannot map $\mathbb{R}^3$ onto $\mathbb{R}^3$ injectively, making it **not invertible** (singular).