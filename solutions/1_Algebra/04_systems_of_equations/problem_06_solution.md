### Exercise 6. Transpose

For

$$
A = 
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that $(AB)^T = B^T A^T$.

---

### Solution

#### Step 1. Compute $A^T$ and $B^T$

The transpose of a matrix is formed by swapping its rows and columns (row $i$ becomes column $i$).

- Matrix $A$ has size $2 \times 3$, so $A^T$ has size $3 \times 2$:

$$
A^T = 
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

- Matrix $B$ has size $3 \times 2$, so $B^T$ has size $2 \times 3$:

$$
B^T = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

---

#### Step 2. Compute $AB$ and $(AB)^T$

Multiply matrix $A$ ($2 \times 3$) by matrix $B$ ($3 \times 2$) to get a $2 \times 2$ matrix:

$$
\begin{aligned}
AB &= 
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(1) + (2)(2) + (3)(-1) & (1)(0) + (2)(1) + (3)(3) \\
(4)(1) + (5)(2) + (6)(-1) & (4)(0) + (5)(1) + (6)(3) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
1 + 4 - 3 & 0 + 2 + 9 \\
4 + 10 - 6 & 0 + 5 + 18 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
\end{aligned}
$$

Now, take the transpose of $AB$:

$$
(AB)^T = 
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

---

#### Step 3. Compute $B^T A^T$

Multiply $B^T$ ($2 \times 3$) by $A^T$ ($3 \times 2$) to get a $2 \times 2$ matrix:

$$
\begin{aligned}
B^T A^T &= 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
(1)(1) + (2)(2) + (-1)(3) & (1)(4) + (2)(5) + (-1)(6) \\
(0)(1) + (1)(2) + (3)(3) & (0)(4) + (1)(5) + (3)(6) \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
1 + 4 - 3 & 4 + 10 - 6 \\
0 + 2 + 9 & 0 + 5 + 18 \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 4. Verify $(AB)^T = B^T A^T$

Comparing the two resulting matrices:

$$
(AB)^T = 
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
= B^T A^T
$$

The identity $(AB)^T = B^T A^T$ is verified.