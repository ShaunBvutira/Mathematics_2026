### Exercise 2. Formula for a 2×2 Matrix

Find the inverse of

$$
A = 
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2 \times 2$ matrix. At the end, check the result by computing one product with $A$.

---

### Solution

#### Step 1. State the inverse formula for a 2×2 matrix

For any $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse exists if $\det M = ad - bc \neq 0$ and is given by:

$$
M^{-1} = \frac{1}{\det M}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}
$$

---

#### Step 2. Compute the determinant of matrix A

For matrix $A = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}$:

$$
\begin{aligned}
\det A &= (3)(4) - (2)(5) \\
       &= 12 - 10 \\
       &= 2
\end{aligned}
$$

Since $\det A = 2 \neq 0$, the inverse $A^{-1}$ exists.

---

#### Step 3. Apply the inverse formula

Swap the main diagonal elements ($a$ and $d$), negate the off-diagonal elements ($b$ and $c$), and multiply by $\frac{1}{\det A}$:

$$
\begin{aligned}
A^{-1} &= \frac{1}{2}
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} \\
       &= 
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 4. Verify the result by computing $A A^{-1}$

Multiply $A$ by $A^{-1}$ to confirm the product yields the identity matrix $I$:

$$
\begin{aligned}
A A^{-1} &= 
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2} \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
(3)(2) + (2)\left(-\frac{5}{2}\right) & (3)(-1) + (2)\left(\frac{3}{2}\right) \\
(5)(2) + (4)\left(-\frac{5}{2}\right) & (5)(-1) + (4)\left(\frac{3}{2}\right) \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
6 - 5 & -3 + 3 \\
10 - 10 & -5 + 6 \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Since $A A^{-1} = I$, the calculated inverse $A^{-1}$ is correct.