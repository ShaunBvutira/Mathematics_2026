### Exercise 6. Parameter and Invertibility

For

$$
A(t) = 
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant.

---

### Solution

#### Step 1. Compute the determinant of matrix A(t)

For the $2 \times 2$ matrix $A(t) = \begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}$, compute the determinant using the standard formula $\det = ad - bc$:

$$
\begin{aligned}
\det A(t) &= (t)(t) - (1)(2) \\
          &= t^2 - 2
\end{aligned}
$$

---

#### Step 2. Relate invertibility to the determinant

**Invertibility Criterion:** A square matrix $A(t)$ is **not invertible** (also called singular) if and only if its determinant is equal to zero:

$$
\det A(t) = 0
$$

Conversely, a matrix is invertible if and only if its determinant is non-zero ($\det A(t) \neq 0$).

---

#### Step 3. Solve for t

Set the determinant equation to zero to find the values of $t$ where the matrix fails to be invertible:

$$
t^2 - 2 = 0
$$

Solve for $t$:

$$
\begin{aligned}
t^2 &= 2 \\
t &= \pm \sqrt{2}
\end{aligned}
$$

---

#### Step 4. Conclusion

The matrix $A(t)$ is **not invertible** when:

$$
t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}
$$

For these specific values, $\det A(t) = 0$, which means the rows (and columns) of matrix $A(t)$ are linearly dependent, and no matrix inverse $A^{-1}(t)$ exists. For all other values of $t$, $\det A(t) \neq 0$, and the matrix is invertible.