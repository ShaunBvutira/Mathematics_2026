### Exercise 8. Determinant of a Product

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq BA$.

---

### Solution

#### Step 1. Compute $\det(AB)$

**Property:** For any two square matrices $A$ and $B$ of the same size, the determinant of their product is the product of their individual determinants:

$$
\det(AB) = \det A \cdot \det B
$$

Using the given values $\det A = 3$ and $\det B = -5$:

$$
\begin{aligned}
\det(AB) &= (3)(-5) \\
         &= -15
\end{aligned}
$$

---

#### Step 2. Compute $\det(BA)$

Applying the multiplicativity property of determinants to the product $BA$:

$$
\det(BA) = \det B \cdot \det A
$$

Using the given values:

$$
\begin{aligned}
\det(BA) &= (-5)(3) \\
         &= -15
\end{aligned}
$$

---

#### Step 3. Compute $\det(A^{-1}B)$

First, verify that $A^{-1}$ exists. A matrix $A$ is invertible if and only if $\det A \neq 0$. Since $\det A = 3 \neq 0$, $A^{-1}$ exists, and its determinant is given by:

$$
\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}
$$

Now, using the product property for determinants:

$$
\begin{aligned}
\det(A^{-1}B) &= \det(A^{-1}) \cdot \det B \\
              &= \left(\frac{1}{3}\right)(-5) \\
              &= -\frac{5}{3}
\end{aligned}
$$

---

#### Step 4. Explain why $\det(AB) = \det(BA)$

While matrix multiplication is generally non-commutative ($AB \neq BA$), real (and complex) number multiplication **is** commutative. 

By the product property of determinants, we have:

$$
\det(AB) = \det A \cdot \det B
$$

and 

$$
\det(BA) = \det B \cdot \det A
$$

Because $\det A$ and $\det B$ are real numbers (scalars), $\det A \cdot \det B = \det B \cdot \det A$. Therefore:

$$
\det(AB) = \det(BA)
$$

The scalar nature of determinant values allows them to commute even when the matrices themselves do not.