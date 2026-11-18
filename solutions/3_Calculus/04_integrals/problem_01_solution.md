### Problem 1. Antiderivative and Verification

#### Question

For

$$
f(x) = 3x^2 - 4x + 5
$$

find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

---

### Solution

#### Step 1. Find One Antiderivative $F(x)$

Apply the linearity of integration (sum/difference rule and constant multiple rule) together with the power rule for antiderivatives, $\int x^n \, dx = \frac{x^{n+1}}{n+1}$ ($n \neq -1$), term by term:

1. **First term ($3x^2$):**
   $$
   \int 3x^2 \, dx = 3 \cdot \frac{x^{2+1}}{2+1} = 3 \cdot \frac{x^3}{3} = x^3
   $$

2. **Second term ($-4x = -4x^1$):**
   $$
   \int (-4x) \, dx = -4 \cdot \frac{x^{1+1}}{1+1} = -4 \cdot \frac{x^2}{2} = -2x^2
   $$

3. **Third term ($5 = 5x^0$):**
   $$
   \int 5 \, dx = 5x
   $$

Combining the three terms (choosing the integration constant $C = 0$) gives one specific antiderivative:

$$
F(x) = x^3 - 2x^2 + 5x
$$

---

#### Step 2. Write the Entire Family of Antiderivatives

Because any two antiderivatives of $f(x)$ on $(-\infty, +\infty)$ differ only by a constant, adding an arbitrary real constant $C$ yields the general indefinite integral—the entire family of antiderivatives:

$$
\int (3x^2 - 4x + 5) \, dx = x^3 - 2x^2 + 5x + C, \qquad C \in \mathbb{R}
$$

---

#### Step 3. Verify the Result by Differentiation

Differentiate the general antiderivative $F_C(x) = x^3 - 2x^2 + 5x + C$ with respect to $x$ using the power rule and the fact that the derivative of any constant is $0$:

$$
\begin{aligned}
\frac{d}{dx}\bigl(x^3 - 2x^2 + 5x + C\bigr)
&= \frac{d}{dx}(x^3) - 2\frac{d}{dx}(x^2) + 5\frac{d}{dx}(x) + \frac{d}{dx}(C) \\
&= 3x^2 - 2(2x) + 5(1) + 0 \\
&= 3x^2 - 4x + 5 \\
&= f(x)
\end{aligned}
$$

Because $F_C'(x) = f(x)$ for every $x \in \mathbb{R}$ and every choice of $C \in \mathbb{R}$, the antiderivative is verified.

---

#### Step 4. Explain the Meaning of the Constant $C$

1. **Algebraic Meaning (Loss of Constant Information Under Differentiation):**
   Differentiation measures instantaneous rate of change, so any additive constant term vanishes when taking a derivative ($\frac{d}{dx}(C) = 0$). Consequently, functions such as $x^3 - 2x^2 + 5x$, $x^3 - 2x^2 + 5x + 7$, and $x^3 - 2x^2 + 5x - 10$ all share the exact same derivative $3x^2 - 4x + 5$. When reversing differentiation, $C$ restores all possible constant terms that could have been present prior to differentiating.

2. **Geometric Meaning (Vertical Shifts of a Family of Curves):**
   Graphically, changing $C$ shifts the cubic curve $y = x^3 - 2x^2 + 5x + C$ **vertically up or down** without altering its shape, steepness, or slope. At every vertical line $x = x_0$, all curves in the family have parallel tangent lines with the exact same slope $f(x_0) = 3x_0^2 - 4x_0 + 5$.

3. **Physical / Initial-Value Meaning:**
   If $f(x) = 3x^2 - 4x + 5$ represents a rate of change (such as velocity at time $x$), then $F_C(x)$ represents the accumulated quantity (such as position). The constant $C = F_C(0)$ encodes the **initial value** at $x = 0$, which must be specified by an initial condition to pin down one unique curve from the infinite family.