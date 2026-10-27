### Exercise 10. Columns of a Matrix Product

Given

$$
A = 
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1, b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

---

### Solution

#### Step 1. Compute $Ab_1$ and $Ab_2$

The columns of matrix $B$ are:

$$
b_1 = 
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}, \quad 
b_2 = 
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

- **Compute $Ab_1$:**

$$
\begin{aligned}
Ab_1 &= 
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
(1)(1) + (2)(-1) + (0)(3) \\
(0)(1) + (1)(-1) + (1)(3) \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

- **Compute $Ab_2$:**

$$
\begin{aligned}
Ab_2 &= 
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
(1)(2) + (2)(0) + (0)(1) \\
(0)(2) + (1)(0) + (1)(1) \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix} \\
     &= 
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute the matrix $AB$

Multiply matrix $A$ ($2 \times 3$) by matrix $B$ ($3 \times 2$) to get a $2 \times 2$ matrix:

$$
\begin{aligned}
AB &= 
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(1) + (2)(-1) + (0)(3) & (1)(2) + (2)(0) + (0)(1) \\
(0)(1) + (1)(-1) + (1)(3) & (0)(2) + (1)(0) + (1)(1) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
1 - 2 + 0 & 2 + 0 + 0 \\
0 - 1 + 3 & 0 + 0 + 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Compare the results and explain the column-by-column property

- **Comparison:**
  The first column of $AB$ is $\begin{pmatrix} -1 \\ 2 \end{pmatrix}$, which matches $Ab_1$.
  The second column of $AB$ is $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$, which matches $Ab_2$.

  Therefore:

$$
AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix} = 
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

- **Explanation:**
  By the **column definition of matrix multiplication**, multiplying matrix $A$ by matrix $B = \begin{pmatrix} b_1 & b_2 \end{pmatrix}$ applies the linear transformation represented by $A$ independently to each column vector of $B$. 

  Specifically, column $j$ of the product $AB$ is formed by multiplying matrix $A$ by the $j$-th column vector of $B$:

$$
A \begin{pmatrix} b_1 & b_2 & \dots & b_k \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 & \dots & Ab_k \end{pmatrix}
$$

  Because each column $b_j$ acts independently as an input vector to $A$, the resulting matrix $AB$ collects the transformed column vectors $Ab_j$ side by side.