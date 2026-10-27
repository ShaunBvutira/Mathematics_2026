### Exercise 1. Definition of the Inverse

For

$$
A = 
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

---

### Solution

#### Step 1. State the definition of the matrix inverse

By definition, a square matrix $B$ is the inverse of an $n \times n$ matrix $A$ (denoted $B = A^{-1}$) if and only if both of the following matrix products yield the identity matrix $I$:

$$
AB = I \quad \text{and} \quad BA = I
$$

For a $2 \times 2$ matrix, the identity matrix is:

$$
I = 
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

---

#### Step 2. Compute the product AB

Multiply $A$ by $B$:

$$
\begin{aligned}
AB &= 
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\
(1)(1) + (1)(-1) & (1)(-1) + (1)(2) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 - 1 & -2 + 2 \\
1 - 1 & -1 + 2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Thus, $AB = I$.

---

#### Step 3. Compute the product BA

Multiply $B$ by $A$:

$$
\begin{aligned}
BA &= 
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\
(-1)(2) + (2)(1) & (-1)(1) + (2)(1) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 - 1 & 1 - 1 \\
-2 + 2 & -1 + 2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Thus, $BA = I$.

---

#### Step 4. Relate to the definition and conclude

Since both $AB = I$ and $BA = I$, the matrix $B$ satisfies the formal definition of the matrix inverse. 

Therefore:

$$
B = A^{-1}
$$