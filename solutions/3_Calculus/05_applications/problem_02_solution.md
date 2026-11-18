### Problem 2. Maximum Area of a Rectangle

#### Question

A rectangle has perimeter $40$.
1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

---

### Solution

#### 1. Write the Area as a Function of the Length of One Side

Let $x$ denote the length of one side of the rectangle and $y$ denote the length of the adjacent side.

Use the perimeter condition $P = 40$ to express $y$ in terms of $x$:

$$
\begin{aligned}
2x + 2y &= 40 \\
x + y &= 20 \\
y &= 20 - x
\end{aligned}
$$

The area $A$ of the rectangle is the product of its two adjacent sides:

$$
\begin{aligned}
A(x) &= x \cdot y \\
&= x(20 - x) \\
&= 20x - x^2
\end{aligned}
$$

Thus, the area as a function of one side length $x$ is:

$$
A(x) = 20x - x^2
$$

---

#### 2. Determine the Domain Resulting from the Geometry of the Problem

For a non-degenerate physical rectangle, both side lengths $x$ and $y$ must be strictly positive:

$$
\begin{aligned}
x > 0 \qquad &\text{and} \qquad y > 0 \\
x > 0 \qquad &\text{and} \qquad 20 - x > 0 \\
x > 0 \qquad &\text{and} \qquad x < 20
\end{aligned}
$$

Combining both inequalities gives the geometric domain:

$$
D_A = (0, 20)
$$

*(Note: At the boundary endpoints $x = 0$ and $x = 20$, one side collapses to length $0$ and the area degenerates to $A(0) = A(20) = 0$.)*

---

#### 3. Find the Dimensions That Give the Maximum Area

Differentiate $A(x) = 20x - x^2$ with respect to $x$:

$$
A'(x) = \frac{d}{dx}(20x - x^2) = 20 - 2x
$$

Set $A'(x) = 0$ to find the critical point inside $(0, 20)$:

$$
\begin{aligned}
20 - 2x &= 0 \\
2x &= 20 \\
x &= 10
\end{aligned}
$$

Since $10 \in (0, 20)$, substitute $x = 10$ back into $y = 20 - x$ to find the second dimension:

$$
y = 20 - 10 = 10
$$

The dimensions that give the maximum area are **$10 \times 10$** (a square of side length $10$), yielding a maximum area of:

$$
A(10) = 10 \cdot 10 = 100
$$

---

#### 4. Justify That the Point Found Actually Gives a Maximum

We can verify that $x = 10$ produces a **global maximum** on $(0, 20)$ in three complementary ways:

1. **Second Derivative Test (Concavity):**
   Compute the second derivative of $A(x)$:

   $$
   A''(x) = \frac{d}{dx}(20 - 2x) = -2 < 0 \qquad \text{for all } x \in (0, 20)
   $$

   Because $A''(10) = -2 < 0$, the graph of $A(x)$ is strictly concave down everywhere on $(0, 20)$, confirming that $x = 10$ is both a local and **global maximum**.

2. **First Derivative Sign Analysis:**
   - For $x \in (0, 10)$: $A'(x) = 20 - 2x > 0$, so $A(x)$ is strictly increasing on $(0, 10]$.
   - For $x \in (10, 20)$: $A'(x) = 20 - 2x < 0$, so $A(x)$ is strictly decreasing on $[10, 20)$.

   Since $A(x)$ rises continuously up to $x = 10$ and falls continuously afterward, $A(10) = 100$ is strictly greater than $A(x)$ for every other $x \in (0, 20)$.

3. **Algebraic Verification (Completing the Square):**
   Rewriting $A(x)$ in vertex form gives:

   $$
   A(x) = -(x^2 - 20x + 100) + 100 = -(x - 10)^2 + 100
   $$

   Since $-(x - 10)^2 \le 0$ for all $x$, we have $A(x) \le 100$, with equality if and only if $x = 10$.