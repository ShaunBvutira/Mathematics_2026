### Problem 7. A Trigonometric Composition

#### Question

For

$$
f(x) = \sin(x^2 + 1)
$$

compute the derivative. Explicitly identify the outer function, the inner function, and the derivative of the inner function. Finally, determine the sign of $f'(0)$.

---

### Solution

#### Step 1. Identify the outer function and the inner function

Decompose the composite function $f(x) = g(u(x))$ from the outside in:
- **Outer function:** $g(u) = \sin(u)$
- **Inner function:** $u(x) = x^2 + 1$

Checking the composition verifies that $g(u(x)) = \sin(x^2 + 1) = f(x)$.

---

#### Step 2. Compute the derivatives of the outer and inner functions

1. **Derivative of the outer function with respect to $u$:**
   $$
   g'(u) = \frac{d}{du}(\sin u) = \cos(u)
   $$

2. **Derivative of the inner function with respect to $x$:**
   $$
   u'(x) = \frac{d}{dx}(x^2 + 1) = 2x
   $$

---

#### Step 3. Apply the Chain Rule to compute $f'(x)$

Using the Chain Rule $\frac{d}{dx}[g(u(x))] = g'(u(x)) \cdot u'(x)$:

$$
\begin{aligned}
f'(x)
&= \cos\bigl(u(x)\bigr) \cdot u'(x) \\
&= \cos(x^2 + 1) \cdot 2x
\end{aligned}
$$

Writing the algebraic factor in front of the trigonometric factor gives:

$$
f'(x) = 2x\cos(x^2 + 1)
$$

---

#### Step 4. Compute $f'(0)$ and determine its sign

Substitute $x = 0$ into $f'(x) = 2x\cos(x^2 + 1)$:

$$
\begin{aligned}
f'(0)
&= 2(0) \cdot \cos(0^2 + 1) \\
&= 0 \cdot \cos(1) \\
&= 0
\end{aligned}
$$

**Sign Determination:**
- **$f'(0) = 0$ is neither positive nor negative (it is zero).**
- **Interpretation:** Because the derivative vanishes at $x = 0$, the graph of $f(x) = \sin(x^2 + 1)$ has a **horizontal tangent line** (slope $m = 0$) at the point $(0, \sin 1)$. Moreover, since $f(-x) = \sin((-x)^2 + 1) = \sin(x^2 + 1) = f(x)$, the function is even and symmetric about the $y$-axis, causing its slope at $x = 0$ to be zero.