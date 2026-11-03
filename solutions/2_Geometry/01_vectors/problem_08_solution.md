### Exercise 8. Linear Combination and Checking the Result

Check whether $w = (5, 1)^T$ can be written as

$$
w = au + bv,
$$

where $u = (1, 1)^T$ and $v = (2, -1)^T$. If so, find $a, b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

---

### Solution

#### Step 1. Set up the system of linear equations

Express $w = au + bv$ in vector component form:

$$
\begin{pmatrix}
5 \\
1 \\
\end{pmatrix}
= a
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
+ b
\begin{pmatrix}
2 \\
-1 \\
\end{pmatrix}
$$

This expands to the system:

$$
\begin{cases}
a + 2b = 5, \\
a - b = 1.
\end{cases}
$$

---

#### Step 2. Solve for $a$ and $b$

Subtract the second equation from the first equation to eliminate $a$:

$$
(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = \frac{4}{3}
$$

Substitute $b = \frac{4}{3}$ into the second equation ($a = 1 + b$):

$$
a = 1 + \frac{4}{3} = \frac{7}{3}
$$

Thus, $w$ can indeed be written as a linear combination of $u$ and $v$ with coefficients:

$$
a = \frac{7}{3}, \quad b = \frac{4}{3}
$$

---

#### Step 3. Reconstruct $w$ from $a$ and $b$ to check the result

Substitute $a = \frac{7}{3}$ and $b = \frac{4}{3}$ back into $au + bv$:

$$
\begin{aligned}
au + bv &= \frac{7}{3} \begin{pmatrix} 1 \\ 1 \end{pmatrix} + \frac{4}{3} \begin{pmatrix} 2 \\ -1 \end{pmatrix} \\
        &= \begin{pmatrix} \frac{7}{3} \\[1ex] \frac{7}{3} \end{pmatrix} + \begin{pmatrix} \frac{8}{3} \\[1ex] -\frac{4}{3} \end{pmatrix} \\
        &= \begin{pmatrix} \frac{7}{3} + \frac{8}{3} \\[1ex] \frac{7}{3} - \frac{4}{3} \end{pmatrix} \\
        &= \begin{pmatrix} \frac{15}{3} \\[1ex] \frac{3}{3} \end{pmatrix} = \begin{pmatrix} 5 \\ 1 \end{pmatrix} = w
\end{aligned}
$$

The reconstruction confirms that $w = \frac{7}{3}u + \frac{4}{3}v$.

---

#### Step 4. Geometric meaning of the existence of coefficients $a, b$

1. **Non-Collinear Basis:** The vectors $u = (1, 1)^T$ and $v = (2, -1)^T$ are non-parallel (linearly independent) in the 2D plane $\mathbb{R}^2$. Therefore, they form a basis for $\mathbb{R}^2$ and span the entire 2D space ($\text{span}\{u, v\} = \mathbb{R}^2$).
2. **Skew Coordinate System:** The existence and uniqueness of $a$ and $b$ mean that $w$ can be uniquely represented in a non-orthogonal grid defined by axes along the directions of $u$ and $v$. 
3. **Parallelogram Diagonal:** Geometrically, traversing $\frac{7}{3}$ units along the line defined by $u$, followed by $\frac{4}{3}$ units along the direction of $v$, forms a vector path that arrives precisely at the destination vector $w = (5, 1)^T$.