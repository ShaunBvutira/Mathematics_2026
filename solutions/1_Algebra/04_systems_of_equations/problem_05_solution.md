### Exercise 5. Matrix Times Vector

Let

$$
A = 
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}, \quad 
x = 
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

---

### Solution

#### Step 1. Compute $Ax$ using row-by-column multiplication

Multiply matrix $A$ by vector $x$:

$$
\begin{aligned}
Ax &= 
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(2)(4) + (-1)(2) \\
(1)(4) + (3)(2) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Identify the columns of $A$ and components of $x$

- Columns of matrix $A$:

$$
v_1 = 
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}, \quad 
v_2 = 
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

- Components of vector $x$:

$$
x_1 = 4, \quad x_2 = 2
$$

---

#### Step 3. Express $Ax$ as a linear combination of the columns of $A$

By definition of matrix-vector multiplication, the product $Ax$ can be written as a linear combination of the columns of $A$ weighted by the entries of $x$:

$$
Ax = x_1 v_1 + x_2 v_2
$$

Substituting the specific vectors and coefficients:

$$
Ax = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

---

#### Step 4. Verify the linear combination

Evaluate the linear combination to confirm it equals the computed product:

$$
\begin{aligned}
4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
&= 
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+ 
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix} \\
&= 
\begin{pmatrix}
8 - 2 \\
4 + 6 \\
\end{pmatrix} \\
&= 
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
\end{aligned}
$$

Both methods yield the vector $\begin{pmatrix} 6 \\ 10 \end{pmatrix}$.