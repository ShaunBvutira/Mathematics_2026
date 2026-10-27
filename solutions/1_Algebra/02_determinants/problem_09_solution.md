### Exercise 9. Area and the Determinant

The vectors

$$
u = 
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix}, \quad 
v = 
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

---

### Solution

#### Step 1. Compute the area using the determinant of matrix (u v)

Form the matrix $M = \begin{pmatrix} u & v \end{pmatrix}$ by placing $u$ in the first column and $v$ in the second column:

$$
M = 
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}
$$

The determinant of $M$ is:

$$
\begin{aligned}
\det M &= (3)(4) - (1)(1) \\
       &= 12 - 1 \\
       &= 11
\end{aligned}
$$

**Area Calculation:** The geometric area of the parallelogram spanned by $u$ and $v$ is equal to the absolute value of the determinant of $M$:

$$
\text{Area} = |\det M| = |11| = 11
$$

---

#### Step 2. Reverse the order of the vectors and compute the new determinant

Form matrix $N = \begin{pmatrix} v & u \end{pmatrix}$ by placing $v$ in the first column and $u$ in the second column:

$$
N = 
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix}
$$

The determinant of $N$ is:

$$
\begin{aligned}
\det N &= (1)(1) - (3)(4) \\
       &= 1 - 12 \\
       &= -11
\end{aligned}
$$

---

#### Step 3. Explain what changes and what remains unchanged

- **What changes in the determinant:** 
  Reversing the order of the vectors corresponds to swapping the two columns of the matrix. Swapping any two columns (or rows) of a matrix multiplies its determinant by $-1$. Therefore, the determinant changes sign from $11$ to $-11$. The sign of the determinant represents the **orientation** of the vectors (clockwise vs. counter-clockwise).

- **What does not change in the area:** 
  The area of the geometric shape (parallelogram) depends only on its physical dimensions (base and height), which are independent of orientation. Because area is calculated using the absolute value of the determinant, it remains unchanged:

$$
\text{Area} = |\det N| = |-11| = 11
$$