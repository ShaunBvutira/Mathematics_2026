### Exercise 3. Swapping Two Rows

For

$$
A = 
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$. First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

---

### Solution

#### Step 1. Compute the determinant of matrix A

Expand along the first row of matrix $A$:

$$
\det A = 1 \cdot \det 
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix}
- 2 \cdot \det 
\begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix}
+ 0 \cdot \det 
\begin{pmatrix}
0 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

Compute the $2 \times 2$ determinants:

$$
\begin{aligned}
\det 
\begin{pmatrix}
3 & 1 \\
1 & 1 \\
\end{pmatrix} 
&= (3)(1) - (1)(1) = 3 - 1 = 2 \\
\det 
\begin{pmatrix}
0 & 1 \\
2 & 1 \\
\end{pmatrix} 
&= (0)(1) - (1)(2) = 0 - 2 = -2
\end{aligned}
$$

Substitute these values into the expansion:

$$
\begin{aligned}
\det A &= 1(2) - 2(-2) \\
       &= 2 + 4 \\
       &= 6
\end{aligned}
$$

Thus, $\det A = 6$.

---

#### Step 2. Predict the determinant of matrix B

 Matrix $B$ is formed by swapping Row 1 and Row 2 of matrix $A$:

$$
B = 
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

**Property of Determinants:** Swapping any two rows of a square matrix multiplies its determinant by $-1$.

**Prediction:**

$$
\det B = -\det A = -6
$$

---

#### Step 3. Verify the prediction by direct calculation

Expand $\det B$ along its first row:

$$
\det B = 0 \cdot \det 
\begin{pmatrix}
2 & 0 \\
1 & 1 \\
\end{pmatrix}
- 3 \cdot \det 
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
\end{pmatrix}
+ 1 \cdot \det 
\begin{pmatrix}
1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

Compute the $2 \times 2$ determinants:

$$
\begin{aligned}
\det 
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
\end{pmatrix} 
&= (1)(1) - (0)(2) = 1 - 0 = 1 \\
\det 
\begin{pmatrix}
1 & 2 \\
2 & 1 \\
\end{pmatrix} 
&= (1)(1) - (2)(2) = 1 - 4 = -3
\end{aligned}
$$

Substitute these values into the expansion:

$$
\begin{aligned}
\det B &= 0 - 3(1) + 1(-3) \\
       &= -3 - 3 \\
       &= -6
\end{aligned}
$$

The direct calculation yields $\det B = -6$, which confirms the prediction made using the determinant row-swap property.