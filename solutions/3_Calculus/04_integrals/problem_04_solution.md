### Problem 4. Substitution as Reversing the Chain Rule

#### Question

Compute

$$
\int 2x(x^2 + 1)^4 \, dx.
$$

Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

---

### Solution

#### Step 1. Identify the Substitution Variable $u$ and Its Derivative

Examine the composite structure of the integrand $2x(x^2 + 1)^4$. The expression $(x^2 + 1)^4$ consists of an outer fourth-power function applied to an inner quadratic expression:

$$
u(x) = x^2 + 1
$$

Differentiate $u(x)$ with respect to $x$ to find its differential $du$:

$$
\frac{du}{dx} = \frac{d}{dx}(x^2 + 1) = 2x \implies du = 2x \, dx
$$

**Observation:** The factor $2x$ multiplying $(x^2 + 1)^4$ is **precisely** the derivative $u'(x)$ of the inner function $u = x^2 + 1$. Thus, the integrand has the exact Chain Rule pattern $\int g'(u(x)) \cdot u'(x) \, dx$ with $g'(u) = u^4$.

---

#### Step 2. Compute the Integral via $u$-Substitution

Rewrite the integral to group $2x \, dx$ together, then substitute $u = x^2 + 1$ and $du = 2x \, dx$:

$$
\begin{aligned}
\int 2x(x^2 + 1)^4 \, dx
&= \int (x^2 + 1)^4 \cdot (2x \, dx) \\
&= \int u^4 \, du
\end{aligned}
$$

Apply the Power Rule $\int u^4 \, du = \frac{u^{4 + 1}}{4 + 1} + C = \frac{u^5}{5} + C$:

$$
\int u^4 \, du = \frac{u^5}{5} + C
$$

Substitute $u = x^2 + 1$ back to express the antiderivative in terms of the original variable $x$:

$$
\int 2x(x^2 + 1)^4 \, dx = \frac{(x^2 + 1)^5}{5} + C, \qquad C \in \mathbb{R}
$$

---

#### Step 3. Verify the Result by Differentiation

Differentiate $F(x) = \frac{1}{5}(x^2 + 1)^5 + C$ with respect to $x$ using the Chain Rule:

$$
\begin{aligned}
F'(x)
&= \frac{d}{dx}\left[\frac{1}{5}(x^2 + 1)^5 + C\right] \\
&= \frac{1}{5} \cdot 5(x^2 + 1)^4 \cdot \frac{d}{dx}(x^2 + 1) + 0 \\
&= (x^2 + 1)^4 \cdot 2x \\
&= 2x(x^2 + 1)^4
\end{aligned}
$$

Because $F'(x)$ matches the original integrand identically, the antiderivative is verified.