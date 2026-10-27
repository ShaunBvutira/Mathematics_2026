### Exercise 5. A 3×3 Matrix

Use Gauss–Jordan elimination to find the inverse of

$$
A = 
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid I]$

Place matrix $A$ and the $3 \times 3$ identity matrix $I$ side by side:

$$
[A \mid I] = 
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}
$$

---

#### Step 2. Apply elementary row operations

**Step 2.1:** Eliminate the entry below the first pivot in Column 1 ($a_{31} = 1$).

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, 0 - 1, 1 - 0 \mid 0 - 1, 0 - 0, 1 - 0) = (0, -1, 1 \mid -1, 0, 1)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}
$$

---

**Step 2.2:** Eliminate the entry below the second pivot in Column 2 ($a_{32} = -1$).

Perform $R_3 \leftarrow R_3 + R_2$:

- Row 3 calculation: $(0 + 0, -1 + 1, 1 + 1 \mid -1 + 0, 0 + 1, 1 + 0) = (0, 0, 2 \mid -1, 1, 1)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}
$$

---

**Step 2.3:** Scale Row 3 to make the third pivot equal to $1$.

Perform $R_3 \leftarrow \frac{1}{2} R_3$:

- Row 3 calculation: $\left(0, 0, 1 \mid -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}\right)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

---

**Step 2.4:** Eliminate the entry above the third pivot in Column 3 ($a_{23} = 1$).

Perform $R_2 \leftarrow R_2 - R_3$:

- Row 2 calculation: $\left(0 - 0, 1 - 0, 1 - 1 \mid 0 - \left(-\frac{1}{2}\right), 1 - \frac{1}{2}, 0 - \frac{1}{2}\right) = \left(0, 1, 0 \mid \frac{1}{2}, \frac{1}{2}, -\frac{1}{2}\right)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

---

**Step 2.5:** Eliminate the entry above the second pivot in Column 2 ($a_{12} = 1$).

Perform $R_1 \leftarrow R_1 - R_2$:

- Row 1 calculation: $\left(1 - 0, 1 - 1, 0 - 0 \mid 1 - \frac{1}{2}, 0 - \frac{1}{2}, 0 - \left(-\frac{1}{2}\right)\right) = \left(1, 0, 0 \mid \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}\right)$

The augmented matrix is now in reduced row echelon form $[I \mid A^{-1}]$:

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 1 & 0 & \mid & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
0 & 0 & 1 & \mid & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

Thus, the inverse matrix is:

$$
A^{-1} = \frac{1}{2}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}
= 
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix}
$$

---

#### Step 3. Check the result by multiplication

Multiply $A$ by $A^{-1}$:

$$
\begin{aligned}
A A^{-1} &= 
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
1\left(\frac{1}{2}\right) + 1\left(\frac{1}{2}\right) + 0 & 1\left(-\frac{1}{2}\right) + 1\left(\frac{1}{2}\right) + 0 & 1\left(\frac{1}{2}\right) + 1\left(-\frac{1}{2}\right) + 0 \\
0 + 1\left(\frac{1}{2}\right) + 1\left(-\frac{1}{2}\right) & 0 + 1\left(\frac{1}{2}\right) + 1\left(\frac{1}{2}\right) & 0 + 1\left(-\frac{1}{2}\right) + 1\left(\frac{1}{2}\right) \\
1\left(\frac{1}{2}\right) + 0 + 1\left(-\frac{1}{2}\right) & 1\left(-\frac{1}{2}\right) + 0 + 1\left(\frac{1}{2}\right) & 1\left(\frac{1}{2}\right) + 0 + 1\left(\frac{1}{2}\right) \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
\frac{1}{2} + \frac{1}{2} & -\frac{1}{2} + \frac{1}{2} & \frac{1}{2} - \frac{1}{2} \\
\frac{1}{2} - \frac{1}{2} & \frac{1}{2} + \frac{1}{2} & -\frac{1}{2} + \frac{1}{2} \\
\frac{1}{2} - \frac{1}{2} & -\frac{1}{2} + \frac{1}{2} & \frac{1}{2} + \frac{1}{2} \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}
\end{aligned}
$$

Since $A A^{-1} = I$, the calculated inverse $A^{-1}$ is correct.s