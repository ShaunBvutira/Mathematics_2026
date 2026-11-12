### Exercise 7. Choosing a Method Deliberately

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. One system with a triangular coefficient matrix:
   $$
   \begin{cases}
   2x - y = 3, \\
   4y = 8;
   \end{cases}
   $$
2. Three systems $Ax = b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. One $3 \times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

---

### Solution

#### Case 1. One system with a triangular coefficient matrix

- **Chosen Method:** **Back-substitution**.
- **Justification:**
  - **Matrix Structure:** The coefficient matrix $A = \begin{pmatrix} 2 & -1 \\ 0 & 4 \end{pmatrix}$ is already in **upper triangular form** (all entries below the main diagonal are zero). Because forward elimination has effectively already been completed, forming an augmented matrix for Gaussian elimination or computing $A^{-1}$ would perform redundant row operations.
  - **Number of Right-Hand Sides:** There is only a **single** right-hand side vector $b = \begin{pmatrix} 3 \\ 8 \end{pmatrix}$, making a direct bottom-up pass the fastest possible path ($O(n^2)$ operations with zero elimination overhead).

##### Complete Execution for Case 1:

1. **Solve the bottom equation for $y$:**
   $$
   4y = 8 \implies y = \frac{8}{4} = 2
   $$

2. **Substitute $y = 2$ upward into the first equation to solve for $x$:**
   $$
   2x - (2) = 3 \implies 2x = 5 \implies x = \frac{5}{2}
   $$

3. **Verification:**
   - First equation: $2\left(\frac{5}{2}\right) - 2 = 5 - 2 = 3$
   - Second equation: $4(2) = 8$

   The unique solution vector is $\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} \frac{5}{2} \\[1ex] 2 \end{pmatrix}$.

---

#### Case 2. Three systems $Ax = b_i$ ($i = 1, 2, 3$) with $A^{-1}$ already known

- **Chosen Method:** **Direct matrix-vector multiplication** ($x_i = A^{-1}b_i$ for each $i = 1, 2, 3$), or equivalently a single block matrix multiplication $X = A^{-1}B$ where $B = \begin{pmatrix} b_1 & b_2 & b_3 \end{pmatrix}$.
- **Justification:**
  - **Matrix Structure & Precomputed Asset:** Although $A$ has no special sparsity or triangular structure specified, the computationally expensive step—inverting $A$—has **already been paid**.
  - **Number of Right-Hand Sides:** Having **three distinct right-hand sides** ($b_1, b_2, b_3$) amortizes the cost of using an inverse. Applying $A^{-1}$ requires only matrix-vector products rather than repeating row operations across multiple augmented systems.

##### Plan and Reusable vs. Unnecessary Computations:

- **Execution Plan:** Compute $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$ directly via dot products of the rows of $A^{-1}$ with each column vector $b_i$.
- **Reusable Part:** The precomputed inverse matrix **$A^{-1}$** is reused across all three right-hand sides without modification.
- **Unnecessary Part:** Computing $\det A$, performing Gaussian elimination / row reduction on augmented matrices $[A \mid b_i]$, or re-deriving $A^{-1}$ via $[A \mid I]$ are completely unnecessary.

---

#### Case 3. One $3 \times 3$ system with unknown $A^{-1}$ and one target solution vector

- **Chosen Method:** **Gaussian elimination with back-substitution** applied to the single augmented matrix $[A \mid b]$.
- **Justification:**
  - **Matrix Structure:** $A$ is a general $3 \times 3$ matrix without guaranteed triangular structure, and $A^{-1}$ is not provided (nor is $A$ even guaranteed to be invertible beforehand).
  - **Number of Right-Hand Sides:** Because there is **only one right-hand side** $b$ and only **one solution vector** $x$ is needed, finding the full inverse $A^{-1}$ (which is equivalent to solving three separate systems $Ax = e_1, e_2, e_3$ simultaneously via $[A \mid I_3]$) does roughly three times as much work as required.

##### Plan and Reusable vs. Unnecessary Computations:

- **Execution Plan:**
  1. Form the $3 \times 4$ augmented matrix $[A \mid b]$.
  2. Apply elementary row operations (forward elimination) to reduce $[A \mid b]$ to row echelon form $[U \mid c]$, where $U$ is upper triangular.
  3. Check consistency (verifying there is no row of the form $[0 \quad 0 \quad 0 \mid \text{nonzero}]$) and solve for $x_3, x_2, x_1$ from bottom to top via back-substitution.
- **Reusable Part:** None of the inverse-finding work needs to be saved because there are no additional right-hand sides $b_2, b_3, \dots$ coming later. (If another right-hand side were ever introduced later, only the forward elimination multipliers/steps on $A$ would be reusable, not $b$.)
- **Unnecessary Part:**
  - Forming the $3 \times 6$ augmented matrix $[A \mid I_3]$ and reducing the upper triangle above the pivots to obtain **reduced row echelon form** for $A^{-1}$ is unnecessary.
  - Computing $3 \times 3$ determinants and cofactors (as required by Cramer's Rule or the adjugate formula $A^{-1} = \frac{1}{\det A}\operatorname{adj}(A)$) is also unnecessary overhead for a single $3 \times 3$ solution vector.