### Exercise 2. Addition and Scalar Multiplication

For

$$
A = 
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute $A+B$, $A-B$, and $3A-2B$. Explain why matrix addition is possible only for matrices of the same size.

---

### Solution

#### Step 1. Compute $A+B$

Matrix addition is performed entrywise by adding corresponding elements:

$$
\begin{aligned}
A + B &= 
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
+
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
1 + 4 & 2 + (-2) \\
-1 + 0 & 3 + 5 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute $A-B$

Matrix subtraction is performed entrywise by subtracting corresponding elements:

$$
\begin{aligned}
A - B &= 
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
-
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
1 - 4 & 2 - (-2) \\
-1 - 0 & 3 - 5 \\
\end{pmatrix} \\
      &= 
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Compute $3A-2B$

First, compute scalar multiples $3A$ and $2B$:

$$
3A = 3
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}
= 
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}
$$

$$
2B = 2
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
= 
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

Now perform the subtraction $3A - 2B$:

$$
\begin{aligned}
3A - 2B &= 
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}
-
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
3 - 8 & 6 - (-4) \\
-3 - 0 & 9 - 10 \\
\end{pmatrix} \\
        &= 
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 4. Explain why addition requires matrices of the same size

By definition, matrix addition is an **element-wise operation**: the entry $(A+B)_{ij}$ in row $i$ and column $j$ of the sum is obtained by adding the entry $a_{ij}$ from $A$ to the entry $b_{ij}$ from $B$:

$$
(A+B)_{ij} = a_{ij} + b_{ij}
$$

If matrix $A$ and matrix $B$ have different dimensions (different numbers of rows or columns), there will be entries in one matrix that have no corresponding entry in the other matrix. Because every entry $a_{ij}$ must pair with a matching entry $b_{ij}$, matrix addition is defined if and only if both matrices have identical dimensions ($m \times n$).