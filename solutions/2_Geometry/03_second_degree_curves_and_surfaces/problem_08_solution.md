### Exercise 8. Sphere

Reduce the general second-degree 3D equation

$$
x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

---

### Solution

#### Step 1. Reduce to canonical form by completing the square

Group the terms containing $x$, $y$, and $z$ together, and move the constant term to the right-hand side:

$$
(x^2 - 4x) + (y^2 + 2y) + (z^2 - 6z) = 2
$$

Complete the square for each variable:
- For $x$: half of $-4$ is $-2$, squared is $(-2)^2 = 4$.
- For $y$: half of $2$ is $1$, squared is $1^2 = 1$.
- For $z$: half of $-6$ is $-3$, squared is $(-3)^2 = 9$.

Add $4$, $1$, and $9$ to both sides of the equation:

$$
(x^2 - 4x + 4) + (y^2 + 2y + 1) + (z^2 - 6z + 9) = 2 + 4 + 1 + 9
$$

Rewrite as squared binomials:

$$
(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16
$$

This is the **canonical form** of the sphere equation, $(x - h)^2 + (y - k)^2 + (z - l)^2 = R^2$.

---

#### Step 2. Identify the center and radius

Comparing $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$ with standard form $(x - h)^2 + (y - k)^2 + (z - l)^2 = R^2$:

- **Center $(h, k, l)$:** $(2, -1, 3)$
- **Radius $R$:** $\sqrt{16} = 4$

---

#### Step 3. Select two points on the sphere

We can construct points on the sphere by moving $R = 4$ units along the coordinate directions from the center $(2, -1, 3)$:

1. **Point $P_1$:** Move $4$ units along the positive $x$-axis from the center:
   $$
   P_1 = (2 + 4, -1, 3) = (6, -1, 3)
   $$

2. **Point $P_2$:** Move $4$ units along the positive $z$-axis from the center:
   $$
   P_2 = (2, -1, 3 + 4) = (2, -1, 7)
   $$

---

#### Step 4. Substitute both points into both forms of the equation

##### Test Point $P_1(6, -1, 3)$:

1. **Canonical Form:** $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$
   $$
   \begin{aligned}
   \text{LHS} &= (6 - 2)^2 + (-1 + 1)^2 + (3 - 3)^2 \\
             &= 4^2 + 0^2 + 0^2 \\
             &= 16 + 0 + 0 = 16 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

2. **General Form:** $x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0$
   $$
   \begin{aligned}
   \text{LHS} &= 6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2 \\
             &= 36 + 1 + 9 - 24 - 2 - 18 - 2 \\
             &= 46 - 46 = 0 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

---

##### Test Point $P_2(2, -1, 7)$:

1. **Canonical Form:** $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$
   $$
   \begin{aligned}
   \text{LHS} &= (2 - 2)^2 + (-1 + 1)^2 + (7 - 3)^2 \\
             &= 0^2 + 0^2 + 4^2 \\
             &= 0 + 0 + 16 = 16 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

2. **General Form:** $x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0$
   $$
   \begin{aligned}
   \text{LHS} &= 2^2 + (-1)^2 + 7^2 - 4(2) + 2(-1) - 6(7) - 2 \\
             &= 4 + 1 + 49 - 8 - 2 - 42 - 2 \\
             &= 54 - 54 = 0 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

Both forms evaluate correctly for both test points, confirming that the canonical form $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$ is correct.