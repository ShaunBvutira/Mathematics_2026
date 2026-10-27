### Exercise 10. Inverse of a Diagonal Matrix

Given

$$
D = 
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}, \quad 
E = 
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

---

### Solution

#### Step 1. Determine invertibility of diagonal matrices

**Rule:** A diagonal matrix is invertible if and only if **all** of its diagonal entries are non-zero. 

- For matrix $D$: The diagonal entries are $2, -3, 5$. Since none of these entries are zero, matrix $D$ is **invertible**.
- For matrix $E$: The second diagonal entry is $0$. Since it has a zero on the main diagonal, $\det E = (2)(0)(5) = 0$, so matrix $E$ is **not invertible**.

---

#### Step 2. Compute the inverse of matrix $D$

For any invertible diagonal matrix $D = \mathrm{diag}(d_1, d_2, \dots, d_n)$, its inverse is formed by taking the reciprocal of each main diagonal entry:

$$
D^{-1} = 
\begin{pmatrix}
\frac{1}{d_1} & 0 & 0 \\
0 & \frac{1}{d_2} & 0 \\
0 & 0 & \frac{1}{d_n} \\
\end{pmatrix}
$$

Applying this rule to matrix $D$:

$$
D^{-1} = 
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix}
$$

---

#### Step 3. Check the result by multiplication

Multiply matrix $D$ by $D^{-1}$ to confirm the product yields the identity matrix $I$:

$$
\begin{aligned}
D D^{-1} &= 
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5} \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
(2)\left(\frac{1}{2}\right) & 0 & 0 \\
0 & (-3)\left(-\frac{1}{3}\right) & 0 \\
0 & 0 & (5)\left(\frac{1}{5}\right) \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Since $D D^{-1} = I$, the inverse matrix $D^{-1}$ is verified.