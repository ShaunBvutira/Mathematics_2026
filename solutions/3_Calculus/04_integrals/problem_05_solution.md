### Problem 5. The Same Substitution in a Different Context

#### Question

Compute

$$
\int x e^{x^2} \, dx.
$$

First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

---

### Solution

#### Step 1. Structural Comparison with Problem 4

Compare the integrand of Problem 4 with the integrand of Problem 5 side by side:

| Feature | Problem 4: $\int 2x(x^2 + 1)^4 \, dx$ | Problem 5: $\int x e^{x^2} \, dx$ |
| :--- | :--- | :--- |
| **Inner function $u(x)$** | $u(x) = x^2 + 1$ (quadratic) | $u(x) = x^2$ (quadratic) |
| **Derivative $u'(x)$** | $u'(x) = 2x$ | $u'(x) = 2x$ |
| **Outer function $g'(u)$** | $g'(u) = u^4$ (power function) | $g'(u) = e^u$ (exponential function) |
| **Linear factor in integrand** | $2x$ (matches $u'(x)$ with factor $1$) | $x = \frac{1}{2}(2x)$ (matches $u'(x)$ up to constant factor $\frac{1}{2}$) |

**What Is Common Despite the Different Appearance:**
1. **Identical Chain-Rule Architecture:** Although Problem 4 is purely algebraic (a polynomial power) and Problem 5 is transcendental (an exponential), both integrands share the exact same composite structure:

   $$
   \text{(constant)} \cdot u'(x) \cdot g'\bigl(u(x)\bigr)
   $$

   In both cases, an inner quadratic function ($x^2 + 1$ vs. $x^2$) is nested inside an outer function, while a linear factor proportional to $x$ sits outside.
2. **Same Substitution Mechanism:** Because $\frac{d}{dx}(x^2 + 1) = \frac{d}{dx}(x^2) = 2x$, setting $u = x^2$ collapses the variable factor $x \, dx$ into $\frac{1}{2} \, du$. The only difference is whether we apply the Power Rule ($\int u^4 \, du$) or the Exponential Rule ($\int e^u \, du$) once the substitution is complete.

---

#### Step 2. Set Up the Substitution $u = x^2$

Choose the exponent as the new variable:

$$
u = x^2
$$

Differentiate $u$ with respect to $x$:

$$
\frac{du}{dx} = 2x \implies du = 2x \, dx \implies x \, dx = \frac{1}{2} \, du
$$

---

#### Step 3. Compute the Integral

Rewrite the integrand to group $x \, dx$ together, substitute $u = x^2$ and $x \, dx = \frac{1}{2} \, du$, and integrate:

$$
\begin{aligned}
\int x e^{x^2} \, dx
&= \int e^{x^2} \cdot (x \, dx) \\
&= \int e^u \cdot \frac{1}{2} \, du \\
&= \frac{1}{2} \int e^u \, du \\
&= \frac{1}{2} e^u + C
\end{aligned}
$$

Substitute $u = x^2$ back to express the result in terms of $x$:

$$
\int x e^{x^2} \, dx = \frac{1}{2} e^{x^2} + C, \qquad C \in \mathbb{R}
$$

---

#### Step 4. Verify the Result by Differentiation

Differentiate $F(x) = \frac{1}{2} e^{x^2} + C$ with respect to $x$ using the Chain Rule:

$$
\begin{aligned}
F'(x)
&= \frac{d}{dx}\left(\frac{1}{2} e^{x^2} + C\right) \\
&= \frac{1}{2} \cdot e^{x^2} \cdot \frac{d}{dx}(x^2) + 0 \\
&= \frac{1}{2} e^{x^2} \cdot 2x \\
&= x e^{x^2}
\end{aligned}
$$

Because $F'(x)$ matches the original integrand identically, the antiderivative is verified.