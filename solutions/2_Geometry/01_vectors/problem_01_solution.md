### Exercise 1. Vector Operations and Their Meaning

For $u = (2, -1, 3)^T$ and $v = (-1, 4, 2)^T$, compute

$$
u + v, \quad u - v, \quad 3u - 2v.
$$

Then verify that $(u + v) - v = u$, and explain geometrically what adding two vectors means.

---

### Solution

#### Step 1. Compute $u + v$, $u - v$, and $3u - 2v$

Given:

$$
u = 
\begin{pmatrix}
2 \\
-1 \\
3 \\
\end{pmatrix}, \quad 
v = 
\begin{pmatrix}
-1 \\
4 \\
2 \\
\end{pmatrix}
$$

- **Compute $u + v$:**

$$
u + v = 
\begin{pmatrix}
2 + (-1) \\
-1 + 4 \\
3 + 2 \\
\end{pmatrix}
=
\begin{pmatrix}
1 \\
3 \\
5 \\
\end{pmatrix}
$$

- **Compute $u - v$:**

$$
u - v = 
\begin{pmatrix}
2 - (-1) \\
-1 - 4 \\
3 - 2 \\
\end{pmatrix}
=
\begin{pmatrix}
3 \\
-5 \\
1 \\
\end{pmatrix}
$$

- **Compute $3u - 2v$:**

$$
\begin{aligned}
3u - 2v &= 
3\begin{pmatrix}
2 \\
-1 \\
3 \\
\end{pmatrix}
-
2\begin{pmatrix}
-1 \\
4 \\
2 \\
\end{pmatrix} \\
&= 
\begin{pmatrix}
6 \\
-3 \\
9 \\
\end{pmatrix}
-
\begin{pmatrix}
-2 \\
8 \\
4 \\
\end{pmatrix} \\
&= 
\begin{pmatrix}
6 - (-2) \\
-3 - 8 \\
9 - 4 \\
\end{pmatrix}
=
\begin{pmatrix}
8 \\
-11 \\
5 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Verify $(u + v) - v = u$

Using the result $u + v = (1, 3, 5)^T$ from Step 1:

$$
(u + v) - v = 
\begin{pmatrix}
1 \\
3 \\
5 \\
\end{pmatrix}
-
\begin{pmatrix}
-1 \\
4 \\
2 \\
\end{pmatrix}
=
\begin{pmatrix}
1 - (-1) \\
3 - 4 \\
5 - 2 \\
\end{pmatrix}
=
\begin{pmatrix}
2 \\
-1 \\
3 \\
\end{pmatrix}
= u
$$

The identity holds true algebraically.

---

#### Step 3. Geometric meaning of vector addition

Geometrically, adding two vectors $u$ and $v$ corresponds to **combining sequential displacements in space**:

1. **The Tip-to-Tail Rule:** Place the tail (start) of vector $v$ at the tip (head) of vector $u$. The sum vector $u + v$ is the direct arrow drawn from the original starting point (tail of $u$) to the final terminal point (tip of $v$).
2. **The Parallelogram Law:** If both vectors $u$ and $v$ are placed with their tails at the origin $(0, 0, 0)$, $u + v$ forms the main diagonal of the parallelogram defined by $u$ and $v$.

Subtractions like $(u + v) - v = u$ geometrically represent starting at the tip of $u + v$ and traversing vector $v$ in reverse (backwards along $-v$), which returns precisely to the terminal position of vector $u$.