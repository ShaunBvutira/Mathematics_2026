### Exercise 4. Gauss–Jordan

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A = 
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A \mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid I]$

Place the matrix $A$ and the $2 \times 2$ identity matrix $I$ side by side:

$$
[A \mid I] = 
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

---

#### Step 2. Apply elementary row operations

**Step 2.1:** Eliminate the entry below the top-left pivot ($a_{21} = 3$).

Perform $R_2 \leftarrow R_2 - 3 R_1$:

- Row 2 calculation: $(3 - 3(1), 5 - 3(2) \mid 0 - 3(1), 1 - 3(0)) = (0, -1 \mid -3, 1)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

---

**Step 2.2:** Make the second pivot equal to $1$.

Perform $R_2 \leftarrow -1 \cdot R_2$:

- Row 2 calculation: $(-1 \cdot 0, -1 \cdot (-1) \mid -1 \cdot (-3), -1 \cdot 1) = (0, 1 \mid 3, -1)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

---

**Step 2.3:** Eliminate the entry above the second pivot ($a_{12} = 2$).

Perform $R_1 \leftarrow R_1 - 2 R_2$:

- Row 1 calculation: $(1 - 2(0), 2 - 2(1) \mid 1 - 2(3), 0 - 2(-1)) = (1, 0 \mid -5, 2)$

The augmented matrix is now in reduced row echelon form $[I \mid A^{-1}]$:

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

Thus, the inverse matrix is:

$$
A^{-1} = 
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}
$$

---

#### Step 3. Explain why obtaining $I$ on the left gives $A^{-1}$ on the right

Every elementary row operation corresponds to premultiplying a matrix by an elementary matrix $E_k$. 

Applying a sequence of row operations $E_1, E_2, \dots, E_k$ to the augmented matrix $[A \mid I]$ is equivalent to multiplying both halves of the augmented matrix by the combined operation matrix $M = E_k \cdots E_2 E_1$:

$$
M [A \mid I] = [M A \mid M I] = [M A \mid M]
$$

When the row operations successfully transform the left side into the identity matrix $I$:

$$
M A = I
$$

By definition of the matrix inverse, the matrix $M$ that transforms $A$ into $I$ must be $A^{-1}$. Therefore, the right side of the augmented matrix becomes:

$$
M = A^{-1}
$$

Hence, transforming $[A \mid I] \to [I \mid A^{-1}]$ automatically leaves the inverse matrix $A^{-1}$ on the right-hand side.