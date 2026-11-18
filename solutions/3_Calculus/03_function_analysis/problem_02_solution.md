### Problem 2. A Parabola from the Perspective of the Derivative

#### Question

For

$$
f(x) = x^2 - 4x + 1,
$$

find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

---

### Solution

#### Step 1. Find the minimum using the derivative

1. **Compute the first derivative:**
   Differentiate $f(x) = x^2 - 4x + 1$ with respect to $x$:

   $$
   f'(x) = \frac{d}{dx}(x^2 - 4x + 1) = 2x - 4
   $$

2. **Find the critical point:**
   Set $f'(x) = 0$ to locate where the tangent line is horizontal:

   $$
   \begin{aligned}
   2x - 4 &= 0 \\
   2x &= 4 \\
   x &= 2
   \end{aligned}
   $$

3. **Verify that $x = 2$ is a global minimum:**
   - **First Derivative Sign Analysis:**
     - For $x < 2$: $f'(x) = 2x - 4 < 0$, so $f(x)$ is strictly decreasing on $(-\infty, 2]$.
     - For $x > 2$: $f'(x) = 2x - 4 > 0$, so $f(x)$ is strictly increasing on $[2, +\infty)$.
   - **Second Derivative Test:**
     $f''(x) = 2 > 0$ everywhere, meaning the graph is strictly concave up on all of $\mathbb{R}$.

   Because $f(x)$ decreases before $x = 2$ and increases after $x = 2$, the point $x = 2$ is both a local and **global minimum**.

4. **Evaluate the minimum value:**
   Substitute $x = 2$ back into $f(x)$:

   $$
   f(2) = 2^2 - 4(2) + 1 = 4 - 8 + 1 = -3
   $$

   Thus, the minimum value is **$-3$**, attained at the point **$(2, -3)$**.

---

#### Step 2. Compare with the vertex form

Complete the square on $f(x) = x^2 - 4x + 1$ to rewrite the quadratic in vertex form $f(x) = a(x - h)^2 + k$:

$$
\begin{aligned}
f(x)
&= (x^2 - 4x + 4) - 4 + 1 \\
&= (x - 2)^2 - 3
\end{aligned}
$$

- Because $(x - 2)^2 \ge 0$ for all real numbers $x$, with equality $(x - 2)^2 = 0$ if and only if $x = 2$, we have:

  $$
  f(x) = (x - 2)^2 - 3 \ge 0 - 3 = -3
  $$

- Reading the vertex $(h, k)$ directly from $f(x) = (x - 2)^2 - 3$ gives the vertex **$(2, -3)$** and minimum value **$-3$**—matching the calculus result identically.

---

#### Step 3. Explain why both approaches lead to the same point

1. **Geometric Meaning (Horizontal Tangent vs. Turning Point of Symmetry):**
   A smooth upward-opening parabola decreases on the left side of its axis of symmetry and increases on the right side. At the exact lowest point—the **vertex**—the curve smoothly transitions from falling to rising, meaning its instantaneous slope must pass through zero ($f'(x) = 0$). Setting the derivative equal to zero locates that unique horizontal tangent line, which occurs precisely at the vertex.

2. **Algebraic Equivalence (Differentiating the Vertex Form):**
   In general, any quadratic written in vertex form is $f(x) = a(x - h)^2 + k$ (with $a > 0$). Differentiating this form directly via the Chain Rule gives:

   $$
   f'(x) = 2a(x - h)
   $$

   Setting $f'(x) = 0$ immediately yields $2a(x - h) = 0 \implies x = h$, and substituting $x = h$ gives $f(h) = a(0)^2 + k = k$. Thus, solving $f'(x) = 0$ is algebraically identical to finding the shift $h$ that makes the squared term $(x - h)^2$ vanish.