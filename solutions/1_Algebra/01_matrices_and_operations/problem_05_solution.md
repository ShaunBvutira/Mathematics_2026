### Exercise 5. Matrix Times Vector

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},
\quad
x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

---

### Solution

#### Step 1: Standard matrix-vector multiplication

$$
Ax =
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
(2)(4) + (-1)(2) \\
(1)(4) + (3)(2) \\
\end{pmatrix}
=
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

#### Step 2: Linear combination of columns

Let the columns of $A$ be $a_1$ and $a_2$:

$$
a_1 =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},
\quad
a_2 =
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

The vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 4 \\ 2 \end{pmatrix}$ provides the coefficients:

$$
Ax = x_1 a_1 + x_2 a_2
$$

$$
Ax = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

#### Step 3: Verification

$$
4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

The linear combination matches the computed matrix-vector product $Ax$.