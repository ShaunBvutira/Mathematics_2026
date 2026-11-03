### Exercise 14. A Small Change in the Right-Hand Side

Compare the systems:

$$
\text{System A: }
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.
\end{cases}
\quad
\text{System B: }
\begin{cases}
x + y = 2, \\
2x - y = 1, \\
3x = 3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

---

### Solution

#### Step 1. Analyze System A

- **Form the augmented matrix $[A \mid b_A]$:**

$$
[A \mid b_A] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3 \\
\end{pmatrix}
$$

- **Perform Gaussian elimination:**

1. $R_2 \leftarrow R_2 - 2R_1$:
   Row 2 becomes: $(2 - 2(1), -1 - 2(1) \mid 1 - 2(2)) = (0, -3 \mid -3)$

2. $R_3 \leftarrow R_3 - 3R_1$:
   Row 3 becomes: $(3 - 3(1), 0 - 3(1) \mid 3 - 3(2)) = (0, -3 \mid -3)$

The matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & -3 & \mid & -3 \\
\end{pmatrix}
$$

3. $R_3 \leftarrow R_3 - R_2$:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

- **Solve via back-substitution:**
  - Row 2: $-3y = -3 \implies y = 1$
  - Row 1: $x + 1 = 2 \implies x = 1$

- **Consistency:** System A is **consistent** and has a **unique solution**:

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix}
=
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}
$$

---

#### Step 2. Analyze System B

- **Form the augmented matrix $[A \mid b_B]$:**

$$
[A \mid b_B] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & 3.1 \\
\end{pmatrix}
$$

- **Perform Gaussian elimination:**

1. $R_2 \leftarrow R_2 - 2R_1$:
   Row 2 becomes: $(0, -3 \mid -3)$

2. $R_3 \leftarrow R_3 - 3R_1$:
   Row 3 becomes: $(3 - 3(1), 0 - 3(1) \mid 3.1 - 3(2)) = (0, -3 \mid -2.9)$

The matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & -3 & \mid & -2.9 \\
\end{pmatrix}
$$

3. $R_3 \leftarrow R_3 - R_2$:
   Row 3 calculation: $(0 - 0, -3 - (-3) \mid -2.9 - (-3)) = (0, 0 \mid 0.1)$

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & 0.1 \\
\end{pmatrix}
$$

- **Interpret Row 3:**
  Row 3 represents the equation $0x + 0y = 0.1$, which implies $0 = 0.1$. This is a contradiction.

- **Consistency:** System B is **inconsistent** and has **no solution**.

---

#### Step 3. Explain why a small change alters the system type

1. **Overdetermined Geometry:**
   Both systems are **overdetermined**, meaning there are more equations ($3$) than unknowns ($2$). In 2D space ($\mathbb{R}^2$), each linear equation represents a straight line. 

2. **Intersection of Three Lines:**
   - For an overdetermined system of 3 lines in a 2D plane to have a solution, all 3 lines must intersect at the **exact same single point** (they must be concurrent).
   - In **System A**, the first two lines $x + y = 2$ and $2x - y = 1$ intersect at $(1, 1)$. The third line $3x = 3$ (or $x = 1$) happens to pass directly through that exact same point $(1, 1)$.
   - In **System B**, changing $3$ to $3.1$ shifts the third line slightly to $x = 1.0333...$. While the first two lines still intersect at $(1, 1)$, the third line no longer passes through that point.

3. **Loss of Compatibility:**
   In an overdetermined system, any slight perturbation to the right-hand side of a redundant equation breaks the precise geometric alignment required for all equations to be satisfied simultaneously. As a result, the system transitions immediately from having a unique solution to having no solution.