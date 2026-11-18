### Problem 3. The Product Rule — Why Is It Needed?

#### Question

For

$$
f(x) = (x^2 + 1)e^x
$$

compute the derivative. Then compare the correct result with the incorrect idea

$$
f'(x) \stackrel{?}{=} (2x)e^x
$$

and explain which term is missing.

---

### Solution

#### Step 1. Identify the components and apply the Product Rule

The function $f(x) = (x^2 + 1)e^x$ is a product of two differentiable functions:

$$
u(x) = x^2 + 1, \qquad v(x) = e^x
$$

Compute the individual derivatives of each factor:

$$
u'(x) = \frac{d}{dx}(x^2 + 1) = 2x, \qquad v'(x) = \frac{d}{dx}(e^x) = e^x
$$

Apply the Product Rule $(uv)' = u'v + uv'$:

$$
\begin{aligned}
f'(x)
&= u'(x)v(x) + u(x)v'(x) \\
&= (2x)e^x + (x^2 + 1)e^x
\end{aligned}
$$

Factor out the common exponential term $e^x$ to write the derivative in compact form:

$$
f'(x) = (x^2 + 2x + 1)e^x = (x + 1)^2 e^x
$$

---

#### Step 2. Compare the correct derivative with the incorrect formula

- **Correct derivative:**
  $$
  f'(x) = 2xe^x + (x^2 + 1)e^x
  $$
- **Incorrect formula:**
  $$
  f'_{\text{incorrect}}(x) = (2x)e^x
  $$

Subtracting the two shows the exact discrepancy:

$$
f'(x) - f'_{\text{incorrect}}(x) = (x^2 + 1)e^x
$$

---

#### Step 3. Explain which term is missing and why

1. **The Missing Term:**
   The missing term is **$u(x)v'(x) = (x^2 + 1)e^x$** (the first factor multiplied by the derivative of the second factor).

2. **Why the Naive Formula Fails:**
   The incorrect expression $(2x)e^x$ comes from falsely assuming that the derivative of a product equals the product of the derivatives: $(uv)' = u' \cdot v'$ (since $(x^2 + 1)' = 2x$ and $(e^x)' = e^x$). In reality, differentiation distributes over *addition*, not *multiplication*.

3. **Geometric and Rate-of-Change Intuition:**
   Think of $f(x) = u(x)v(x)$ as the area of a rectangle with width $u(x) = x^2 + 1$ and height $v(x) = e^x$. When $x$ increases slightly by $\Delta x$, **both** dimensions grow simultaneously:
   - The width changes by $\Delta u \approx u'(x)\Delta x$, adding a vertical strip of area $v(x)\Delta u \approx (2x)e^x\Delta x$.
   - The height changes by $\Delta v \approx v'(x)\Delta x$, adding a horizontal strip of area $u(x)\Delta v \approx (x^2 + 1)e^x\Delta x$.
   
   The naive guess $(2x)e^x$ accounts only for the change in the polynomial factor $(x^2 + 1)$ while falsely treating $e^x$ as if it were a constant. Because $e^x$ is also changing at rate $e^x$, its contribution $(x^2 + 1)e^x$ must be added to capture the full rate of change of the product.