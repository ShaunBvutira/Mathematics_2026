### Exercise 8. Inverse of a Transformation

The matrix

$$
S = 
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S, S^{-1}$ on one simple vector.

---

### Solution

#### Step 1. Compute $S^{-1}$

For the diagonal matrix $S = \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix}$, compute its determinant:

$$
\begin{aligned}
\det S &= (2)\left(\frac{1}{2}\right) - (0)(0) \\
       &= 1
\end{aligned}
$$

Using the inverse formula for a $2 \times 2$ matrix:

$$
\begin{aligned}
S^{-1} &= \frac{1}{1}
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix} \\
       &= 
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Explain geometrically what the inverse transformation does

- **Action of $S$:** Matrix $S$ scales the plane by stretching vectors along the $x$-axis by a factor of $2$ and compressing vectors along the $y$-axis by a factor of $\frac{1}{2}$.

- **Action of $S^{-1}$:** The inverse transformation undoes the geometric changes made by $S$. Specifically, $S^{-1}$ compresses vectors along the $x$-axis by a factor of $\frac{1}{2}$ and stretches vectors along the $y$-axis by a factor of $2$.

---

#### Step 3. Check the action of the pair $S, S^{-1}$ on a simple vector

Choose the simple vector:

$$
v = 
\begin{pmatrix}
4 \\
6 \\
\end{pmatrix}
$$

**Step 3.1:** Apply transformation $S$ to vector $v$:

$$
\begin{aligned}
v' = S v &= 
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
\begin{pmatrix}
4 \\
6 \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
(2)(4) + (0)(6) \\
(0)(4) + \left(\frac{1}{2}\right)(6) \\
\end{pmatrix} \\
         &= 
\begin{pmatrix}
8 \\
3 \\
\end{pmatrix}
\end{aligned}
$$

**Step 3.2:** Apply the inverse transformation $S^{-1}$ to $v'$:

$$
\begin{aligned}
S^{-1} v' &= 
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
8 \\
3 \\
\end{pmatrix} \\
          &= 
\begin{pmatrix}
\left(\frac{1}{2}\right)(8) + (0)(3) \\
(0)(8) + (2)(3) \\
\end{pmatrix} \\
          &= 
\begin{pmatrix}
4 \\
6 \\
\end{pmatrix} \\
          &= v
\end{aligned}
$$

Applying $S$ followed by $S^{-1}$ returns the vector to its original state $v$, confirming that $S^{-1} (S v) = I v = v$.