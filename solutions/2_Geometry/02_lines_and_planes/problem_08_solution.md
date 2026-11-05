### Exercise 8. Intersection Point of a Line and a Plane

Find the intersection point of the line

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \\ 2 \end{pmatrix} + t \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix}, \quad t \in \mathbb{R}
$$

with the plane $x + y + z = 4$. Check the result by substituting it into both descriptions.

---

### Solution

#### Step 1. Write the parametric equations of the line

From the vector form of the line, express $x$, $y$, and $z$ in terms of parameter $t$:

$$
\begin{cases}
x = 1 + t, \\
y = 2t, \\
z = 2 - t.
\end{cases}
$$

---

#### Step 2. Substitute the parametric equations into the plane equation

Substitute $x = 1 + t$, $y = 2t$, and $z = 2 - t$ into the plane equation $x + y + z = 4$:

$$
(1 + t) + (2t) + (2 - t) = 4
$$

Combine like terms:

$$
\begin{aligned}
(1 + 2) + (t + 2t - t) &= 4 \\
3 + 2t &= 4 \\
2t &= 1 \\
t &= \frac{1}{2}
\end{aligned}
$$

---

#### Step 3. Compute the coordinates of the intersection point

Substitute parameter $t = \frac{1}{2}$ back into the parametric equations of the line:

$$
\begin{cases}
x = 1 + \frac{1}{2} = \frac{3}{2}, \\[1ex]
y = 2\left(\frac{1}{2}\right) = 1, \\[1ex]
z = 2 - \frac{1}{2} = \frac{3}{2}.
\end{cases}
$$

The intersection point is **$P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$** (or $(1.5, 1, 1.5)$).

---

#### Step 4. Check the result in both descriptions

1. **Check against the line equation:**
   Substitute $t = \frac{1}{2}$ into the line equation:
   $$
   \begin{pmatrix} 1 \\ 0 \\ 2 \end{pmatrix} + \frac{1}{2} \begin{pmatrix} 1 \\ 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 1 + \frac{1}{2} \\ 0 + 1 \\ 2 - \frac{1}{2} \end{pmatrix} = \begin{pmatrix} \frac{3}{2} \\ 1 \\ \frac{3}{2} \end{pmatrix} \quad \checkmark
   $$

2. **Check against the plane equation:**
   Substitute $x = \frac{3}{2}$, $y = 1$, and $z = \frac{3}{2}$ into $x + y + z = 4$:
   $$
   \text{LHS} = \frac{3}{2} + 1 + \frac{3}{2} = \frac{6}{2} + 1 = 3 + 1 = 4 = \text{RHS} \quad \checkmark
   $$

Both descriptions are satisfied, verifying that $\left(\frac{3}{2}, 1, \frac{3}{2}\right)$ is the correct intersection point.