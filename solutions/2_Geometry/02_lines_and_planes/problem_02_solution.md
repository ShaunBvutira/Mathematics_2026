### Exercise 2. A Line in Space

Given the vector parametric equation of line $L$:

$$
L: \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} + t \begin{pmatrix} 1 \\ 2 \\ -2 \end{pmatrix}, \quad t \in \mathbb{R}
$$

1. State a point on the line and its direction vector.
2. Check whether $P = (4, 3, -1)$ lies on $L$.
3. Find the point corresponding to $t = -1$.

---

### Solution

#### Step 1. State a point on the line and its direction vector

From the standard vector form $r(t) = P_0 + t v$:

- **Point on the line ($P_0$):** $(2, -1, 3)$ (obtained by setting parameter $t = 0$).
- **Direction vector ($v$):**

$$
v = \begin{pmatrix} 1 \\ 2 \\ -2 \end{pmatrix}
$$

---

#### Step 2. Check whether $P = (4, 3, -1)$ lies on $L$

For $P(4, 3, -1)$ to lie on $L$, there must exist a single, consistent value of the parameter $t$ that satisfies all three component equations simultaneously:

$$
\begin{cases}
4 = 2 + t, \\
3 = -1 + 2t, \\
-1 = 3 - 2t.
\end{cases}
$$

Solve for $t$ in each equation:

1. **$x$-component:** 
   $$
   4 = 2 + t \implies t = 2
   $$

2. **$y$-component:** 
   $$
   3 = -1 + 2t \implies 2t = 4 \implies t = 2
   $$

3. **$z$-component:** 
   $$
   -1 = 3 - 2t \implies -2t = -4 \implies t = 2
   $$

Since the parameter value $t = 2$ is consistent across all three coordinate equations, **the point $P = (4, 3, -1)$ lies on line $L$**.

---

#### Step 3. Find the point corresponding to $t = -1$

Substitute $t = -1$ directly into the parametric vector equation:

$$
\begin{aligned}
\begin{pmatrix} x \\ y \\ z \end{pmatrix} &= \begin{pmatrix} 2 \\ -1 \\ 3 \end{pmatrix} + (-1)\begin{pmatrix} 1 \\ 2 \\ -2 \end{pmatrix} \\
&= \begin{pmatrix} 2 - 1 \\ -1 - 2 \\ 3 + 2 \end{pmatrix} \\
&= \begin{pmatrix} 1 \\ -3 \\ 5 \end{pmatrix}
\end{aligned}
$$

The point corresponding to $t = -1$ is **$(1, -3, 5)$**.