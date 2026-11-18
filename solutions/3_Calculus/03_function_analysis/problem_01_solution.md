### Problem 1. A Cubic Polynomial

#### Question

Analyze the monotonicity and extrema of

$$f(x) = x^3 - 3x^2 + 2.$$

Sketch the graph based on the results and mark the critical points.

---

### Solution

#### Step 1. Domain and First Derivative

Since $f(x) = x^3 - 3x^2 + 2$ is a polynomial, it is defined and differentiable everywhere on $\mathbb{R} = (-\infty, +\infty)$.

Differentiate $f(x)$ term by term using the power rule:

$$f'(x) = \frac{d}{dx}(x^3 - 3x^2 + 2) = 3x^2 - 6x$$

Factor out $3x$ to make sign analysis straightforward:

$$f'(x) = 3x(x - 2)$$

---

#### Step 2. Find the Critical Points

Set $f'(x) = 0$ to find all stationary points (since $f'(x)$ is defined for all $x \in \mathbb{R}$, there are no singular critical points):

$$\begin{aligned} 3x(x - 2) &= 0 \\ x = 0 \quad &\text{or} \quad x = 2 \end{aligned}$$

Evaluate $f(x)$ at both critical $x$-values to obtain the coordinates of the critical points on the graph:
1. **At $x = 0$:**
   $$f(0) = 0^3 - 3(0)^2 + 2 = 2 \implies P_1(0, 2)$$
2. **At $x = 2$:**
   $$f(2) = 2^3 - 3(2)^2 + 2 = 8 - 12 + 2 = -2 \implies P_2(2, -2)$$

---

#### Step 3. Sign Analysis of $f'(x)$ and Monotonicity

The critical numbers $x = 0$ and $x = 2$ divide the domain $(-\infty, +\infty)$ into three open intervals: $(-\infty, 0)$, $(0, 2)$, and $(2, +\infty)$. Test the sign of $f'(x) = 3x(x - 2)$ on each interval:

| Interval | Test Point | Sign of $3x$ | Sign of $(x - 2)$ | Sign of $f'(x)$ | Behavior of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $(-\infty, 0)$ | $x = -1$ | $-$ | $-$ | **$+$** ($f'(-1) = 9 > 0$) | **Strictly increasing** |
| $(0, 2)$ | $x = 1$ | $+$ | $-$ | **$-$** ($f'(1) = -3 < 0$) | **Strictly decreasing** |
| $(2, +\infty)$ | $x = 3$ | $+$ | $+$ | **$+$** ($f'(3) = 9 > 0$) | **Strictly increasing** |

**Summary of Monotonicity:**
- **$f(x)$ is strictly increasing** on $(-\infty, 0]$ and on $[2, +\infty)$.
- **$f(x)$ is strictly decreasing** on $[0, 2]$.

---

#### Step 4. Classify the Local Extrema

Apply the First Derivative Test at each critical number:

1. **At $x = 0$:**
   $f'(x)$ changes sign from **positive ($+$)** on $(-\infty, 0)$ to **negative ($-$)** on $(0, 2)$. Therefore, $f$ has a **local maximum** at $x = 0$:

   $$f_{\text{max}} = f(0) = 2 \quad \text{at } (0, 2)$$

2. **At $x = 2$:**
   $f'(x)$ changes sign from **negative ($-$)** on $(0, 2)$ to **positive ($+$)** on $(2, +\infty)$. Therefore, $f$ has a **local minimum** at $x = 2$:

   $$f_{\text{min}} = f(2) = -2 \quad \text{at } (2, -2)$$

*(Note: Since $\lim_{x \to -\infty} f(x) = -\infty$ and $\lim_{x \to +\infty} f(x) = +\infty$, the function has no global maximum or global minimum on $\mathbb{R}$.)*

---

#### Step 5. Auxiliary Points and Graph Sketch

To make the sketch accurate, locate the axis intercepts and the inflection point ($f''(x) = 6x - 6 = 0 \implies x = 1, f(1) = 0$):
- **$y$-intercept:** $(0, 2)$ (also the local maximum).
- **$x$-intercepts ($x^3 - 3x^2 + 2 = 0$):**
  Factoring $(x - 1)(x^2 - 2x - 2) = 0$ yields three $x$-intercepts:
  - $x = 1 \implies (1, 0)$ (also the inflection point of symmetry),
  - $x = 1 - \sqrt{3} \approx -0.73 \implies (1 - \sqrt{3}, 0)$,
  - $x = 1 + \sqrt{3} \approx 2.73 \implies (1 + \sqrt{3}, 0)$.

```text
      y
      ^
    3 |
    2 |        * Max (0, 2)
    1 |       / \
  ----+------*---+---*---------*-----> x
   -1 |     /    0   1 (1,0)   2   3
   -1 |    /          \       /
   -2 |   /            * Min (2, -2)
   -3 |  /