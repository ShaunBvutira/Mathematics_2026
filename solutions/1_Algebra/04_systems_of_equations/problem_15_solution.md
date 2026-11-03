### Exercise 15. Classifying Three Systems

---

### Solution

#### System 1

$$
\begin{cases}
x + y = 2, \\
x - y = 0.
\end{cases}
$$

- **Form augmented matrix:**

$$
[A_1 \mid b_1] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
1 & -1 & \mid & 0 \\
\end{pmatrix}
$$

- **Perform minimal elimination ($R_2 \leftarrow R_2 - R_1$):**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}
$$

- **Classification & Justification:** **Exactly one solution (Unique solution)**.
  - **Reasoning:** The reduced matrix has $2$ non-zero rows with pivots in both variable columns (column 1 for $x$ and column 2 for $y$). Since the number of pivots ($2$) equals the number of variables ($2$), there are no free variables and no inconsistent rows.

---

#### System 2

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4.
\end{cases}
$$

- **Form augmented matrix:**

$$
[A_2 \mid b_2] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 4 \\
\end{pmatrix}
$$

- **Perform minimal elimination ($R_2 \leftarrow R_2 - 2R_1$):**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

- **Classification & Justification:** **Infinitely many solutions**.
  - **Reasoning:** Row 2 reduces to $[0 \ 0 \mid 0]$, which indicates that the second equation is completely redundant (a scalar multiple of the first). There is only $1$ pivot (column 1 for $x$), leaving column 2 ($y$) as a free variable with no contradictions.

---

#### System 3

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

- **Form augmented matrix:**

$$
[A_3 \mid b_3] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & 2 & \mid & 5 \\
\end{pmatrix}
$$

- **Perform minimal elimination ($R_2 \leftarrow R_2 - 2R_1$):**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

- **Classification & Justification:** **No solution (Inconsistent)**.
  - **Reasoning:** Row 2 yields the contradictory row $[0 \ 0 \mid 1]$, which represents the equation $0x + 0y = 1 \implies 0 = 1$. Since $0$ can never equal $1$, no values of $x$ and $y$ can satisfy the system.