
### Problem 2. Powers, Roots, and the Domain

#### Question

Compute

$$
\int \left( 2\sqrt{x} + \frac{3}{x^2} - x^{1/3} \right) dx.
$$

First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

---

### Solution

#### Step 1. Determine the Domain of the Original Expression

Examine each term in the integrand $f(x) = 2\sqrt{x} + \frac{3}{x^2} - x^{1/3}$ individually over the real numbers:
- **First term ($2\sqrt{x}$):** The real square root requires a non-negative radicand, so $x \ge 0$.
- **Second term ($\frac{3}{x^2}$):** Division by zero is undefined, so $x^2 \neq 0 \implies x \neq 0$.
- **Third term ($-x^{1/3} = -\sqrt[3]{x}$):** The real cube root is defined for all $x \in \mathbb{R}$.

Intersecting all three conditions ($x \ge 0$, $x \neq 0$, and $x \in \mathbb{R}$) gives the domain of the original expression:

$$
D_f = (0, +\infty)
$$

---

#### Step 2. Rewrite Each Term as a Power of $x$

Convert roots to fractional exponents and reciprocals to negative exponents:
- $2\sqrt{x} = 2x^{1/2}$
- $\frac{3}{x^2} = 3x^{-2}$
- $-x^{1/3} = -x^{1/3}$ (already in power form)

Thus, the integral becomes:

$$
\int \left( 2x^{1/2} + 3x^{-2} - x^{1/3} \right) dx
$$

---

#### Step 3. Integrate Term by Term Using the Power Rule

Apply linearity and the Power Rule $\int x^n \, dx = \frac{x^{n+1}}{n+1} + C$ ($n \neq -1$) to each term on $(0, +\infty)$:

1. **First term ($2x^{1/2}$):**
   $$
   \int 2x^{1/2} \, dx = 2 \cdot \frac{x^{\frac{1}{2} + 1}}{\frac{1}{2} + 1} = 2 \cdot \frac{x^{3/2}}{\frac{3}{2}} = 2 \cdot \frac{2}{3}x^{3/2} = \frac{4}{3}x^{3/2}
   $$

2. **Second term ($3x^{-2}$):**
   $$
   \int 3x^{-2} \, dx = 3 \cdot \frac{x^{-2 + 1}}{-2 + 1} = 3 \cdot \frac{x^{-1}}{-1} = -3x^{-1} = -\frac{3}{x}
   $$

3. **Third term ($-x^{1/3}$):**
   $$
   -\int x^{1/3} \, dx = -\frac{x^{\frac{1}{3} + 1}}{\frac{1}{3} + 1} = -\frac{x^{4/3}}{\frac{4}{3}} = -\frac{3}{4}x^{4/3}
   $$

Combine the results and add the constant of integration $C$:

$$
\int \left( 2\sqrt{x} + \frac{3}{x^2} - x^{1/3} \right) dx = \frac{4}{3}x^{3/2} - \frac{3}{x} - \frac{3}{4}x^{4/3} + C, \qquad x > 0
$$

*(Equivalently in radical form: $\frac{4}{3}x\sqrt{x} - \frac{3}{x} - \frac{3}{4}x\sqrt[3]{x} + C$.)*

---

#### Step 4. Verify the Result by Differentiation

Differentiate $F(x) = \frac{4}{3}x^{3/2} - 3x^{-1} - \frac{3}{4}x^{4/3} + C$ with respect to $x$ for $x > 0$:

$$
\begin{aligned}
F'(x)
&= \frac{4}{3} \cdot \left(\frac{3}{2}x^{\frac{3}{2} - 1}\right) - 3 \cdot \left(-1 \cdot x^{-1 - 1}\right) - \frac{3}{4} \cdot \left(\frac{4}{3}x^{\frac{4}{3} - 1}\right) + 0 \\
&= 2x^{1/2} + 3x^{-2} - x^{1/3} \\
&= 2\sqrt{x} + \frac{3}{x^2} - x^{1/3}
\end{aligned}
$$

Since $F'(x)$ reproduces the exact original integrand on $(0, +\infty)$, the antiderivative is verified.