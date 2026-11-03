### Exercise 11. A Parameter in a System of Three Equations

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x + y + z = 1, \\
x + ty + z = 2, \\
x + y + tz = 3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the system as an augmented matrix:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}
$$

---

#### Step 2. Perform elimination

**Step 2.1:** Eliminate $x$ from the second and third rows using Row 1.

Perform $R_2 \leftarrow R_2 - R_1$:

- Row 2 calculation: $(1 - 1, t - 1, 1 - 1 \mid 2 - 1) = (0, t - 1, 0 \mid 1)$

Perform $R_3 \leftarrow R_3 - R_1$:

- Row 3 calculation: $(1 - 1, 1 - 1, t - 1 \mid 3 - 1) = (0, 0, t - 1 \mid 2)$

The augmented matrix is now in row echelon form:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t - 1 & 0 & \mid & 1 \\
0 & 0 & t - 1 & \mid & 2 \\
\end{pmatrix}
$$

---

#### Step 3. Parameter Case Analysis

The standard calculation step of dividing by $(t - 1)$ to isolate variables ceases to be valid when $t - 1 = 0$, i.e., when $t = 1$. Therefore, we analyze $t = 1$ separately from $t \neq 1$.

##### Case 1: $t = 1$ (Critical parameter value)

Substitute $t = 1$ into the row-echelon augmented matrix:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}
$$

Looking at Row 2 (or Row 3):

$$
0x + 0y + 0z = 1 \implies 0 = 1
$$

This is a contradiction.

- **Result for $t = 1$:** The system is **inconsistent** and has **no solution**.

---

##### Case 2: $t \neq 1$ (Standard case)

When $t \neq 1$, $t - 1 \neq 0$, so dividing by $(t - 1)$ is a valid arithmetic operation. 

Solve for the variables using back-substitution:

1. **From Row 3:**
   $$
   (t - 1)z = 2 \implies z = \frac{2}{t - 1}
   $$

2. **From Row 2:**
   $$
   (t - 1)y = 1 \implies y = \frac{1}{t - 1}
   $$

3. **From Row 1:**
   $$
   x + y + z = 1 \implies x = 1 - y - z
   $$
   Substitute $y$ and $z$:
   $$
   \begin{aligned}
   x &= 1 - \frac{1}{t - 1} - \frac{2}{t - 1} \\
     &= 1 - \frac{3}{t - 1} \\
     &= \frac{(t - 1) - 3}{t - 1} \\
     &= \frac{t - 4}{t - 1}
   \end{aligned}
   $$

- **Result for $t \neq 1$:** The system has **exactly one solution** (a unique solution).

---

#### Step 4. Summary of Results

- **For $t = 1$:** **No solution** (inconsistent system due to $0 = 1$).
- **For $t \neq 1$:** **Unique solution**, given by:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=
\begin{pmatrix}
\frac{t - 4}{t - 1} \\[1ex]
\frac{1}{t - 1} \\[1ex]
\frac{2}{t - 1} \\
\end{pmatrix}
$$

*(Note: Infinitely many solutions cannot occur for any value of $t$.)*