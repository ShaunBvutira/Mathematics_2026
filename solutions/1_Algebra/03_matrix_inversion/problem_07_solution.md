### Exercise 7. Inverse of a Product

For

$$
A = 
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}, \quad 
B = 
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

---

### Solution

#### Step 1. Compute $(AB)^{-1}$

First, calculate the product $AB$:

$$
\begin{aligned}
AB &= 
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
(1)(2) + (1)(0) & (1)(0) + (1)(3) \\
(0)(2) + (1)(0) & (0)(0) + (1)(3) \\
\end{pmatrix} \\
   &= 
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\end{aligned}
$$

Next, find the inverse $(AB)^{-1}$ using the $2 \times 2$ inverse formula. The determinant of $AB$ is:

$$
\det(AB) = (2)(3) - (3)(0) = 6
$$

Applying the inverse formula:

$$
\begin{aligned}
(AB)^{-1} &= \frac{1}{6}
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} \\
          &= 
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 2. Compute $B^{-1}A^{-1}$

First, find the individual inverses $A^{-1}$ and $B^{-1}$.

For $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$:

$$
\det A = (1)(1) - (1)(0) = 1
$$

$$
A^{-1} = \frac{1}{1}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
= 
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
$$

For $B = \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}$:

$$
\det B = (2)(3) - (0)(0) = 6
$$

$$
B^{-1} = \frac{1}{6}
\begin{pmatrix}
3 & 0 \\
0 & 2 \\
\end{pmatrix}
= 
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

Now, multiply $B^{-1}$ by $A^{-1}$:

$$
\begin{aligned}
B^{-1} A^{-1} &= 
\begin{pmatrix}
\frac{1}{2} & 0 \\
0 & \frac{1}{3} \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} \\
              &= 
\begin{pmatrix}
\left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\
(0)(1) + \left(\frac{1}{3}\right)(0) & (0)(-1) + \left(\frac{1}{3}\right)(1) \\
\end{pmatrix} \\
              &= 
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
\end{aligned}
$$

---

#### Step 3. Compare the results

Both calculations yield the identical result:

$$
(AB)^{-1} = B^{-1}A^{-1} = 
\begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} \\
0 & \frac{1}{3} \\
\end{pmatrix}
$$

---

#### Step 4. Explain the meaning of the reversed order

The formula $(AB)^{-1} = B^{-1}A^{-1}$ is known as the **shoes and socks property**.

1. **Forward Operation ($AB$):** When applying the transformation $AB$ to a vector $x$, matrix $B$ acts first, followed by matrix $A$:
   $$
   (AB)x = A(Bx)
   $$

2. **Reversing the Operation:** To undo the combined action of putting on socks ($B$) and then putting on shoes ($A$), you must take off your shoes first ($A^{-1}$) and then take off your socks ($B^{-1}$).

Algebraically, multiplying $(AB)$ by $(B^{-1}A^{-1})$ demonstrates how the inner terms cancel out first:

$$
(AB)(B^{-1}A^{-1}) = A (B B^{-1}) A^{-1} = A I A^{-1} = A A^{-1} = I
$$

Because matrix multiplication is not generally commutative, reversing the order is required to ensure that each operation is undone in the correct sequential order.