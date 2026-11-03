### Exercise 5. Row Echelon Form and Number of Solutions

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

---

### Solution

#### Step 1. Identify pivot columns and basic versus free variables

Let the variable columns correspond to $x, y, z$.

- **Row 1:** First non-zero entry is $1$ in column 1.
- **Row 2:** First non-zero entry is $1$ in column 2.
- **Row 3:** Entirely zero row ($0 = 0$), which indicates no contradiction.

The pivot columns are column 1 (for $x$) and column 2 (for $y$). Column 3 (for $z$) contains no pivot.

- **Basic (Pivot) variables:** $x, y$
- **Free variables:** $z$

---

#### Step 2. Determine the number of free variables and overall solutions

- **Number of free variables:** 

  $$
  \text{Free variables} = (\text{Total variables}) - (\text{Number of pivots}) = 3 - 2 = 1
  $$

  Since there is $1$ free variable ($z$) and no contradictory row (such as $[0 \ 0 \ 0 \mid c]$ with $c \neq 0$), the parameter $z$ can take any real value in $\mathbb{R}$.

- **Number of solutions:** Because the free variable can take infinitely many real values, the system has **infinitely many solutions**.

---

#### Step 3. Express the solution in parametric form

Convert the non-zero rows back to algebraic equations:

1. **Second row:**
   $$
   y + 2z = 1 \implies y = 1 - 2z
   $$

2. **First row:**
   $$
   x + 2y - z = 3
   $$

Substitute $y = 1 - 2z$ into the first equation to express $x$ strictly in terms of $z$:

$$
\begin{aligned}
x + 2(1 - 2z) - z &= 3 \\
x + 2 - 4z - z &= 3 \\
x + 2 - 5z &= 3 \\
x &= 1 + 5z
\end{aligned}
$$

Set $z = t$, where $t \in \mathbb{R}$ is a free parameter:

$$
\begin{cases}
x = 1 + 5t, \\
y = 1 - 2t, \\
z = t,
\end{cases}
\quad t \in \mathbb{R}
$$

Or in vector form:

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix}
=
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}
+ t
\begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix},
\quad t \in \mathbb{R}
$$

---

#### Step 4. Explain how to know how many variables can be chosen freely

The number of variables that may be chosen freely is determined by the **number of non-pivot columns** in the matrix when it is in Row Echelon Form.

1. Each pivot element anchors a specific basic variable that is uniquely determined once all free variables are chosen.
2. Every column without a pivot corresponds to a degree of freedom. Each such variable can be assigned an arbitrary parameter value independently of the others.
3. Here, out of $3$ variables, $2$ columns have pivots and $1$ column lacks a pivot. Thus, exactly $1$ variable ($z$) may be chosen freely.