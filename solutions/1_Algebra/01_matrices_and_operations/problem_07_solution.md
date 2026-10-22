### Exercise 7. Identity Matrix, Zero Matrix, and Powers

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute $AI$, $IA$, $A+0$, $A^2$, and $A^3$. Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

---

### Solution

#### Step 1: Compute $AI$ and $IA$

The $2 \times 2$ identity matrix is:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

Compute $AI$:

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
=
\begin{pmatrix}
(2)(1)+(1)(0) & (2)(0)+(1)(1) \\
(0)(1)+(2)(0) & (0)(0)+(2)(1) \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

Compute $IA$:

$$
IA=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
=
\begin{pmatrix}
(1)(2)+(0)(0) & (1)(1)+(0)(2) \\
(0)(2)+(1)(0) & (0)(1)+(1)(2) \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

#### Step 2: Compute $A+0$

The $2 \times 2$ zero matrix is:

$$
0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

Compute $A+0$:

$$
A+0=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
+
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
=
\begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix}
=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

#### Step 3: Compute $A^2$

$$
A^2=AA=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

$$
A^2=
\begin{pmatrix}
(2)(2)+(1)(0) & (2)(1)+(1)(2) \\
(0)(2)+(2)(0) & (0)(1)+(2)(2) \\
\end{pmatrix}
=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

#### Step 4: Compute $A^3$

$$
A^3=A^2 A=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

$$
A^3=
\begin{pmatrix}
(4)(2)+(4)(0) & (4)(1)+(4)(2) \\
(0)(2)+(4)(0) & (0)(1)+(4)(2) \\
\end{pmatrix}
=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

#### Step 5: Roles of $I$ and $0$

- **Identity Matrix $I$:** Serves as the multiplicative identity element for matrix multiplication, meaning $AI = IA = A$ for any square matrix $A$.
- **Zero Matrix $0$:** Serves as the additive identity element for matrix addition, meaning $A + 0 = A$ for any matrix $A$.

#### Step 6: Pattern in Successive Powers of $A$

Examining $A$, $A^2$, and $A^3$:

$$
A^1 =
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
\quad
A^2 =
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},
\quad
A^3 =
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

For a general integer power $k \ge 1$:

- The main diagonal entries are equal to $2^k$.
- The bottom-left entry remains $0$.
- The top-right entry equals $k \cdot 2^{k-1}$.

Thus, the general formula for $A^k$ is:

$$
A^k =
\begin{pmatrix}
2^k & k \cdot 2^{k-1} \\
0 & 2^k \\
\end{pmatrix}
$$