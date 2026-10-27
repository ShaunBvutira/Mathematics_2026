### Exercise 2. Determinant of a 3×3 Matrix

For

$$
A = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

---

### Solution

#### Step 1. Apply Sarrus' Rule

For a $3 \times 3$ matrix

$$
M = 
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i \\
\end{pmatrix}
$$

Sarrus' rule computes the determinant by summing the products of the main diagonals and subtracting the products of the anti-diagonals:

$$
\det M = (aei + bfg + cdh) - (ceg + afh + bdi)
$$

For matrix $A$:

$$
A = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

Calculate the products of the three main diagonals:

$$
\begin{aligned}
d_1 &= (1)(3)(5) = 15 \\
d_2 &= (2)(4)(2) = 16 \\
d_3 &= (-1)(0)(1) = 0
\end{aligned}
$$

Sum of main diagonal products:

$$
15 + 16 + 0 = 31
$$

Calculate the products of the three anti-diagonals:

$$
\begin{aligned}
a_1 &= (-1)(3)(2) = -6 \\
a_2 &= (1)(4)(1) = 4 \\
a_3 &= (2)(0)(5) = 0
\end{aligned}
$$

Sum of anti-diagonal products:

$$
(-6) + 4 + 0 = -2
$$

Subtract the sum of anti-diagonal products from the sum of main diagonal products:

$$
\begin{aligned}
\det A &= 31 - (-2) \\
       &= 31 + 2 \\
       &= 33
\end{aligned}
$$

---

#### Step 2. Check using Laplace Expansion along Row 1

To verify the result using a fundamental property of determinants, expand $\det A$ along the first row (which benefits from the zero entry in the first column):

$$
\det A = 1 \cdot \det 
\begin{pmatrix}
3 & 4 \\
1 & 5 \\
\end{pmatrix}
- 2 \cdot \det 
\begin{pmatrix}
0 & 4 \\
2 & 5 \\
\end{pmatrix}
+ (-1) \cdot \det 
\begin{pmatrix}
0 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

Evaluate each $2 \times 2$ minor determinant:

$$
\begin{aligned}
\det 
\begin{pmatrix}
3 & 4 \\
1 & 5 \\
\end{pmatrix} 
&= (3)(5) - (4)(1) = 15 - 4 = 11 \\
\det 
\begin{pmatrix}
0 & 4 \\
2 & 5 \\
\end{pmatrix} 
&= (0)(5) - (4)(2) = 0 - 8 = -8 \\
\det 
\begin{pmatrix}
0 & 3 \\
2 & 1 \\
\end{pmatrix} 
&= (0)(1) - (3)(2) = 0 - 6 = -6
\end{aligned}
$$

Substitute the minors back into the row expansion:

$$
\begin{aligned}
\det A &= 1(11) - 2(-8) - 1(-6) \\
       &= 11 + 16 + 6 \\
       &= 33
\end{aligned}
$$

Both methods yield $\det A = 33$, confirming the result.