### Problem 4. A Function with Two Vertical Asymptotes

#### Question

Analyze

$$
f(x) = \frac{1}{x^2 - 1}.
$$

Determine the domain, asymptotes, sign, and monotonicity on the intervals of the domain. Explain why each interval must be analyzed separately.

---

### Solution

#### Step 1. Determine the Domain of $f(x)$

Since $f(x) = \frac{1}{x^2 - 1}$ is a rational function, it is defined for all real numbers $x \in \mathbb{R}$ except where the denominator equals zero:

$$
x^2 - 1 = 0 \implies (x - 1)(x + 1) = 0 \implies x = -1 \quad \text{or} \quad x = 1
$$

Thus, the domain of $f(x)$ consists of **three disjoint open intervals**:

$$
D_f = \mathbb{R} \setminus \{-1, 1\} = (-\infty, -1) \cup (-1, 1) \cup (1, +\infty)
$$

*(Note also that $f(-x) = \frac{1}{(-x)^2 - 1} = \frac{1}{x^2 - 1} = f(x)$, so $f$ is an **even function** whose graph is symmetric with respect to the $y$-axis.)*

---

#### Step 2. Determine the Asymptotes

1. **Vertical Asymptotes ($x = -1$ and $x = 1$):**
   Factor the denominator as $x^2 - 1 = (x + 1)(x - 1)$ and examine the one-sided limits near both excluded points:
   - **Near $x = -1$:**
     - As $x \to -1^-$: $(x + 1) \to 0^-$ and $(x - 1) \to -2 < 0$, so $(x + 1)(x - 1) \to 0^+$ (product of two negatives):

       $$
       \lim_{x \to -1^-} \frac{1}{x^2 - 1} = +\infty
       $$

     - As $x \to -1^+$: $(x + 1) \to 0^+$ and $(x - 1) \to -2 < 0$, so $(x + 1)(x - 1) \to 0^-$:

       $$
       \lim_{x \to -1^+} \frac{1}{x^2 - 1} = -\infty
       $$

   - **Near $x = 1$:**
     - As $x \to 1^-$: $(x + 1) \to 2 > 0$ and $(x - 1) \to 0^-$, so $(x + 1)(x - 1) \to 0^-$:

       $$
       \lim_{x \to 1^-} \frac{1}{x^2 - 1} = -\infty
       $$

     - As $x \to 1^+$: $(x + 1) \to 2 > 0$ and $(x - 1) \to 0^+$, so $(x + 1)(x - 1) \to 0^+$:

       $$
       \lim_{x \to 1^+} \frac{1}{x^2 - 1} = +\infty
       $$

   Therefore, the lines **$x = -1$** and **$x = 1$** are both **vertical asymptotes**.

2. **Horizontal Asymptote ($y = 0$):**
   Compute the limits as $x \to \pm\infty$:

   $$
   \lim_{x \to \pm\infty} \frac{1}{x^2 - 1} = 0
   $$

   Therefore, the $x$-axis (**$y = 0$**) is a **horizontal asymptote** on both sides.

3. **Oblique (Slant) Asymptote:**
   None, because a horizontal asymptote exists as $x \to \pm\infty$.

---

#### Step 3. Sign Analysis of $f(x)$ (Zeros and Sign Intervals)

- **Zeros:** Since the numerator is the constant $1 \neq 0$, $f(x) = 0$ has no solution. The graph never crosses the $x$-axis.
- **$y$-intercept:** At $x = 0$, $f(0) = \frac{1}{0^2 - 1} = -1$, giving $(0, -1)$.
- **Sign on each interval of $D_f$:**
  Because the numerator $1 > 0$, the sign of $f(x)$ equals the sign of the denominator $x^2 - 1 = (x + 1)(x - 1)$:

| Interval of $D_f$ | Sign of $(x + 1)$ | Sign of $(x - 1)$ | Sign of $x^2 - 1$ | Sign of $f(x)$ | Graph Position |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $(-\infty, -1)$ | $-$ | $-$ | **$+$** | **$f(x) > 0$** | Above $x$-axis |
| $(-1, 1)$ | $+$ | $-$ | **$-$** | **$f(x) < 0$** | Below $x$-axis |
| $(1, +\infty)$ | $+$ | $+$ | **$+$** | **$f(x) > 0$** | Above $x$-axis |

---

#### Step 4. First Derivative, Critical Points, and Monotonicity

Rewrite $f(x) = (x^2 - 1)^{-1}$ and differentiate using the Chain Rule (or Quotient Rule):

$$
\begin{aligned}
f'(x)
&= -1 \cdot (x^2 - 1)^{-2} \cdot \frac{d}{dx}(x^2 - 1) \\
&= -\frac{2x}{(x^2 - 1)^2}, \qquad x \neq \pm 1
\end{aligned}
$$

1. **Critical Points:**
   Set $f'(x) = 0$:

   $$
   -\frac{2x}{(x^2 - 1)^2} = 0 \implies -2x = 0 \implies x = 0
   $$

   Since $0 \in (-1, 1) \subset D_f$, **$x = 0$** is the sole critical point in the domain, with $f(0) = -1$.

2. **Sign of $f'(x)$ and Monotonicity on Each Interval:**
   For every $x \in D_f$, the denominator $(x^2 - 1)^2 > 0$. Therefore, the sign of $f'(x) = -\frac{2x}{(x^2 - 1)^2}$ is strictly opposite to the sign of $x$, while respecting the breaks at the vertical asymptotes $x = -1$ and $x = 1$:

| Interval | Sign of $-2x$ | Sign of $(x^2 - 1)^2$ | Sign of $f'(x)$ | Monotonicity of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- |
| $(-\infty, -1)$ | $+$ (since $x < 0$) | $+$ | **$f'(x) > 0$** | **Strictly increasing** |
| $(-1, 0)$ | $+$ (since $x < 0$) | $+$ | **$f'(x) > 0$** | **Strictly increasing** |
| $(0, 1)$ | $-$ (since $x > 0$) | $+$ | **$f'(x) < 0$** | **Strictly decreasing** |
| $(1, +\infty)$ | $-$ (since $x > 0$) | $+$ | **$f'(x) < 0$** | **Strictly decreasing** |

3. **Local Extremum:**
   Inside the middle interval $(-1, 1)$, $f'(x)$ changes sign from positive on $(-1, 0)$ to negative on $(0, 1)$, so $f$ attains a **local maximum** at **$(0, -1)$** ($f_{\text{local max}} = -1$). (There is no global maximum or minimum because $f(x) \to \pm\infty$ near the asymptotes.)

---

#### Step 5. Explain Why Each Interval Must Be Analyzed Separately

1. **Domain Discontinuities Break Connectedness:**
   The vertical asymptotes at $x = -1$ and $x = 1$ partition the real line into three completely separate pieces: $(-\infty, -1)$, $(-1, 1)$, and $(1, +\infty)$. Because $f$ is undefined at $x = \pm 1$, the Mean Value Theorem and monotonicity theorems apply only on individual intervals where $f$ is continuous and differentiable.
2. **Sign Changes Across Singularities (Not Zeros):**
   Although $f(x)$ has no $x$-intercepts, it still changes sign across $x = -1$ (from $+$ to $-$) and across $x = 1$ (from $-$ to $+$). Crossing a vertical asymptote allows a function to jump from $+\infty$ directly to $-\infty$ without passing through zero.
3. **False Monotonicity Claims Across Asymptotes:**
   Notice that $f'(x) > 0$ on both $(-\infty, -1)$ and $(-1, 0)$. However, it would be **false** to claim that $f(x)$ is increasing on the union $(-\infty, -1) \cup (-1, 0)$:
   - Take $x_1 = -2 \in (-\infty, -1)$ and $x_2 = -\frac{1}{2} \in (-1, 0)$.
   - Even though $x_1 < x_2$ ($-2 < -0.5$), we have $f(-2) = \frac{1}{3} > f\left(-\frac{1}{2}\right) = -\frac{4}{3}$.
   
   Because the graph resets from $+\infty$ down to $-\infty$ as it crosses the vertical asymptote $x = -1$ (and similarly jumps from $-\infty$ up to $+\infty$ across $x = 1$), monotonicity holds **only within each separate interval**, never across the discontinuities.s