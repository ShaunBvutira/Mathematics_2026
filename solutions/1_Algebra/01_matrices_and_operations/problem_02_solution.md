### Exercise 2. Addition and Scalar Multiplication

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},
\quad
B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute $A+B$, $A-B$, and $3A-2B$. Explain why matrix addition is possible only for matrices of the same size.

---

### Solution

#### Step 1: Computation of $A+B$

$$
A+B =
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}
=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
$$

#### Step 2: Computation of $A-B$

$$
A-B =
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}
=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
$$

#### Step 3: Computation of $3A-2B$

$$
3A =
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},
\quad
2B =
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

$$
3A-2B =
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix}
=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
$$

#### Step 4: Explanation

Matrix addition is defined element-wise:

$$
(A+B)_{ij} = A_{ij} + B_{ij}
$$

If matrices are of different sizes, corresponding entries $A_{ij}$ and $B_{ij}$ do not exist for every position, making the addition undefined.
