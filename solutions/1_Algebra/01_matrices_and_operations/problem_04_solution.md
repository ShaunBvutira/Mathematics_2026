### Exercise 4. Matrix Multiplication and Noncommutativity

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},
\quad
B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

---

### Solution

#### Step 1: Computation of $AB$

$$
AB =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
(1)(2) + (2)(3) & (1)(0) + (2)(1) \\
(0)(2) + (1)(3) & (0)(0) + (1)(1) \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
2+6 & 0+2 \\
0+3 & 0+1 \\
\end{pmatrix}
=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

#### Step 2: Computation of $BA$

$$
BA =
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
(2)(1) + (0)(0) & (2)(2) + (0)(1) \\
(3)(1) + (1)(0) & (3)(2) + (1)(1) \\
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
2+0 & 4+0 \\
3+0 & 6+1 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
$$

#### Step 3: Comparison and Explanation

Comparing the two products:

$$
AB =
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
= BA
$$

Thus, $AB \neq BA$.

Noncommutativity of matrix multiplication means that changing the order of matrices in a multiplication operation can change the resulting matrix. Unlike real numbers, where $ab = ba$ always holds, matrix multiplication generally depends on the order of the factors.
