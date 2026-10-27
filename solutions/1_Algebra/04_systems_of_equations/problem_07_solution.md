### Exercise 7. Identity Matrix, Zero Matrix, and Powers

For

$$
A = 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute $AI$, $IA$, $A + 0$, $A^2$, and $A^3$. Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

---

### Solution

#### Step 1. Compute $AI$, $IA$, and $A + 0$

Let $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ be the $2 \times 2$ identity matrix and $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ be the $2 \times 2$ zero matrix.

- **Compute $AI$:**

$$
\begin{aligned}
AI &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(2)(1) + (1)(0) & (2)(0) + (1)(1) \\
(0)(1) + (2)(0) & (0)(0) + (2)(1) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

- **Compute $IA$:**

$$
\begin{aligned}
IA &= 
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(2) + (0)(0) & (1)(1) + (0)(2) \\
(0)(2) + (1)(0) & (0)(1) + (1)(2) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

- **Compute $A + 0$:**

$$
\begin{aligned}
A + 0 &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
+
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
2 + 0 & 1 + 0 \\
0 + 0 & 2 + 0 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute the matrix powers $A^2$ and $A^3$

- **Compute $A^2 = A A$:**

$$
\begin{aligned}
A^2 &= 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
(2)(2) + (1)(0) & (2)(1) + (1)(2) \\
(0)(2) + (2)(0) & (0)(1) + (2)(2) \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
4 & 2 + 2 \\
0 & 4 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\end{aligned}
$$

- **Compute $A^3 = A^2 A$:**

$$
\begin{aligned}
A^3 &= 
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
(4)(2) + (4)(0) & (4)(1) + (4)(2) \\
(0)(2) + (4)(0) & (0)(1) + (4)(2) \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
8 & 4 + 8 \\
0 & 8 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Explain the roles of $I$ and $0$

1. **Role of $I$ (Multiplicative Identity):** 
   The identity matrix $I$ acts like the real number $1$ under multiplication. For any square matrix $A$, multiplying by $I$ on either the left or the right leaves the matrix unchanged:
   $$
   AI = IA = A
   $$

2. **Role of $0$ (Additive Identity):** 
   The zero matrix $0$ acts like the real number $0$ under addition. Adding $0$ to any matrix $A$ of the same size leaves the matrix unchanged:
   $$
   A + 0 = A
   $$

---

#### Step 4. Describe the pattern observed in successive powers of $A$

Writing out $A^1$, $A^2$, and $A^3$ side-by-side:

$$
A^1 = 
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}, \quad 
A^2 = 
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}, \quad 
A^3 = 
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

Rewriting the entries in terms of the power $n$:

- **Main diagonal entries:** The diagonal elements are powers of $2$, specifically $2^n$.
- **Bottom-left entry:** Remains $0$ for all powers (preserving the upper-triangular structure).
- **Top-right entry:** The values are $1, 4, 12, \dots$, which follow the formula $n \cdot 2^{n-1}$:
  - For $n=1$: $1 \cdot 2^{1-1} = 1 \cdot 1 = 1$
  - For $n=2$: $2 \cdot 2^{2-1} = 2 \cdot 2 = 4$
  - For $n=3$: $3 \cdot 2^{3-1} = 3 \cdot 4 = 12$

Thus, the general pattern for the $n$-th power $A^n$ is:

$$
A^n = 
\begin{pmatrix}
2^n & n \cdot 2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$