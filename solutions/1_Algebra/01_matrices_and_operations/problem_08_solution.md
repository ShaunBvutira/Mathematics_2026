### Exercise 8. Row Operations and Their Reversibility

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2 \leftarrow R_2 - 2R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

---

### Solution

#### Initial Matrix

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

#### Step 1: Perform $R_2 \leftarrow R_2 - 2R_1$

Compute the new row $2$:

$$
R_2 - 2R_1 = (2, 4, 1) - 2(1, 2, -1) = (2-2, 4-4, 1-(-2)) = (0, 0, 3)
$$

The matrix becomes:

$$
A_1 =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

#### Step 2: Perform $R_3 \leftarrow R_3 + R_1$

Compute the new row $3$:

$$
R_3 + R_1 = (-1, 1, 3) + (1, 2, -1) = (-1+1, 1+2, 3+(-1)) = (0, 3, 2)
$$

The matrix becomes:

$$
A_2 =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

#### Step 3: Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)

Swap row $2$ and row $3$:

$$
A_3 =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

#### Step 4: Reversing Operations

1. The operation $R_2 \leftarrow R_2 - 2R_1$ is reversed by:

$$
R_2 \leftarrow R_2 + 2R_1
$$

2. The operation $R_3 \leftarrow R_3 + R_1$ is reversed by:

$$
R_3 \leftarrow R_3 - R_1
$$

3. The row swap $R_2 \leftrightarrow R_3$ is reversed by performing the same swap again:

$$
R_2 \leftrightarrow R_3
$$