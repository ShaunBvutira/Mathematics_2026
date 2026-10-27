### Exercise 6. Solving a System Using the Inverse

Solve

$$
A x = b,
$$

where

$$
A = 
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}, \quad 
b = 
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x = A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

---

### Solution

#### Step 1. Compute the inverse matrix $A^{-1}$

For the $2 \times 2$ matrix $A = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}$, compute its determinant:

$$
\begin{aligned}
\det A &= (2)(3) - (1)(1) \\
       &= 6 - 1 \\
       &= 5
\end{aligned}
$$

Since $\det A = 5 \neq 0$, the inverse matrix $A^{-1}$ exists and is given by the formula:

$$
\begin{aligned}
A^{-1} &= \frac{1}{\det A}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix} \\
       &= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Solve for $x$ using $x = A^{-1}b$

Multiply the inverse matrix $A^{-1}$ by vector $b$:

$$
\begin{aligned}
x &= A^{-1} b \\
  &= \frac{1}{5}
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} \\
  &= \frac{1}{5}
\begin{pmatrix}
(3)(5) + (-1)(7) \\
(-1)(5) + (2)(7) \\
\end{pmatrix} \\
  &= \frac{1}{5}
\begin{pmatrix}
15 - 7 \\
-5 + 14 \\
\end{pmatrix} \\
  &= \frac{1}{5}
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix} \\
  &= 
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Substitute $x$ back into $A x = b$ to verify

Multiply matrix $A$ by the calculated vector $x$:

$$
\begin{aligned}
A x &= 
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac{8}{5} \\
\frac{9}{5} \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
(2)\left(\frac{8}{5}\right) + (1)\left(\frac{9}{5}\right) \\
(1)\left(\frac{8}{5}\right) + (3)\left(\frac{9}{5}\right) \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
\frac{16}{5} + \frac{9}{5} \\
\frac{8}{5} + \frac{27}{5} \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}
\end{aligned}
$$

Since $A x = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b$, the solution $x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}$ is verified.