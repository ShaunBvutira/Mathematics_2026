### Exercise 10. A Polynomial Through Three Points

Find a polynomial $p(x) = ax^2 + bx + c$ whose graph passes through $(0, 1)$, $(1, 3)$, and $(2, 9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

---

### Solution

#### Step 1. Form the system of linear equations

For the graph of $p(x) = ax^2 + bx + c$ to pass through a given point $(x_0, y_0)$, the condition $p(x_0) = y_0$ must hold:

1. **Point $(0, 1)$:**
   $$
   p(0) = a(0)^2 + b(0) + c = 1 \implies c = 1
   $$

2. **Point $(1, 3)$:**
   $$
   p(1) = a(1)^2 + b(1) + c = 3 \implies a + b + c = 3
   $$

3. **Point $(2, 9)$:**
   $$
   p(2) = a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9
   $$

This yields the following system of linear equations in unknowns $a, b, c$:

$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

---

#### Step 2. Solve the system by elimination / substitution

Substitute $c = 1$ into the second and third equations:

1. **Second equation:**
   $$
   a + b + 1 = 3 \implies a + b = 2
   $$

2. **Third equation:**
   $$
   4a + 2b + 1 = 9 \implies 4a + 2b = 8 \implies 2a + b = 4
   $$

Now solve the $2 \times 2$ reduced system:

$$
\begin{cases}
a + b = 2, \\
2a + b = 4.
\end{cases}
$$

Subtract the first equation from the second equation:

$$
(2a + b) - (a + b) = 4 - 2 \implies a = 2
$$

Substitute $a = 2$ back into $a + b = 2$:

$$
2 + b = 2 \implies b = 0
$$

Thus, the coefficients are:

$$
a = 2, \quad b = 0, \quad c = 1
$$

The required quadratic polynomial is:

$$
p(x) = 2x^2 + 1
$$

---

#### Step 3. Check consistency by evaluating all three points

Substitute $x = 0, 1, 2$ into $p(x) = 2x^2 + 1$:

1. **Check $(0, 1)$:**
   $$
   p(0) = 2(0)^2 + 1 = 0 + 1 = 1 \quad \checkmark \quad (\text{matches } y = 1)
   $$

2. **Check $(1, 3)$:**
   $$
   p(1) = 2(1)^2 + 1 = 2(1) + 1 = 3 \quad \checkmark \quad (\text{matches } y = 3)
   $$

3. **Check $(2, 9)$:**
   $$
   p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9 \quad \checkmark \quad (\text{matches } y = 9)
   $$

All three points satisfy $p(x) = 2x^2 + 1$, confirming the polynomial is correct.