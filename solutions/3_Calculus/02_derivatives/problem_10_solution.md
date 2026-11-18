### Problem 10. The Tangent Line as an Application of the Derivative

#### Question

For

$$
f(x) = x^2 - 3x + 1
$$

find the equation of the tangent line at the point with $x = 2$. Give the point of tangency, the value $f'(2)$, the equation of the line, and verify that the point lies on the obtained tangent line.

---

### Solution

#### Step 1. Find the point of tangency $(2, f(2))$

Substitute $x = 2$ into the original function $f(x) = x^2 - 3x + 1$ to find the $y$-coordinate of the point on the graph:

$$
\begin{aligned}
f(2)
&= 2^2 - 3(2) + 1 \\
&= 4 - 6 + 1 \\
&= -1
\end{aligned}
$$

Thus, the **point of tangency** is:

$$
P(2, -1)
$$

---

#### Step 2. Compute the derivative $f'(x)$ and the slope $f'(2)$

Differentiate $f(x) = x^2 - 3x + 1$ term by term using the power rule:

$$
f'(x) = \frac{d}{dx}(x^2 - 3x + 1) = 2x - 3
$$

Evaluate the derivative at $x = 2$ to find the slope $m$ of the tangent line at $P(2, -1)$:

$$
f'(2) = 2(2) - 3 = 4 - 3 = 1
$$

Thus, the slope of the tangent line is **$m = f'(2) = 1$**.

---

#### Step 3. Write the equation of the tangent line

Use the point-slope form of a line $y - y_0 = m(x - x_0)$ with $(x_0, y_0) = (2, -1)$ and $m = 1$:

$$
\begin{aligned}
y - (-1) &= 1 \cdot (x - 2) \\
y + 1 &= x - 2 \\
y &= x - 3
\end{aligned}
$$

Thus, the **equation of the tangent line** is:

$$
y = x - 3
$$

*(In standard form: $x - y - 3 = 0$.)*

---

#### Step 4. Verify that the point of tangency lies on the tangent line

Substitute the coordinates of the point of tangency $(x, y) = (2, -1)$ into the tangent line equation $y = x - 3$:
- **Left-hand side (LHS):** $y = -1$
- **Right-hand side (RHS):** $x - 3 = 2 - 3 = -1$

Since $\text{LHS} = \text{RHS} = -1$, the point $(2, -1)$ satisfies the equation and lies on the tangent line $y = x - 3$.