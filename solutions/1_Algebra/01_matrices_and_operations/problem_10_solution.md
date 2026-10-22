### Exercise 10. Columns of a Matrix Product

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},
\quad
B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Denote the columns of $B$ by $b_1, b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

---

### Solution

#### Step 1: Compute $Ab_1$ and $Ab_2$

The columns of $B$ are:

$$
b_1 =
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},
\quad
b_2 =
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

Compute $Ab_1$:

$$
Ab_1 =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}
=
\begin{pmatrix}
(1)(1) + (2)(-1) + (0)(3) \\
(0)(1) + (1)(-1) + (1)(3) \\
\end{pmatrix}
=
\begin{pmatrix}
1 - 2 + 0 \\
0 - 1 + 3 \\
\end{pmatrix}
=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
$$

Compute $Ab_2$:

$$
Ab_2 =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
=
\begin{pmatrix}
(1)(2) + (2)(0) + (0)(1) \\
(0)(2) + (1)(0) + (1)(1) \\
\end{pmatrix}
=
\begin{pmatrix}
2 + 0 + 0 \\
0 + 0 + 1 \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

#### Step 2: Compute the matrix $AB$

Multiply $A$ ($2 \times 3$) and $B$ ($3 \times 2$) directly:

$$
AB =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
(1)(1) + (2)(-1) + (0)(3) & (1)(2) + (2)(0) + (0)(1) \\
(0)(1) + (1)(-1) + (1)(3) & (0)(2) + (1)(0) + (1)(1) \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

#### Step 3: Comparison and Explanation

Comparing the computed matrix $AB$ with $Ab_1$ and $Ab_2$:

$$
AB =
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}
$$

**Explanation:**
By definition of matrix multiplication, the $j$-th column of a product $AB$ is obtained by multiplying the left matrix $A$ by the $j$-th column of the right matrix $B$, denoted as $b_j$. Writing $B$ in column form $B = \begin{pmatrix} b_1 & b_2 \end{pmatrix}$, we have:

$$
AB = A \begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}
$$

Thus, each column of the matrix product $AB$ is precisely the matrix $A$ acting on the corresponding column vector of $B$.