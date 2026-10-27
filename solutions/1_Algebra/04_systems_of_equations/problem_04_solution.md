### Exercise 4. Matrix Multiplication and Noncommutativity

For

$$
A = 
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB = BA$? Use this example to explain what noncommutativity of matrix multiplication means.

---

### Solution

#### Step 1. Compute $AB$

Multiply matrix $A$ by matrix $B$:

$$
\begin{aligned}
AB &= 
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(2) + (2)(3) & (1)(0) + (2)(1) \\
(0)(2) + (1)(3) & (0)(0) + (1)(1) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 + 6 & 0 + 2 \\
0 + 3 & 0 + 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute $BA$

Multiply matrix $B$ by matrix $A$:

$$
\begin{aligned}
BA &= 
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(2)(1) + (0)(0) & (2)(2) + (0)(1) \\
(3)(1) + (1)(0) & (3)(2) + (1)(1) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 + 0 & 4 + 0 \\
3 + 0 & 6 + 1 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Compare $AB$ and $BA$

Comparing the two resulting matrices entry by entry:

$$
AB = 
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
= BA
$$

Therefore, $AB \neq BA$.

---

#### Step 4. Explain noncommutativity of matrix multiplication

In ordinary real-number arithmetic, multiplication is **commutative** ($ab = ba$ for all numbers $a$ and $b$).

However, matrix multiplication is generally **non-commutative**. This means that changing the order of the matrices in a product usually changes the final result:

$$
AB \neq BA
$$

**Why this happens:**
1. **Row-by-Column Combinations:** Entry $(i, j)$ of $AB$ is the dot product of the $i$-th row of $A$ and the $j$-th column of $B$. When the order is reversed to $BA$, entry $(i, j)$ becomes the dot product of the $i$-th row of $B$ and the $j$-th column of $A$, combining completely different numerical components.
2. **Order of Transformations:** Geometrically, matrix multiplication represents sequential transformations. The matrix $AB$ represents applying transformation $B$ first, followed by transformation $A$. In contrast, $BA$ represents applying transformation $A$ first, followed by transformation $B$. In geometry, applying linear actions in a different order leads to different final states.