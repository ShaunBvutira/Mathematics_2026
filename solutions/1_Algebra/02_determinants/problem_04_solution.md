### Exercise 4. Triangular Matrix

Without expanding the determinant, compute

$$
\det 
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

---

### Solution

#### Step 1. State the rule for triangular matrices

**Rule:** The determinant of any triangular matrix (upper triangular, lower triangular, or diagonal) is equal to the product of the entries on its main diagonal.

For an arbitrary $n \times n$ triangular matrix $T$ with diagonal entries $t_{11}, t_{22}, \dots, t_{nn}$, the rule is:

$$
\det T = \prod_{i=1}^{n} t_{ii} = t_{11} \cdot t_{22} \cdots t_{nn}
$$

---

#### Step 2. Compute the determinant using the rule

Let the matrix be:

$$
A = 
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}
$$

Matrix $A$ is an **upper triangular matrix** because all entries below the main diagonal are equal to zero. 

Applying the main diagonal product rule directly:

$$
\begin{aligned}
\det A &= (2)(-3)(7) \\
       &= -6 \cdot 7 \\
       &= -42
\end{aligned}
$$

---

#### Step 3. Explain the rule using this example

The rule works because of cofactor expansion (Laplace expansion). If we expand along the first column of matrix $A$, all entries below the first element are zero:

$$
\det A = 2 \cdot \det 
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
- 0 \cdot \det 
\begin{pmatrix}
4 & 1 \\
0 & 7 \\
\end{pmatrix}
+ 0 \cdot \det 
\begin{pmatrix}
4 & 1 \\
-3 & 5 \\
\end{pmatrix}
$$

Since the zero terms drop out:

$$
\det A = 2 \cdot \det 
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
$$

Expanding the remaining $2 \times 2$ determinant along its first column yields:

$$
\det 
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix}
= (-3)(7) - (5)(0) = (-3)(7)
$$

Substituting this back gives the product of the diagonal elements:

$$
\det A = (2)(-3)(7) = -42
$$

Because all non-diagonal elements in the expansion column or row are zero, every step of Laplace expansion reduces the determinant to the product of the next diagonal entry, isolating the main diagonal.