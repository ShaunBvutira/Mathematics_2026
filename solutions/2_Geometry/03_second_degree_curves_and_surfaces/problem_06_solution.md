### Exercise 6. Shifted Ellipse

Reduce the general second-degree equation

$$
4x^2 + 9y^2 - 16x + 18y - 11 = 0
$$

to canonical form. Give the center and semi-axis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

---

### Solution

#### Step 1. Reduce to canonical form by completing the square

Group the terms containing $x$ and $y$ together, and move the constant term to the right-hand side:

$$
(4x^2 - 16x) + (9y^2 + 18y) = 11
$$

Factor out the leading coefficients of $x^2$ and $y^2$:

$$
4(x^2 - 4x) + 9(y^2 + 2y) = 11
$$

Complete the square inside each set of parentheses:
- For $x$: half of $-4$ is $-2$, squared is $(-2)^2 = 4$.
- For $y$: half of $2$ is $1$, squared is $1^2 = 1$.

Add the corresponding weighted values to the right-hand side:
- $4 \cdot 4 = 16$ for the $x$-term.
- $9 \cdot 1 = 9$ for the $y$-term.

$$
4(x^2 - 4x + 4) + 9(y^2 + 2y + 1) = 11 + 16 + 9
$$

Rewrite as squared binomials:

$$
4(x - 2)^2 + 9(y + 1)^2 = 36
$$

Divide both sides by $36$ to set the right-hand side to $1$:

$$
\frac{4(x - 2)^2}{36} + \frac{9(y + 1)^2}{36} = 1
$$

Simplify the fractions:

$$
\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1
$$

This is the **canonical form** of the shifted ellipse, $\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1$.

---

#### Step 2. Identify the center and semi-axis lengths

Comparing $\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1$ with the standard form:

- **Center $(h, k)$:** $(2, -1)$
- **Horizontal semi-axis ($a$):** $a^2 = 9 \implies a = \sqrt{9} = 3$
- **Vertical semi-axis ($b$):** $b^2 = 4 \implies b = \sqrt{4} = 2$

*(Since $a = 3 > b = 2$, the ellipse is horizontal with major axis length $2a = 6$ and minor axis length $2b = 4$.)*

---

#### Step 3. Check by substituting the center into the original left-hand side

Substitute the center coordinates $(x, y) = (2, -1)$ into the original general expression $LHS = 4x^2 + 9y^2 - 16x + 18y - 11$:

$$
\begin{aligned}
\text{LHS} &= 4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11 \\
          &= 4(4) + 9(1) - 32 - 18 - 11 \\
          &= 16 + 9 - 32 - 18 - 11 \\
          &= 25 - 61 \\
          &= -36
\end{aligned}
$$

##### Consistency Verification with Canonical Form:

Rearranging the completed-square step before dividing by $36$ gives:

$$
4(x - 2)^2 + 9(y + 1)^2 - 36 = 4x^2 + 9y^2 - 16x + 18y - 11
$$

Evaluating at the center $(x, y) = (2, -1)$:
- The squared terms vanish: $4(2 - 2)^2 + 9(-1 + 1)^2 = 0 + 0 = 0$.
- The remaining constant value is precisely **$-36$**.

This confirms that the original polynomial evaluated at the center equals $-36$, which directly balances the $+36$ required on the right-hand side to achieve canonical unity ($1$).