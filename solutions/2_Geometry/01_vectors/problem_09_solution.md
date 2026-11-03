### Exercise 9. Cross Product as a Perpendicular Direction

For $u = (1, 2, 0)^T$ and $v = (0, 1, 3)^T$, compute $u \times v$. Use dot products to check perpendicularity to both vectors, compute $v \times u$, and compare the results.

---

### Solution

#### Step 1. Compute $u \times v$

The cross product $u \times v$ of two vectors $u = (u_1, u_2, u_3)^T$ and $v = (v_1, v_2, v_3)^T$ is computed using the determinant formula:

$$
u \times v = 
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3 \\
\end{vmatrix}
=
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
1 & 2 & 0 \\
0 & 1 & 3 \\
\end{vmatrix}
$$

Expanding along the first row:

$$
\begin{aligned}
u \times v &= \hat{i} \begin{vmatrix} 2 & 0 \\ 1 & 3 \end{vmatrix} - \hat{j} \begin{vmatrix} 1 & 0 \\ 0 & 3 \end{vmatrix} + \hat{k} \begin{vmatrix} 1 & 2 \\ 0 & 1 \end{vmatrix} \\
           &= \hat{i} (2 \cdot 3 - 0 \cdot 1) - \hat{j} (1 \cdot 3 - 0 \cdot 0) + \hat{k} (1 \cdot 1 - 2 \cdot 0) \\
           &= 6\hat{i} - 3\hat{j} + 1\hat{k}
\end{aligned}
$$

Thus, the cross product is:

$$
u \times v = 
\begin{pmatrix}
6 \\
-3 \\
1 \\
\end{pmatrix}
$$

---

#### Step 2. Verify perpendicularity using dot products

Check that $(u \times v)$ is orthogonal to both $u$ and $v$ by computing their dot products:

1. **Check orthogonality with $u = (1, 2, 0)^T$:**

   $$
   (u \times v) \cdot u = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0
   $$

   Since $(u \times v) \cdot u = 0$, $u \times v$ is perpendicular to $u$.

2. **Check orthogonality with $v = (0, 1, 3)^T$:**

   $$
   (u \times v) \cdot v = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0
   $$

   Since $(u \times v) \cdot v = 0$, $u \times v$ is perpendicular to $v$.

Both dot products equal zero, confirming that $u \times v$ is perpendicular to both original vectors.

---

#### Step 3. Compute $v \times u$

Compute the cross product in reverse order, $v \times u$:

$$
v \times u = 
\begin{vmatrix}
\hat{i} & \hat{j} & \hat{k} \\
0 & 1 & 3 \\
1 & 2 & 0 \\
\end{vmatrix}
$$

Expanding along the first row:

$$
\begin{aligned}
v \times u &= \hat{i} \begin{vmatrix} 1 & 3 \\ 2 & 0 \end{vmatrix} - \hat{j} \begin{vmatrix} 0 & 3 \\ 1 & 0 \end{vmatrix} + \hat{k} \begin{vmatrix} 0 & 1 \\ 1 & 2 \end{vmatrix} \\
           &= \hat{i} (1 \cdot 0 - 3 \cdot 2) - \hat{j} (0 \cdot 0 - 3 \cdot 1) + \hat{k} (0 \cdot 2 - 1 \cdot 1) \\
           &= -6\hat{i} + 3\hat{j} - 1\hat{k}
\end{aligned}
$$

Thus:

$$
v \times u = 
\begin{pmatrix}
-6 \\
3 \\
-1 \\
\end{pmatrix}
$$

---

#### Step 4. Compare the results

Comparing $u \times v$ and $v \times u$:

$$
u \times v = 
\begin{pmatrix}
6 \\
-3 \\
1 \\
\end{pmatrix},
\quad
v \times u = 
\begin{pmatrix}
-6 \\
3 \\
-1 \\
\end{pmatrix}
$$

- **Anti-commutativity:** The relationship between the two products is $v \times u = -(u \times v)$.
- **Geometric Interpretation:** Reversing the order of vectors in a cross product flips the orientation of the resulting vector by $180^\circ$ (pointing in the exact opposite direction) while maintaining the same magnitude and line of action perpendicular to the plane containing $u$ and $v$. This follows the right-hand rule.