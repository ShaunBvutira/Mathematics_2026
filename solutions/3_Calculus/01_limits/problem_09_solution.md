### Exercise 9. One-Sided Limits and an Asymptote

#### Question

Analyze the left-hand and right-hand limits of

$$
f(x) = \frac{1}{x - 2}
$$

as $x \to 2$. Does the two-sided limit exist? Interpret the result on a sketch of the graph and identify the vertical asymptote.

---

### Solution

#### Step 1. Analyze the Left-Hand Limit ($x \to 2^-$)

When $x$ approaches $2$ from the left ($x \to 2^-$), $x$ takes values strictly smaller than $2$ (for example, $x = 1.9, 1.99, 1.999$):
- The numerator is the positive constant $1$.
- The denominator $x - 2$ is **negative** and approaches $0$ from below ($x - 2 \to 0^-$).
- Dividing a positive constant by an arbitrarily small negative number produces a negative number of arbitrarily large magnitude:

$$
\lim_{x \to 2^-} \frac{1}{x - 2} = -\infty
$$

| $x$ (approaching from left) | $x - 2$ | $f(x) = \frac{1}{x - 2}$ |
| :--- | :--- | :--- |
| $1.9$ | $-0.1$ | $-10$ |
| $1.99$ | $-0.01$ | $-100$ |
| $1.999$ | $-0.001$ | $-1{,}000$ |

---

#### Step 2. Analyze the Right-Hand Limit ($x \to 2^+$)

When $x$ approaches $2$ from the right ($x \to 2^+$), $x$ takes values strictly greater than $2$ (for example, $x = 2.1, 2.01, 2.001$):
- The numerator is the positive constant $1$.
- The denominator $x - 2$ is **positive** and approaches $0$ from above ($x - 2 \to 0^+$).
- Dividing a positive constant by an arbitrarily small positive number produces a positive number of arbitrarily large magnitude:

$$
\lim_{x \to 2^+} \frac{1}{x - 2} = +\infty
$$

| $x$ (approaching from right) | $x - 2$ | $f(x) = \frac{1}{x - 2}$ |
| :--- | :--- | :--- |
| $2.1$ | $+0.1$ | $+10$ |
| $2.01$ | $+0.01$ | $+100$ |
| $2.001$ | $+0.001$ | $+1{,}000$ |

---

#### Step 3. Determine Existence of the Two-Sided Limit

A two-sided limit $\lim_{x \to 2} f(x)$ exists as a finite real number if and only if both one-sided limits exist as finite real numbers and are equal. Here:
1. Neither one-sided limit is finite (both diverge infinitely).
2. Even in the extended real sense, the left-hand limit ($-\infty$) and right-hand limit ($+\infty$) go in opposite directions ($-\infty \neq +\infty$).

Therefore, the two-sided limit **$\lim_{x \to 2} \frac{1}{x - 2}$ does not exist**.

---

#### Step 4. Identify the Vertical Asymptote and Sketch Interpretation

- **Vertical Asymptote:** Because at least one one-sided limit of $f(x)$ is infinite as $x \to 2$, the vertical line **$x = 2$** is a **vertical asymptote** of the graph.

- **Geometric Interpretation on the Sketch:**
  The graph of $f(x) = \frac{1}{x - 2}$ is the standard rectangular hyperbola $y = \frac{1}{x}$ shifted **$2$ units to the right**:
  - **Vertical Asymptote ($x = 2$):** Draw a dashed vertical line at $x = 2$. The curve never touches or crosses this line because $x = 2$ is excluded from the domain.
  - **Left Branch ($x < 2$):** Lies in the region below the $x$-axis for $x \in (-\infty, 2)$, passing through the $y$-intercept $\left(0, -\frac{1}{2}\right)$ and $(1, -1)$, and plunging steeply downward toward $-\infty$ as it hugs the left side of the dashed line $x = 2$.
  - **Right Branch ($x > 2$):** Lies entirely in Quadrant I for $x \in (2, +\infty)$, shooting steeply upward toward $+\infty$ as it hugs the right side of the dashed line $x = 2$, and passing through $(3, 1)$ and $\left(4, \frac{1}{2}\right)$.
  - **Horizontal Asymptote ($y = 0$):** As $x \to \pm\infty$, $\frac{1}{x - 2} \to 0$, so both branches flatten out along the $x$-axis ($y = 0$).