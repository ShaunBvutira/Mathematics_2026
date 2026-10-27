### Exercise 1. Determinant of a 2×2 Matrix

Compute

$$
\det 
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}, \quad 
\det 
\begin{pmatrix}
17 & 2 \\
14 & 1 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

---

### Solution

#### Step 1. Define the determinant formula for a 2×2 matrix

For any $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by:

$$
\det A = ad - bc
$$

---

#### Step 2. Compute the determinant of the first matrix

Let the first matrix be:

$$
A = 
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix}
$$

Applying the formula:

$$
\begin{aligned}
\det A &= (3)(4) - (-2)(5) \\
       &= 12 - (-10) \\
       &= 12 + 10 \\
       &= 22
\end{aligned}
$$

Thus, $\det A = 22$.

---

#### Step 3. Compute the determinant of the second matrix

Let the second matrix be:

$$
B = 
\begin{pmatrix}
17 & 2 \\
14 & 1 \\
\end{pmatrix}
$$

Applying the formula:

$$
\begin{aligned}
\det B &= (17)(1) - (2)(14) \\
       &= 17 - 28 \\
       &= -11
\end{aligned}
$$

Thus, $\det B = -11$.

---

#### Step 4. Determine invertibility

A square matrix is invertible if and only if its determinant is non-zero ($\det \neq 0$).

- For matrix $A$: $\det A = 22 \neq 0$, so $A$ is invertible.
- For matrix $B$: $\det B = -11 \neq 0$, so $B$ is invertible.

Both matrices are invertible because neither of their determinants is equal to zero.