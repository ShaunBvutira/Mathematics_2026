### Exercise 3. Vector Normalization

For $v = (3, 4)^T$, find a unit vector $e$ with the same direction and orientation. Check that $\|e\| = 1$, reconstruct $v$ in the form $v = \|v\|e$, and explain what changes during normalization and what remains unchanged.

---

### Solution

#### Step 1. Calculate the magnitude of $v$

The length (magnitude) of vector $v = (v_1, v_2)^T$ is given by:

$$
\|v\| = \sqrt{v_1^2 + v_2^2}
$$

Substituting $v = (3, 4)^T$:

$$
\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

---

#### Step 2. Find the normalized unit vector $e$

A unit vector $e$ pointing in the exact same direction and orientation as $v$ is obtained by scaling $v$ by the reciprocal of its length:

$$
e = \frac{1}{\|v\|} v = \frac{1}{5} \begin{pmatrix} 3 \\ 4 \end{pmatrix} = \begin{pmatrix} \frac{3}{5} \\ \frac{4}{5} \end{pmatrix} = \begin{pmatrix} 0.6 \\ 0.8 \end{pmatrix}
$$

---

#### Step 3. Verify that $\|e\| = 1$

Calculate the magnitude of vector $e$:

$$
\begin{aligned}
\|e\| &= \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} \\
      &= \sqrt{\frac{9}{25} + \frac{16}{25}} \\
      &= \sqrt{\frac{25}{25}} \\
      &= \sqrt{1} = 1
\end{aligned}
$$

The norm check confirms that $e$ is indeed a unit vector.

---

#### Step 4. Reconstruct $v$ as $v = \|v\|e$

Using the calculated magnitude $\|v\| = 5$ and unit vector $e = \left(\frac{3}{5}, \frac{4}{5}\right)^T$:

$$
\|v\|e = 5 \begin{pmatrix} \frac{3}{5} \\ \frac{4}{5} \end{pmatrix} = \begin{pmatrix} 5 \cdot \frac{3}{5} \\ 5 \cdot \frac{4}{5} \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix} = v
$$

This decomposes $v$ into its magnitude ($\|v\| = 5$) and pure directional information ($e$).

---

#### Step 5. Explain what changes and what remains unchanged

- **What changes:**
  - **Length (Magnitude):** The length of the vector changes from its original magnitude ($\|v\| = 5$) to exactly $1$ unit ($\|e\| = 1$).

- **What remains unchanged:**
  - **Direction (Line of Action):** The angle/slope of the vector relative to the coordinate axes remains identical, as both components are scaled by the exact same positive scalar factor ($\frac{1}{5}$).
  - **Orientation (Sense/Sign):** Because the scaling factor $\frac{1}{\|v\|}$ is strictly positive, the arrow continues to point in the same direction along its line of action rather than reversing.