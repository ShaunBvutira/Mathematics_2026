### Exercise 8. Two Systems with the Same Coefficient Matrix

Solve by elimination the two systems:

$$
\text{System 1: }
\begin{cases}
2x + y = 5, \\
x - y = 1.
\end{cases}
\quad
\text{System 2: }
\begin{cases}
2x + y = 1, \\
x - y = 4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

---

### Solution

#### Step 1. Solve System 1 using elimination

- **Form augmented matrix $[A \mid b_1]$:**

$$
[A \mid b_1] = 
\begin{pmatrix}
2 & 1 & \mid & 5 \\
1 & -1 & \mid & 1 \\
\end{pmatrix}
$$

- **Eliminate $x$ from Row 2:**

Swap $R_1 \leftrightarrow R_2$ to set up a pivot of $1$:

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
2 & 1 & \mid & 5 \\
\end{pmatrix}
$$

Perform $R_2 \leftarrow R_2 - 2R_1$:
- Row 2: $(2 - 2(1), 1 - 2(-1) \mid 5 - 2(1)) = (0, 3 \mid 3)$

$$
\begin{pmatrix}
1 & -1 & \mid & 1 \\
0 & 3 & \mid & 3 \\
\end{pmatrix}
$$

- **Back-substitution:**
  1. $3y = 3 \implies y = 1$
  2. $x - y = 1 \implies x - 1 = 1 \implies x = 2$

$$
\text{Solution 1: } 
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

---

#### Step 2. Solve System 2 using elimination

- **Form augmented matrix $[A \mid b_2]$:**

$$
[A \mid b_2] = 
\begin{pmatrix}
2 & 1 & \mid & 1 \\
1 & -1 & \mid & 4 \\
\end{pmatrix}
$$

- **Eliminate $x$ from Row 2:**

Swap $R_1 \leftrightarrow R_2$:

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
2 & 1 & \mid & 1 \\
\end{pmatrix}
$$

Perform $R_2 \leftarrow R_2 - 2R_1$:
- Row 2: $(2 - 2(1), 1 - 2(-1) \mid 1 - 2(4)) = (0, 3 \mid -7)$

$$
\begin{pmatrix}
1 & -1 & \mid & 4 \\
0 & 3 & \mid & -7 \\
\end{pmatrix}
$$

- **Back-substitution:**
  1. $3y = -7 \implies y = -\frac{7}{3}$
  2. $x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = \frac{12}{3} \implies x = \frac{5}{3}$

$$
\text{Solution 2: } 
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{5}{3} \\
-\frac{7}{3} \\
\end{pmatrix}
$$

---

#### Step 3. Compare elimination steps and explain identical operations

- **Comparison:**
  In both systems, the exact same sequence of row operations was applied:
  1. Row swap: $R_1 \leftrightarrow R_2$
  2. Row elimination: $R_2 \leftarrow R_2 - 2R_1$

  As a result, the left-hand coefficient side of the augmented matrix transformed identically in both cases:

$$
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix}
\xrightarrow{R_1 \leftrightarrow R_2}
\begin{pmatrix}
1 & -1 \\
2 & 1 \\
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\begin{pmatrix}
1 & -1 \\
0 & 3 \\
\end{pmatrix}
$$

- **Why this happens:**
  Elementary row operations depend **only on the coefficient matrix $A$**. Because both systems share the exact same coefficient matrix $A = \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$, the row multipliers and pivot choices required to reach upper-triangular form are identical. 

  The right-hand side vectors $b_1 = \begin{pmatrix} 5 \\ 1 \end{pmatrix}$ and $b_2 = \begin{pmatrix} 1 \\ 4 \end{pmatrix}$ simply follow along and undergo the same linear operations. 

*(Note: To avoid repeating steps when solving multiple systems with the same coefficient matrix $A$, one can combine right-hand sides into a single joint matrix $[A \mid b_1 \ b_2]$ and reduce both simultaneously).*