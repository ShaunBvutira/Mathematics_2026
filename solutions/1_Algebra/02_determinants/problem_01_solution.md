### Exercise 1. Determinant of a $2 \times 2$ Matrix

Compute

$$
\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}, \quad \det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

---

### Solution

#### Step 1. Determinant formula for a $2 \times 2$ matrix

For a $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is given by:

$$
\det(M) = ad - bc
$$

A matrix is **invertible** if and only if its determinant is non-zero ($\det(M) \neq 0$).

---

#### Step 2. Compute the determinant of the first matrix

Let $A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$:

$$
\begin{aligned}
\det(A) &= (3)(4) - (-2)(5) \\
        &= 12 - (-10) \\
        &= 12 + 10 \\
        &= 22
\end{aligned}
$$

---

#### Step 3. Compute the determinant of the second matrix

Let $B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$:

$$
\begin{aligned}
\det(B) &= (1)(14) - (7)(2) \\
        &= 14 - 14 \\
        &= 0
\end{aligned}
$$

---

#### Step 4. Invertibility conclusion and justification

- **Matrix $A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ is invertible.**
  - **Justification:** $\det(A) = 22 \neq 0$. Since the determinant is non-zero, $A$ is non-singular and its inverse exists.

- **Matrix $B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$ is not invertible (singular).**
  - **Justification:** $\det(B) = 0$. A zero determinant indicates that the rows are linearly dependent ($R_2 = 2R_1$), so no inverse exists.