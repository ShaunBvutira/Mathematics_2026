### Exercise 9. Matrix Equation

Given

$$
A = 
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX = B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

---

### Solution

#### Step 1. Determine which side to multiply by $A^{-1}$

Because matrix multiplication is non-commutative ($AX \neq XA$), we must be careful with the placement of inverse matrices.

We are given:

$$
AX = B
$$

To isolate $X$, we must eliminate $A$ from the left side of $X$. Therefore, we must multiply by $A^{-1}$ from the **left** (left-multiplication):

$$
A^{-1}(AX) = A^{-1}B
$$

Using the associative property:

$$
(A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B
$$

Multiplying from the right ($AXA^{-1}$) would not isolate $X$. Thus, $A^{-1}$ must be used on the **left side** of $B$.

---

#### Step 2. Compute the inverse matrix $A^{-1}$

For matrix $A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$:

$$
\det A = (1)(1) - (2)(0) = 1
$$

Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
= 
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
$$

---

#### Step 3. Solve for $X$

Multiply $A^{-1}$ by $B$:

$$
\begin{aligned}
X &= A^{-1} B \\
  &= 
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
  &= 
\begin{pmatrix}
(1)(3) + (-2)(2) & (1)(1) + (-2)(4) \\
(0)(3) + (1)(2) & (0)(1) + (1)(4) \\
\end{pmatrix} \\
  &= 
\begin{pmatrix}
3 - 4 & 1 - 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} \\
  &= 
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 4. Check the result by computing $AX$

Multiply matrix $A$ by the computed solution matrix $X$:

$$
\begin{aligned}
AX &= 
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(-1) + (2)(2) & (1)(-7) + (2)(4) \\
(0)(-1) + (1)(2) & (0)(-7) + (1)(4) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
-1 + 4 & -7 + 8 \\
0 + 2 & 0 + 4 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} \\
   &= B
\end{aligned}
$$

Since $AX = B$, the solution $X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$ is verified.