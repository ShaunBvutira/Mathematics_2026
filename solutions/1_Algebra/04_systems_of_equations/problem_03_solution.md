### Exercise 3. Inconsistent Systems

Solve or show that the system is inconsistent:

$$
\begin{cases}
x + 2y = 3, \\
2x + 4y = 7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the linear system in augmented matrix form:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}
$$

---

#### Step 2. Perform elimination

Eliminate the variable $x$ from the second row using $R_1$.

Perform $R_2 \leftarrow R_2 - 2 R_1$:

- Row 2 calculation: $(2 - 2(1), 4 - 2(2) \mid 7 - 2(3)) = (0, 0 \mid 1)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

---

#### Step 3. Interpret the contradiction

Convert the second row of the reduced matrix back into an algebraic equation:

$$
0x + 0y = 1 \implies 0 = 1
$$

This is a **false statement (contradiction)** because $0$ can never equal $1$, regardless of the values chosen for $x$ and $y$.

---

#### Step 4. Geometric interpretation and conclusion

- **Algebraic Conclusion:** Because elimination leads directly to a row of the form $[0 \ 0 \ \dots \ 0 \mid c]$ with $c \neq 0$, the system has **no solution** (it is **inconsistent**).

- **Geometric Interpretation:** The two equations represent parallel lines in $\mathbb{R}^2$:
  - Line 1: $y = -\frac{1}{2}x + \frac{3}{2}$
  - Line 2: $y = -\frac{1}{2}x + \frac{7}{4}$

  Both lines have the exact same slope ($m = -\frac{1}{2}$) but different $y$-intercepts ($\frac{3}{2} \neq \frac{7}{4}$). Since parallel lines never intersect, there is no point $(x, y)$ that satisfies both equations simultaneously.