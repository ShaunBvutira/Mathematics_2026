### Exercise 6. A System with a Parameter — Which Cases Actually Occur?

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

Among the three possibilities — **exactly one solution**, **infinitely many solutions**, **no solution** — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

---

### Solution

#### Step 1. Form the augmented matrix $[A \mid b]$

Write the linear system in augmented matrix form:

$$
[A \mid b] = 
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

---

#### Step 2. Perform elimination

Eliminate $x$ from the second row by subtracting $a$ times Row 1 from Row 2 ($R_2 \leftarrow R_2 - a R_1$):

- Row 2 calculation: $(a - a(1), a - a(1) \mid 4 - a(2)) = (0, 0 \mid 4 - 2a)$

The augmented matrix becomes:

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4 - 2a \\
\end{pmatrix}
$$

---

#### Step 3. Case Analysis

Analyze the simplified second-row equation:

$$
0x + 0y = 4 - 2a
$$

##### Case 1: $4 - 2a \neq 0 \implies a \neq 2$
When $a \neq 2$, the right-hand side $4 - 2a$ is non-zero, yielding a contradiction:

$$
0 = 4 - 2a \quad (\text{where } 4 - 2a \neq 0)
$$

- **Result:** The system has **no solution** (it is **inconsistent**).

##### Case 2: $4 - 2a = 0 \implies a = 2$
When $a = 2$, substitute $a = 2$ back into the original system:

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4.
\end{cases}
$$

Dividing the second equation by $2$ shows it is identical to the first equation ($x + y = 2$). The second row of the augmented matrix becomes $[0 \ 0 \mid 0]$, leaving $x$ as a basic variable and $y = t$ as a free variable:

$$
\begin{cases}
x = 2 - t, \\
y = t,
\end{cases}
\quad t \in \mathbb{R}
$$

- **Result:** The system has **infinitely many solutions**.

---

#### Step 4. Summary and Explanation of Missing Case

- **No solution:** Occurs for all $a \neq 2$.
- **Infinitely many solutions:** Occurs when $a = 2$.
- **Exactly one solution:** **Cannot occur for any value of $a$**.

**Why "exactly one solution" can never occur:**

For a $2 \times 2$ system to have a unique solution, the determinant of the coefficient matrix $A$ must be non-zero ($\det A \neq 0$). 

Calculating the determinant of $A$:

$$
\det A = 
\begin{vmatrix}
1 & 1 \\
a & a \\
\end{vmatrix}
= (1)(a) - (1)(a) = a - a = 0
$$

Since $\det A = 0$ for **every** real number $a$, the coefficient rows $(1, 1)$ and $(a, a)$ are linearly dependent (the second row is always $a$ times the first). Thus, the rank of $A$ is at most $1$, meaning the system can never have $2$ pivots. Without $2$ pivots, a unique solution is geometrically impossible—the two equations represent either parallel lines (when $a \neq 2$) or the exact same line (when $a = 2$).