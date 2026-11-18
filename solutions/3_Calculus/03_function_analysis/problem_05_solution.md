### Problem 5. An Exponential Function with a Maximum

#### Question

Analyze the monotonicity and extrema of

$$f(x) = x e^{-x}.$$

Also examine the behavior as $x \to \infty$ and explain how the limit affects the shape of the graph on the right-hand side.

---

### Solution

#### Step 1. Domain and Intercepts

- **Domain:** Both $x$ and $e^{-x}$ are defined and smooth for all real numbers, so $D_f = \mathbb{R} = (-\infty, +\infty)$.
- **Intercepts:** Since $e^{-x} > 0$ for all $x \in \mathbb{R}$, $f(x) = 0 \iff x = 0$. The graph crosses both axes at a single point: the origin **$(0, 0)$**.
- **Sign of $f(x)$:**
  - For $x < 0$: $f(x) < 0$ (below the $x$-axis),
  - For $x > 0$: $f(x) > 0$ (above the $x$-axis).

---

#### Step 2. First Derivative and Critical Points

Apply the Product Rule $(uv)' = u'v + uv'$ with $u(x) = x$ ($u'(x) = 1$) and $v(x) = e^{-x}$ ($v'(x) = -e^{-x}$ by the Chain Rule):

$$\begin{aligned} f'(x) &= (1)e^{-x} + x(-e^{-x}) \\ &= e^{-x} - x e^{-x} \\ &= (1 - x)e^{-x} \end{aligned}$$

Set $f'(x) = 0$ to locate all critical points:

$$(1 - x)e^{-x} = 0$$

Because $e^{-x} > 0$ for every real number $x$, the exponential factor never vanishes. Dividing both sides by $e^{-x}$ gives the unique critical number:

$$1 - x = 0 \implies x = 1$$

Evaluate $f(1)$ to obtain the coordinates of the critical point:

$$f(1) = 1 \cdot e^{-1} = \frac{1}{e} \approx 0.368 \implies P\left(1, \frac{1}{e}\right)$$

---

#### Step 3. Sign Analysis of $f'(x)$ and Monotonicity

The critical point $x = 1$ splits the domain $(-\infty, +\infty)$ into two intervals: $(-\infty, 1)$ and $(1, +\infty)$. Because $e^{-x} > 0$ everywhere, the sign of $f'(x) = (1 - x)e^{-x}$ matches the sign of $(1 - x)$:

| Interval | Test Point | Sign of $(1 - x)$ | Sign of $e^{-x}$ | Sign of $f'(x)$ | Behavior of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $(-\infty, 1)$ | $x = 0$ | $+$ | $+$ | **$+$** ($f'(0) = 1 > 0$) | **Strictly increasing** |
| $(1, +\infty)$ | $x = 2$ | $-$ | $+$ | **$-$** ($f'(2) = -e^{-2} < 0$) | **Strictly decreasing** |

**Summary of Monotonicity:**
- **$f(x)$ is strictly increasing** on $(-\infty, 1]$.
- **$f(x)$ is strictly decreasing** on $[1, +\infty)$.

---

#### Step 4. Classify the Extremum (Local and Global Maximum)

- **First Derivative Test:** At $x = 1$, $f'(x)$ changes sign from **positive ($+$)** on $(-\infty, 1)$ to **negative ($-$)** on $(1, +\infty)$. Thus, $f$ has a **local maximum** at $x = 1$.
- **Global Maximum:** Because $f(x)$ increases continuously on $(-\infty, 1]$ and decreases continuously on $[1, +\infty)$, no other point in $\mathbb{R}$ can achieve a higher output. Therefore, $f$ attains its **global (absolute) maximum** at $x = 1$:

  $$f_{\text{max}} = f(1) = \frac{1}{e} \quad \text{at } \left(1, \frac{1}{e}\right)$$

- **Minimum:** As $x \to -\infty$, $x \to -\infty$ and $e^{-x} \to +\infty$, so $\lim_{x \to -\infty} x e^{-x} = -\infty$. Hence, the function has **no local or global minimum**.

---

#### Step 5. Behavior as $x \to +\infty$ and Effect on the Right-Hand Graph

1. **Limit as $x \to +\infty$:**
   Rewrite $f(x)$ as a quotient to resolve the $\infty \cdot 0$ indeterminate form:

   $$\lim_{x \to +\infty} x e^{-x} = \lim_{x \to +\infty} \frac{x}{e^x}$$

   Because exponential growth dominates linear growth (or by L'Hôpital's Rule, $\lim_{x \to +\infty} \frac{1}{e^x} = 0$):

   $$\lim_{x \to +\infty} x e^{-x} = 0$$

   Since $f(x) = \frac{x}{e^x} > 0$ for all $x > 0$, the function approaches $0$ strictly from above ($f(x) \to 0^+$).

2. **How the Limit Shapes the Right-Hand Side of the Graph:**
   - **Horizontal Asymptote ($y = 0$):** The positive $x$-axis ($y = 0$) acts as a **one-sided horizontal asymptote** as $x \to +\infty$ (whereas on the left, as $x \to -\infty$, the curve plunges to $-\infty$).
   - **Positive Tail Above the Axis:** After peaking at $\left(1, \frac{1}{e}\right)$, the curve decreases steadily for all $x > 1$ without ever touching or crossing the $x$-axis again ($f(x) > 0$ for every $x > 0$).
   - **Concavity Shift (Inflection Point at $x = 2$):** Differentiating again gives $f''(x) = (x - 2)e^{-x}$, which changes sign from negative to positive at $x = 2$ ($f(2) = \frac{2}{e^2} \approx 0.271$). Thus, as the graph descends from the peak $\left(1, \frac{1}{e}\right)$, it is initially concave down on $(1, 2)$, transitions to **concave up** on $(2, +\infty)$, and flattens smoothly into an exponential tail hugging the top of the $x$-axis.

```text
      y
      ^
 1/e -|       * Max (1, 1/e)
      |      / \
      |     /   * Inflection (2, 2/e^2)
      |    /     \__
  ----+---*---------+------------------> x (y = 0, Horizontal Asymptote)
     -1  (0,0)      2      4      6
      |  /
      | /
      |/