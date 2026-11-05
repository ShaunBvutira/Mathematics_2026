### Exercise 2. Circle by Completing the Square

Reduce the general second-degree equation

$$
x^2 + y^2 - 6x + 4y - 3 = 0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

---

### Solution

#### Step 1. Reduce to canonical form by completing the square

Group the $x$-terms and $y$-terms together, and move the constant term to the right-hand side:

$$
(x^2 - 6x) + (y^2 + 4y) = 3
$$

Complete the square for both variables:
- For $x$: take half of $-6$ (which is $-3$) and square it: $(-3)^2 = 9$.
- For $y$: take half of $4$ (which is $2$) and square it: $2^2 = 4$.

Add $9$ and $4$ to both sides of the equation to maintain equality:

$$
(x^2 - 6x + 9) + (y^2 + 4y + 4) = 3 + 9 + 4
$$

Rewrite the perfect square trinomials as squared binomials:

$$
(x - 3)^2 + (y + 2)^2 = 16
$$

This is the **canonical form** of the circle equation, $(x - h)^2 + (y - k)^2 = R^2$.

---

#### Step 2. Identify the center and radius

Comparing $(x - 3)^2 + (y + 2)^2 = 16$ with the standard form $(x - h)^2 + (y - k)^2 = R^2$:

- **Center $(h, k)$:** $(3, -2)$
- **Radius $R$:** $\sqrt{16} = 4$

---

#### Step 3. Select two simple points on the circle

We can find simple integer points by adding or subtracting the radius $R = 4$ from the center $(3, -2)$ along the horizontal or vertical directions:

1. **Point $P_1$ (Topmost point):** Move $4$ units up from the center $(3, -2)$:
   $$
   P_1 = (3, -2 + 4) = (3, 2)
   $$

2. **Point $P_2$ (Rightmost point):** Move $4$ units right from the center $(3, -2)$:
   $$
   P_2 = (3 + 4, -2) = (7, -2)
   $$

---

#### Step 4. Substitute both points into both forms of the equation

##### Test Point $P_1(3, 2)$:

1. **Canonical Form:** $(x - 3)^2 + (y + 2)^2 = 16$
   $$
   \begin{aligned}
   \text{LHS} &= (3 - 3)^2 + (2 + 2)^2 \\
             &= 0^2 + 4^2 \\
             &= 0 + 16 = 16 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

2. **General Form:** $x^2 + y^2 - 6x + 4y - 3 = 0$
   $$
   \begin{aligned}
   \text{LHS} &= 3^2 + 2^2 - 6(3) + 4(2) - 3 \\
             &= 9 + 4 - 18 + 8 - 3 \\
             &= 21 - 21 = 0 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

---

##### Test Point $P_2(7, -2)$:

1. **Canonical Form:** $(x - 3)^2 + (y + 2)^2 = 16$
   $$
   \begin{aligned}
   \text{LHS} &= (7 - 3)^2 + (-2 + 2)^2 \\
             &= 4^2 + 0^2 \\
             &= 16 + 0 = 16 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

2. **General Form:** $x^2 + y^2 - 6x + 4y - 3 = 0$
   $$
   \begin{aligned}
   \text{LHS} &= 7^2 + (-2)^2 - 6(7) + 4(-2) - 3 \\
             &= 49 + 4 - 42 - 8 - 3 \\
             &= 53 - 53 = 0 = \text{RHS} \quad \checkmark
   \end{aligned}
   $$

Both forms evaluate correctly for both test points, confirming that the canonical form $(x - 3)^2 + (y + 2)^2 = 16$ is correct.