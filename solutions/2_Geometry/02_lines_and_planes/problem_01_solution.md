### Exercise 1. Line Through Two Points

Find the equation of the line through $A = (1, 2)$ and $B = (4, -1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

---

### Solution

#### Step 1. Identify a direction vector

A direction vector $v$ for the line passing through points $A$ and $B$ is found by taking the displacement vector from $A$ to $B$:

$$
v = \vec{AB} = B - A = 
\begin{pmatrix} 4 - 1 \\ -1 - 2 \end{pmatrix} = 
\begin{pmatrix} 3 \\ -3 \end{pmatrix}
$$

*(Note: Any non-zero scalar multiple of $v$, such as $\begin{pmatrix} 1 \\ -1 \end{pmatrix}$, is also a valid direction vector.)*

---

#### Step 2. Construct the parametric form

Using point $A(1, 2)$ as the initial position vector and $v = \begin{pmatrix} 3 \\ -3 \end{pmatrix}$ as the direction vector, the parametric equations are:

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 \\ 2 \end{pmatrix} + t \begin{pmatrix} 3 \\ -3 \end{pmatrix}, \quad t \in \mathbb{R}
$$

Written separately as component equations:

$$
\begin{cases}
x = 1 + 3t, \\
y = 2 - 3t,
\end{cases}
\quad t \in \mathbb{R}
$$

---

#### Step 3. Construct the general form and identify a normal vector

To convert to general (implicit) form $Ax + By + C = 0$, eliminate the parameter $t$:

1. From the first parametric equation, isolate $t$:
   $$
   3t = x - 1 \implies t = \frac{x - 1}{3}
   $$
2. Substitute $t$ into the second parametric equation:
   $$
   y = 2 - 3\left(\frac{x - 1}{3}\right) = 2 - (x - 1) = 2 - x + 1 = 3 - x
   $$
3. Rearrange all terms to one side:
   $$
   x + y - 3 = 0
   $$

From the general equation $Ax + By + C = 0$, the normal vector $n = \begin{pmatrix} A \\ B \end{pmatrix}$ is formed by the coefficients of $x$ and $y$:

$$
n = \begin{pmatrix} 1 \\ 1 \end{pmatrix}
$$

*(Check orthogonality between direction vector $v$ and normal vector $n$: $v \cdot n = (3)(1) + (-3)(1) = 3 - 3 = 0 \quad \checkmark$)*

---

#### Step 4. Verify that both points satisfy the general equation

Substitute the coordinates of points $A$ and $B$ into the general equation $x + y - 3 = 0$:

1. **Check Point $A(1, 2)$:**
   $$
   1 + 2 - 3 = 3 - 3 = 0 \quad \checkmark
   $$

2. **Check Point $B(4, -1)$:**
   $$
   4 + (-1) - 3 = 4 - 4 = 0 \quad \checkmark
   $$

Both points satisfy the general equation, confirming the line equation is correct.