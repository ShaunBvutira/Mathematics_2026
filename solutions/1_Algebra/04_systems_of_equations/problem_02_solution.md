### Exercise 1. From a System to a Matrix

Write the system

$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

in the form $Ax = b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

---

### Solution

#### Step 1. Express the system in matrix form $Ax = b$

Writing the system of linear equations as a matrix equation $Ax = b$:

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

---

#### Step 2. Identify $A$, $x$, and $b$

- **Coefficient Matrix ($A$):** The $3 \times 3$ matrix containing the numerical coefficients of the variables:

$$
A = 
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
$$

- **Vector of Unknowns ($x$):** The $3 \times 1$ column vector containing the variables:

$$
x = 
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
$$

- **Right-Hand Side Vector ($b$):** The $3 \times 1$ column vector containing the constant terms:

$$
b = 
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}
$$

---

#### Step 3. Explain how each row corresponds to one equation

By the definition of matrix-vector multiplication, computing row $i$ of the product $Ax$ takes the dot product of the $i$-th row vector of $A$ with the variable vector $x$:

- **Row 1:** $(2, -1, 1) \cdot (x, y, z)^T = 2x - y + z = 4$ (first equation)
- **Row 2:** $(1, 3, -2) \cdot (x, y, z)^T = x + 3y - 2z = 1$ (second equation)
- **Row 3:** $(3, 1, 1) \cdot (x, y, z)^T = 3x + y + z = 7$ (third equation)

Thus, each row of the coefficient matrix $A$ holds the exact coefficients for the variables in the corresponding linear equation, while the matching row entry in $b$ provides the equation's constant target value.