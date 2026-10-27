### Exercise 3. When Does the Inverse Not Exist?

For

$$
A = 
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

---

### Solution

#### Step 1. Explanation using the determinant

**Criterion:** A square matrix $A$ has an inverse $A^{-1}$ if and only if its determinant is non-zero ($\det A \neq 0$). If $\det A = 0$, the matrix is singular and its inverse does not exist.

Compute the determinant of matrix $A$:

$$
\begin{aligned}
\det A &= (2)(2) - (4)(1) \\
       &= 4 - 4 \\
       &= 0
\end{aligned}
$$

Since $\det A = 0$, the matrix $A$ is singular, and therefore $A^{-1}$ does not exist.

Furthermore, applying the inverse formula for a $2 \times 2$ matrix demonstrates why this fails algebraically:

$$
A^{-1} = \frac{1}{\det A}
\begin{pmatrix}
2 & -4 \\
-1 & 2 \\
\end{pmatrix}
$$

Because $\det A = 0$, evaluating the formula requires dividing by zero ($\frac{1}{0}$), which is undefined.

---

#### Step 2. Explanation using row dependence

Let the rows of matrix $A$ be:

$$
\begin{aligned}
R_1 &= \begin{pmatrix} 2 & 4 \end{pmatrix} \\
R_2 &= \begin{pmatrix} 1 & 2 \end{pmatrix}
\end{aligned}
$$

Comparing the two rows shows that Row 1 is a direct scalar multiple of Row 2:

$$
R_1 = 2 R_2
$$

Because one row is a scalar multiple of the other, the rows of matrix $A$ are **linearly dependent**.

**Geometric and Structural Impact:**
1. **Loss of Dimension:** The matrix maps all 2D space $\mathbb{R}^2$ onto a single 1D line ($y = \frac{1}{2}x$). Because 2D space is compressed into 1D, information is lost.
2. **Non-injectivity:** Multiple distinct vectors map to the zero vector $(0, 0)^T$ (for instance, $A \begin{pmatrix} 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$). 

Since a linear transformation that compresses space into a lower dimension cannot be uniquely reversed, matrix $A$ cannot have an inverse.