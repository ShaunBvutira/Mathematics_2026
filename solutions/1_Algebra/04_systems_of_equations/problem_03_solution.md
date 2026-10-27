### Exercise 3. When Can Matrices Be Multiplied?

The matrix sizes are

$$
A_{2 \times 3}, \quad B_{3 \times 4}, \quad C_{4 \times 2}, \quad D_{2 \times 2}.
$$

For the products $AB$, $BA$, $BC$, $CB$, $AC$, $CA$, $AD$, $DA$, determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

---

### Solution

#### Step 1. State the dimension compatibility condition for matrix multiplication

Two matrices $X$ and $Y$ can be multiplied to form the product $XY$ **if and only if** the number of columns in $X$ (the inner dimension of the first matrix) equals the number of rows in $Y$ (the inner dimension of the second matrix).

If matrix $X$ has size $m \times k$ and matrix $Y$ has size $k \times n$:

$$
X_{m \times k} \cdot Y_{k \times n} = (XY)_{m \times n}
$$

The resulting matrix $XY$ will have size $m \times n$ ( outer dimensions ). If the inner dimensions do not match ($k \neq k'$), the product is **undefined**.

---

#### Step 2. Analyze each product

1. **Product $AB$:**
   - Inner dimensions: $A_{2 \times \mathbf{3}}$ and $B_{\mathbf{3} \times 4}$.
   - Since $3 = 3$, the product is **defined**.
   - **Size of $AB$:** $2 \times 4$.

2. **Product $BA$:**
   - Inner dimensions: $B_{3 \times \mathbf{4}}$ and $A_{\mathbf{2} \times 3}$.
   - Since $4 \neq 2$, the product is **undefined**.

3. **Product $BC$:**
   - Inner dimensions: $B_{3 \times \mathbf{4}}$ and $C_{\mathbf{4} \times 2}$.
   - Since $4 = 4$, the product is **defined**.
   - **Size of $BC$:** $3 \times 2$.

4. **Product $CB$:**
   - Inner dimensions: $C_{4 \times \mathbf{2}}$ and $B_{\mathbf{3} \times 4}$.
   - Since $2 \neq 3$, the product is **undefined**.

5. **Product $AC$:**
   - Inner dimensions: $A_{2 \times \mathbf{3}}$ and $C_{\mathbf{4} \times 2}$.
   - Since $3 \neq 4$, the product is **undefined**.

6. **Product $CA$:**
   - Inner dimensions: $C_{4 \times \mathbf{2}}$ and $A_{\mathbf{2} \times 3}$.
   - Since $2 = 2$, the product is **defined**.
   - **Size of $CA$:** $4 \times 3$.

7. **Product $AD$:**
   - Inner dimensions: $A_{2 \times \mathbf{3}}$ and $D_{\mathbf{2} \times 2}$.
   - Since $3 \neq 2$, the product is **undefined**.

8. **Product $DA$:**
   - Inner dimensions: $D_{2 \times \mathbf{2}}$ and $A_{\mathbf{2} \times 3}$.
   - Since $2 = 2$, the product is **defined**.
   - **Size of $DA$:** $2 \times 3$.

---

#### Step 3. Summary of Results

$$
\begin{aligned}
AB &: \text{Defined, size } 2 \times 4 \\
BA &: \text{Undefined} \\
BC &: \text{Defined, size } 3 \times 2 \\
CB &: \text{Undefined} \\
AC &: \text{Undefined} \\
CA &: \text{Defined, size } 4 \times 3 \\
AD &: \text{Undefined} \\
DA &: \text{Defined, size } 2 \times 3
\end{aligned}
$$