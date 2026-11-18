### Problem 5. The Chain Rule as Working Through Layers

#### Question

For

$$
f(x) = (3x^2 - 2x + 1)^5
$$

identify the inner and outer functions, compute their derivatives, and combine the result according to the chain rule. Explain the origin of the additional factor.

---

### Solution

#### Step 1. Identify the inner and outer functions

Decompose the composite function $f(x) = g(u(x))$ into two layers from the inside out:
- **Inner function:** $u(x) = 3x^2 - 2x + 1$
- **Outer function:** $g(u) = u^5$

Checking the composition confirms that $g(u(x)) = (3x^2 - 2x + 1)^5 = f(x)$.

---

#### Step 2. Compute the derivatives of both layers

1. **Derivative of the outer function with respect to $u$:**
   $$
   g'(u) = \frac{d}{du}(u^5) = 5u^4
   $$

2. **Derivative of the inner function with respect to $x$:**
   $$
   u'(x) = \frac{d}{dx}(3x^2 - 2x + 1) = 6x - 2
   $$

---

#### Step 3. Combine the results using the Chain Rule

According to the Chain Rule, $\frac{d}{dx}[g(u(x))] = g'(u(x)) \cdot u'(x)$:

$$
\begin{aligned}
f'(x)
&= 5\bigl(u(x)\bigr)^4 \cdot u'(x) \\
&= 5(3x^2 - 2x + 1)^4 \cdot (6x - 2)
\end{aligned}
$$

Factoring out $2$ from $(6x - 2) = 2(3x - 1)$ simplifies the leading coefficient:

$$
f'(x) = 10(3x - 1)(3x^2 - 2x + 1)^4
$$

---

#### Step 4. Explain the origin of the additional factor $(6x - 2)$

1. **Rate-of-Change Multiplication:**
   The outer function $g(u) = u^5$ does not depend directly on $x$; it depends on the intermediate quantity $u = 3x^2 - 2x + 1$.
   - The outer derivative $g'(u) = 5u^4$ tells us how fast the output $f$ changes **per unit change in $u$** ($\frac{df}{du}$).
   - The inner derivative $u'(x) = 6x - 2$ tells us how fast $u$ itself changes **per unit change in $x$** ($\frac{du}{dx}$).

2. **Chaining Rates Together:**
   When $x$ increases by a tiny amount $\Delta x$, the inner expression shifts by $\Delta u \approx (6x - 2)\Delta x$. That shift in $u$ then drives a change in the fifth power of $\Delta f \approx 5u^4 \Delta u$. Substituting $\Delta u$ gives:

   $$
   \Delta f \approx 5u^4 \cdot (6x - 2)\Delta x \implies \frac{df}{dx} = \frac{df}{du} \cdot \frac{du}{dx} = 5(3x^2 - 2x + 1)^4(6x - 2)
   $$

3. **Why Omitting It Fails:**
   Simply applying the power rule as $5(3x^2 - 2x + 1)^4$ would falsely assume that $u$ changes at the exact same rate as $x$ ($\frac{du}{dx} = 1$). Because the quadratic expression $3x^2 - 2x + 1$ speeds up or slows down at rate $6x - 2$, multiplying by the additional factor $(6x - 2)$ scales the outer rate by the true speed of the inner layer.