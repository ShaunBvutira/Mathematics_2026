### Exercise 7. Choosing a Method Deliberately

---

### Solution

#### Part 1. One system with a triangular coefficient matrix

**Given System:**

$$
\begin{cases}
2x - y = 3, \\
4y = 8.
\end{cases}
$$

**Chosen Method:** **Back-substitution** (Direct solution from triangular form).

**Justification:** The coefficient matrix $A = \begin{pmatrix} 2 & -1 \\ 0 & 4 \end{pmatrix}$ is upper triangular. Forward elimination is already complete, making Gauss–Jordan elimination or matrix inversion redundant and inefficient.

**Complete Computation:**

1. **Solve for $y$ directly from row 2:**
   $$
   4y = 8 \implies y = \frac{8}{4} = 2
   $$

2. **Substitute $y = 2$ into row 1 to solve for $x$:**
   $$
   2x - (2) = 3 \implies 2x = 5 \implies x = \frac{5}{2}
   $$

**Final Solution Vector:**

$$
x = 
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{5}{2} \\
2 \\
\end{pmatrix}
$$

---

#### Part 2. Three systems $A x = b_i$ with the same matrix $A$ and known $A^{-1}$

**Chosen Method:** **Direct Matrix-Vector Multiplication** ($x_i = A^{-1}b_i$).

**Plan & Strategy:**
1. Compute each solution vector directly by evaluating $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$.
2. Alternatively, pack the right-hand sides into a matrix $B = \begin{pmatrix} b_1 & b_2 & b_3 \end{pmatrix}$ and perform a single matrix-matrix product $X = A^{-1}B$.

**Reusable vs. Unnecessary Computations:**
- **Reusable:** The known inverse $A^{-1}$ is computed once and reused across all three right-hand sides.
- **Unnecessary:** Performing Gaussian elimination three separate times on $[A \mid b_1]$, $[A \mid b_2]$, and $[A \mid b_3]$ is completely unnecessary, as it would redundantly reduce $A$ from scratch three times.

---

#### Part 3. One $3 \times 3$ system where $A^{-1}$ is unknown and a single solution is needed

**Chosen Method:** **Gaussian Elimination with Back-substitution** on $[A \mid b]$.

**Plan & Strategy:**
1. Form the augmented matrix $[A \mid b]$.
2. Perform row operations to reduce $[A \mid b]$ to row echelon form $[U \mid c]$.
3. Use back-substitution to solve for the unknown vector $x$.

**Reusable vs. Unnecessary Computations:**
- **Necessary Computation:** Reducing $[A \mid b]$ requires roughly $\frac{2}{3}n^3 = 18$ operations for a $3 \times 3$ system.
- **Unnecessary Computation:** Computing $A^{-1}$ first is completely unnecessary. Inverting $A$ via $[A \mid I]$ takes $\approx 2n^3 = 54$ operations (three times as much work) plus an extra matrix-vector multiplication $A^{-1}b$. Finding $A^{-1}$ is wasteful when only a single right-hand side $b$ needs to be solved.