### Exercise 8. Row Operations and Their Reversibility

For

$$
A = 
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:
1. $R_2 \leftarrow R_2 - 2 R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

---

### Solution

#### Step 1. Perform operation 1: $R_2 \leftarrow R_2 - 2 R_1$

Subtract $2$ times Row 1 from Row 2:

- Row 2 calculation: $(2 - 2(1), 4 - 2(2), 1 - 2(-1)) = (0, 0, 3)$

The matrix becomes:

$$
A_1 = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

---

#### Step 2. Perform operation 2: $R_3 \leftarrow R_3 + R_1$

Add Row 1 to Row 3 of matrix $A_1$:

- Row 3 calculation: $(-1 + 1, 1 + 2, 3 + (-1)) = (0, 3, 2)$

The matrix becomes:

$$
A_2 = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

---

#### Step 3. Perform operation 3: Interchange $R_2$ and $R_3$

Swap the second and third rows of matrix $A_2$ ($R_2 \leftrightarrow R_3$):

The matrix becomes:

$$
A_3 = 
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

---

#### Step 4. State the reversing (inverse) operations

Elementary row operations are invertible, meaning each operation can be undone by another elementary row operation of the same type:

1. **Reversing Operation 1 ($R_2 \leftarrow R_2 - 2 R_1$):**
   Add $2$ times Row 1 back to Row 2:
   $$
   R_2 \leftarrow R_2 + 2 R_1
   $$

2. **Reversing Operation 2 ($R_3 \leftarrow R_3 + R_1$):**
   Subtract Row 1 from Row 3:
   $$
   R_3 \leftarrow R_3 - R_1
   $$

3. **Reversing Operation 3 (Interchange $R_2$ and $R_3$):**
   Interchange $R_2$ and $R_3$ again:
   $$
   R_2 \leftrightarrow R_3
   $$