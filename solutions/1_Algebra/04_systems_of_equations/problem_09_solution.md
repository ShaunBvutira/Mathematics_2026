### Exercise 9. Composing Transformations

Let

$$
S = 
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}, \quad 
R = 
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$
x = 
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

---

### Solution

#### Step 1. Compute $RSx$ (Scale first, then Rotate)

First, compute the image of $x$ under scaling matrix $S$:

$$
\begin{aligned}
Sx &= 
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(2)(1) + (0)(2) \\
(0)(1) + (1)(2) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

Next, apply the rotation matrix $R$ to vector $Sx$:

$$
\begin{aligned}
RSx &= 
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
(0)(2) + (-1)(2) \\
(1)(2) + (0)(2) \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute $SRx$ (Rotate first, then Scale)

First, compute the image of $x$ under rotation matrix $R$:

$$
\begin{aligned}
Rx &= 
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(0)(1) + (-1)(2) \\
(1)(1) + (0)(2) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

Next, apply the scaling matrix $S$ to vector $Rx$:

$$
\begin{aligned}
SRx &= 
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
(2)(-2) + (0)(1) \\
(0)(-2) + (1)(1) \\
\end{pmatrix} \\
    &= 
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Compare the results

Comparing the final output vectors:

$$
RSx = 
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\neq
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
= SRx
$$

The two transformation sequences produce completely different output vectors.

---

#### Step 4. Geometric explanation of why order matters

1. **For $RSx$ (Scale, then Rotate):**
   - **Step 1 ($S$):** The vector $(1, 2)^T$ is stretched horizontally along the $x$-axis by a factor of $2$, becoming $(2, 2)^T$.
   - **Step 2 ($R$):** Rotating $(2, 2)^T$ by $90^\circ$ counterclockwise maps the positive $x$-axis component to the positive $y$-axis, and the positive $y$-axis component to the negative $x$-axis, yielding $(-2, 2)^T$. The stretched dimension ends up along the **$y$-axis**.

2. **For $SRx$ (Rotate, then Scale):**
   - **Step 1 ($R$):** Rotating $(1, 2)^T$ by $90^\circ$ counterclockwise moves it first to $(-2, 1)^T$. The original $x$-component ($1$) is now on the $y$-axis, and the original $y$-component ($2$) is now on the negative $x$-axis.
   - **Step 2 ($S$):** Matrix $S$ *always* stretches along the global $x$-axis. Applying $S$ stretches the newly rotated negative $x$-component ($-2$) to $-4$, yielding $(-4, 1)^T$. The stretched dimension stays on the **$x$-axis**.

Because non-uniform scaling expands space along fixed coordinate axes, rotating space *before* scaling changes which original components get stretched. Thus, spatial transformations generally do not commute.