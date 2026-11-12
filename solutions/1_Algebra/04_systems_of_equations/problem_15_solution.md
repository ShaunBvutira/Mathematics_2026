### Exercise 15. Classifying Three Systems

#### Question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**
$$
\begin{cases}
x + y = 2, \\
x - y = 0,
\end{cases}
$$

**System 2**
$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4,
\end{cases}
$$

**System 3**
$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

---

### Solution

#### System 1

$$
\begin{cases}
x + y = 2, \\
x - y = 0
\end{cases}
$$

- **Minimal Elimination:**
  Write the augmented matrix and eliminate $x$ from the second row using $R_2 \leftarrow R_2 - R_1$:

  $$
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  1 & -1 & 0
  \end{array}\right)
  \xrightarrow{R_2 \leftarrow R_2 - R_1}
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  0 & -2 & -2
  \end{array}\right)
  $$

- **Classification:** **One solution** (consistent and independent).
- **Justification:**
  - The echelon form has a non-zero pivot in every variable column ($1$ in column $1$ and $-2 \neq 0$ in column $2$), with no contradictory row.
  - Because both variables $x$ and $y$ are pivot (basic) variables and there are zero free variables, the system determines a unique solution: $y = 1$ and $x = 1$. Geometrically, the two lines have different slopes ($-1$ and $1$) and intersect at a single point $(1, 1)$.

---

#### System 2

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4
\end{cases}
$$

- **Minimal Elimination:**
  Write the augmented matrix and eliminate $x$ from the second row using $R_2 \leftarrow R_2 - 2R_1$:

  $$
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  2 & 2 & 4
  \end{array}\right)
  \xrightarrow{R_2 \leftarrow R_2 - 2R_1}
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  0 & 0 & 0
  \end{array}\right)
  $$

- **Classification:** **Infinitely many solutions** (consistent and dependent).
- **Justification:**
  - The second row reduces to $0x + 0y = 0$, which is always satisfied and imposes no restriction on the variables.
  - Only one pivot remains (in the $x$-column), leaving $y$ as a **free variable** ($y = t \in \mathbb{R}$, giving $x = 2 - t$). Geometrically, the second equation is simply twice the first, so both equations represent the exact same line.

---

#### System 3

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5
\end{cases}
$$

- **Minimal Elimination:**
  Write the augmented matrix and eliminate $x$ from the second row using $R_2 \leftarrow R_2 - 2R_1$:

  $$
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  2 & 2 & 5
  \end{array}\right)
  \xrightarrow{R_2 \leftarrow R_2 - 2R_1}
  \left(\begin{array}{cc|c}
  1 & 1 & 2 \\
  0 & 0 & 1
  \end{array}\right)
  $$

- **Classification:** **No solution** (inconsistent).
- **Justification:**
  - The second row translates to the equation $0x + 0y = 1$, or $0 = 1$, which is a contradiction for all real numbers $x$ and $y$.
  - Because a pivot appears in the augmented right-hand side column, the system is inconsistent. Geometrically, the two equations define parallel lines ($x + y = 2$ and $x + y = \frac{5}{2}$) that never intersect.