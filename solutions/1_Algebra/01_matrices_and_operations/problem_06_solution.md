### Exercise 6. Transpose

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},
\quad
B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^\mathrm{T}$, $B^\mathrm{T}$, and $AB$. Then verify in this example that $(AB)^\mathrm{T} = B^\mathrm{T} A^\mathrm{T}$.

---

### Solution

#### Step 1: Compute $A^\mathrm{T}$

The rows of $A$ ($2 \times 3$) become the columns of $A^\mathrm{T}$ ($3 \times 2$):

$$
A^\mathrm{T}=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

#### Step 2: Compute $B^\mathrm{T}$

The rows of $B$ ($3 \times 2$) become the columns of $B^\mathrm{T}$ ($2 \times 3$):

$$
B^\mathrm{T}=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

#### Step 3: Compute $AB$

Multiply $A$ ($2 \times 3$) and $B$ ($3 \times 2$) to obtain a $2 \times 2$ matrix:

$$
AB =
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
(1)(1) + (2)(2) + (3)(-1) & (1)(0) + (2)(1) + (3)(3) \\
(4)(1) + (5)(2) + (6)(-1) & (4)(0) + (5)(1) + (6)(3) \\
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
1 + 4 - 3 & 0 + 2 + 9 \\
4 + 10 - 6 & 0 + 5 + 18 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}
$$

#### Step 4: Compute $(AB)^\mathrm{T}$

Transpose the resulting matrix $AB$:

$$
(AB)^\mathrm{T} =
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

#### Step 5: Compute $B^\mathrm{T} A^\mathrm{T}$

Multiply $B^\mathrm{T}$ ($2 \times 3$) and $A^\mathrm{T}$ ($3 \times 2$):

$$
B^\mathrm{T} A^\mathrm{T} =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}
$$

$$
B^\mathrm{T} A^\mathrm{T} =
\begin{pmatrix}
(1)(1) + (2)(2) + (-1)(3) & (1)(4) + (2)(5) + (-1)(6) \\
(0)(1) + (1)(2) + (3)(3) & (0)(4) + (1)(5) + (3)(6) \\
\end{pmatrix}
$$

$$
B^\mathrm{T} A^\mathrm{T} =
\begin{pmatrix}
1 + 4 - 3 & 4 + 10 - 6 \\
0 + 2 + 9 & 0 + 5 + 18 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

#### Step 6: Verification

Comparing $(AB)^\mathrm{T}$ and $B^\mathrm{T} A^\mathrm{T}$:

$$
(AB)^\mathrm{T} =
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
= B^\mathrm{T} A^\mathrm{T}
$$

The identity $(AB)^\mathrm{T} = B^\mathrm{T} A^\mathrm{T}$ is verified.
