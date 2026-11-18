### Problem 1. Derivative of a Polynomial and the Slope of a Tangent Line

#### Question

For

$$
f(x) = 3x^5 - 2x^3 + 7x - 4
$$

find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

---

### Solution

#### Step 1. Differentiate $f(x)$ term by term

Apply the linearity of differentiation (sum/difference and constant multiple rules) together with the power rule $\frac{d}{dx}(x^n) = nx^{n-1}$ and the constant rule $\frac{d}{dx}(c) = 0$:

$$
\begin{aligned}
f'(x)
&= \frac{d}{dx}\left(3x^5 - 2x^3 + 7x - 4\right) \\
&= 3 \cdot \frac{d}{dx}(x^5) - 2 \cdot \frac{d}{dx}(x^3) + 7 \cdot \frac{d}{dx}(x^1) - \frac{d}{dx}(4) \\
&= 3(5x^4) - 2(3x^2) + 7(1) - 0 \\
&= 15x^4 - 6x^2 + 7
\end{aligned}
$$

Thus, the derivative is:

$$
f'(x) = 15x^4 - 6x^2 + 7
$$

---

#### Step 2. Compute $f'(0)$ and $f'(1)$

1. **At $x = 0$:**
   $$
   f'(0) = 15(0)^4 - 6(0)^2 + 7 = 0 - 0 + 7 = 7
   $$

2. **At $x = 1$:**
   $$
   f'(1) = 15(1)^4 - 6(1)^2 + 7 = 15 - 6 + 7 = 16
   $$

---

#### Step 3. Determine the signs and interpret the tangent line slopes

1. **At $x = 0$ ($f(0) = -4$):**
   - **Sign:** $f'(0) = 7 > 0$ (**positive**).
   - **Geometric Interpretation:** The tangent line to the graph $y = f(x)$ at the point $(0, -4)$ has a positive slope of **$m = 7$**. Because the slope is positive, the tangent line slants upward from left to right (rising $7$ units vertically for every $1$ unit moved horizontally), indicating that $f(x)$ is increasing at $x = 0$.

2. **At $x = 1$ ($f(1) = 3 - 2 + 7 - 4 = 4$):**
   - **Sign:** $f'(1) = 16 > 0$ (**positive**).
   - **Geometric Interpretation:** The tangent line to the graph $y = f(x)$ at the point $(1, 4)$ has a positive slope of **$m = 16$**. Again, the tangent line slants upward from left to right, so $f(x)$ is also increasing at $x = 1$.

3. **Comparison Between the Two Points:**
   - Both derivatives are positive, so the graph rises at both $x = 0$ and $x = 1$.
   - Because $f'(1) = 16 > f'(0) = 7$, the tangent line at $(1, 4)$ is **more than twice as steep** as the tangent line at $(0, -4)$.