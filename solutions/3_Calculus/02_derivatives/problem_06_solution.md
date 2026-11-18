### Problem 6. Product Rule and Trigonometry

#### Question

For

$$
f(x) = x\sin x + \cos x
$$

compute the derivative and simplify the result. Then compute $f'(0)$ and interpret the direction of the tangent line at that point.

---

### Solution

#### Step 1. Differentiate $f(x)$ term by term

Apply the sum rule $\frac{d}{dx}[x\sin x + \cos x] = \frac{d}{dx}(x\sin x) + \frac{d}{dx}(\cos x)$:

1. **First term ($x\sin x$) via the Product Rule $(uv)' = u'v + uv'$:**
   Set $u(x) = x$ (so $u'(x) = 1$) and $v(x) = \sin x$ (so $v'(x) = \cos x$):

   $$
   \frac{d}{dx}(x\sin x) = (1)\sin x + x\cos x = \sin x + x\cos x
   $$

2. **Second term ($\cos x$):**

   $$
   \frac{d}{dx}(\cos x) = -\sin x
   $$

---

#### Step 2. Combine and simplify the derivative

Add the two derivatives together and cancel the opposite $\sin x$ terms:

$$
\begin{aligned}
f'(x)
&= (\sin x + x\cos x) + (-\sin x) \\
&= \sin x + x\cos x - \sin x \\
&= x\cos x
\end{aligned}
$$

Thus, the simplified derivative is:

$$
f'(x) = x\cos x
$$

---

#### Step 3. Compute $f'(0)$

Substitute $x = 0$ into $f'(x) = x\cos x$:

$$
f'(0) = 0 \cdot \cos(0) = 0 \cdot 1 = 0
$$

---

#### Step 4. Interpret the direction of the tangent line at $x = 0$

1. **Point of Tangency:**
   Evaluating the original function at $x = 0$ gives:

   $$
   f(0) = 0 \cdot \sin(0) + \cos(0) = 0 + 1 = 1
   $$

   So the point of tangency on the graph is $(0, 1)$.

2. **Direction and Equation of the Tangent Line:**
   - Because $f'(0) = 0$, the slope of the tangent line at $(0, 1)$ is **$m = 0$**.
   - A line with zero slope is **horizontal** (parallel to the $x$-axis), pointing neither upward nor downward.
   - Its equation is $y = 1$.

3. **Local Behavior Around $x = 0$:**
   Near $x = 0$, $\cos x > 0$:
   - For $x < 0$ (just to the left of $0$), $f'(x) = x\cos x < 0$, so the graph is decreasing.
   - For $x > 0$ (just to the right of $0$), $f'(x) = x\cos x > 0$, so the graph is increasing.
   
   Consequently, the horizontal tangent line at $(0, 1)$ marks a **local minimum** where the graph levels off before turning upward.