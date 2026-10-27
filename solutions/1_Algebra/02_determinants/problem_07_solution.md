### Exercise 7. Using Properties Instead of Recomputing

Suppose that for a $3 \times 3$ matrix $A$, $\det A = -4$. Compute

$$
\det(2A), \quad \det(A^T), \quad \det(A^2), \quad \det(-A).
$$

Justify each answer using the appropriate property.

---

### Solution

#### Step 1. Compute $\det(2A)$

**Property:** For an $n \times n$ matrix $A$ and a scalar $c$, scaling the matrix scales each of its $n$ rows by $c$. Therefore:

$$
\det(cA) = c^n \det A
$$

Since $A$ is a $3 \times 3$ matrix ($n = 3$) and $c = 2$:

$$
\begin{aligned}
\det(2A) &= 2^3 \det A \\
         &= 8 (-4) \\
         &= -32
\end{aligned}
$$

---

#### Step 2. Compute $\det(A^T)$

**Property:** Transposing a square matrix does not change its determinant:

$$
\det(A^T) = \det A
$$

Using the given value $\det A = -4$:

$$
\det(A^T) = -4
$$

---

#### Step 3. Compute $\det(A^2)$

**Property:** The determinant of a product of square matrices equals the product of their determinants ($\det(AB) = \det A \cdot \det B$). Consequently:

$$
\det(A^2) = \det(A \cdot A) = (\det A)^2
$$

Using $\det A = -4$:

$$
\begin{aligned}
\det(A^2) &= (-4)^2 \\
          &= 16
\end{aligned}
$$

---

#### Step 4. Compute $\det(-A)$

**Property:** Negating a matrix is equivalent to multiplying it by the scalar $c = -1$. For an $n \times n$ matrix:

$$
\det(-A) = (-1)^n \det A
$$

Since $A$ is a $3 \times 3$ matrix ($n = 3$ is odd):

$$
\begin{aligned}
\det(-A) &= (-1)^3 \det A \\
         &= -1 (-4) \\
         &= 4
\end{aligned}
$$

---

#### Summary of Results

$$
\begin{aligned}
\det(2A) &= -32, \\
\det(A^T) &= -4, \\
\det(A^2) &= 16, \\
\det(-A) &= 4.
\end{aligned}
$$