### Problem 6. A Logarithmic Function

#### Question

Analyze the domain, zero, and monotonicity of

$$
f(x) = \ln x - x + 1.
$$

Explain why the analysis must begin with the domain.

---

### Solution

#### Step 1. Determine the Domain of $f(x)$

Examine each term in $f(x) = \ln x - x + 1$:
- The linear part $-x + 1$ is defined for all real numbers $x \in \mathbb{R}$.
- The natural logarithm $\ln x$ is defined over the real numbers if and only if its argument is strictly positive ($x > 0$).

Intersecting these conditions gives the domain of $f(x)$:

$$
D_f = (0, +\infty)
$$

*(Boundary behavior: As $x \to 0^+$, $\ln x \to -\infty$ and $-x + 1 \to 1$, so $\lim_{x \to 0^+} f(x) = -\infty$, giving a vertical asymptote along the positive $y$-axis $x = 0$. As $x \to +\infty$, $\lim_{x \to +\infty} (\ln x - x + 1) = -\infty$ because linear growth dominates logarithmic growth.)*

---

#### Step 2. First Derivative, Critical Points, and Monotonicity

Differentiate $f(x) = \ln x - x + 1$ on its domain $(0, +\infty)$:

$$
\begin{aligned}
f'(x)
&= \frac{d}{dx}(\ln x - x + 1) \\
&= \frac{1}{x} - 1 \\
&= \frac{1 - x}{x}, \qquad x > 0
\end{aligned}
$$

1. **Critical Points:**
   Set $f'(x) = 0$ inside $D_f = (0, +\infty)$:

   $$
   \frac{1 - x}{x} = 0 \implies 1 - x = 0 \implies x = 1
   $$

   Since $1 \in (0, +\infty)$, **$x = 1$** is the unique critical point in the domain.

2. **Sign Analysis of $f'(x)$ and Monotonicity:**
   Because $x > 0$ everywhere on $D_f = (0, +\infty)$, the denominator of $f'(x) = \frac{1 - x}{x}$ is always positive. Thus, the sign of $f'(x)$ is determined solely by the numerator $1 - x$:

| Interval | Test Point | Sign of $(1 - x)$ | Sign of $x$ | Sign of $f'(x)$ | Behavior of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $(0, 1)$ | $x = \frac{1}{2}$ | $+$ | $+$ | **$+$** ($f'\!\left(\frac{1}{2}\right) = 1 > 0$) | **Strictly increasing** |
| $(1, +\infty)$ | $x = 2$ | $-$ | $+$ | **$-$** ($f'(2) = -\frac{1}{2} < 0$) | **Strictly decreasing** |

**Summary of Monotonicity:**
- **$f(x)$ is strictly increasing** on $(0, 1]$.
- **$f(x)$ is strictly decreasing** on $[1, +\infty)$.

3. **Global Maximum:**
   At $x = 1$, $f'(x)$ changes sign from positive to negative, so $f$ attains a local and **global (absolute) maximum** at $x = 1$:

   $$
   f_{\text{max}} = f(1) = \ln(1) - 1 + 1 = 0 - 1 + 1 = 0 \quad \text{at } (1, 0)
   $$

---

#### Step 3. Find and Verify the Uniqueness of the Zero

1. **Direct Evaluation at $x = 1$:**
   From Step 2, substituting $x = 1$ gives:

   $$
   f(1) = \ln(1) - 1 + 1 = 0
   $$

   So **$x = 1$** is a zero of $f(x)$ (giving the $x$-intercept $(1, 0)$, where the graph touches the $x$-axis tangentially without crossing it).

2. **Proof That $x = 1$ Is the Only Zero:**
   Because $f(x)$ is strictly increasing on $(0, 1]$ and strictly decreasing on $[1, +\infty)$, $f(1) = 0$ is the strict global maximum of $f(x)$ on $(0, +\infty)$:
   - For all $x \in (0, 1)$: $f(x) < f(1) = 0$.
   - For all $x \in (1, +\infty)$: $f(x) < f(1) = 0$.

   Therefore, $f(x) \le 0$ everywhere on $(0, +\infty)$ with equality if and only if $x = 1$. Thus, **$x = 1$ is the unique zero** of $f(x)$ (and this simultaneously proves the classic logarithmic inequality $\ln x \le x - 1$ for all $x > 0$).

---

#### Step 4. Explain Why the Analysis Must Begin with the Domain

1. **Avoiding Spurious Intervals and False Sign Changes:**
   Look at the algebraic formula for the derivative:

   $$
   f'(x) = \frac{1 - x}{x}
   $$

   As a standalone rational expression, $\frac{1 - x}{x}$ appears to be defined for negative numbers $x < 0$ (where it would evaluate to a negative value, since $1 - x > 0$ and $x < 0$). Without first establishing that $D_f = (0, +\infty)$, one might mistakenly include $(-\infty, 0)$ in the sign table and claim that $f(x)$ is decreasing on $(-\infty, 0)$—even though $f(x)$ does not exist at all for $x \le 0$.
2. **Defining the Valid Search Space for Zeros and Critical Points:**
   The domain sets the exact universe of admissible inputs. Any candidate critical point or zero must belong to $D_f = (0, +\infty)$ to be valid; points outside $(0, +\infty)$ cannot correspond to points on the graph.
3. **Establishing Boundary Behavior:**
   Knowing that the domain starts at $x = 0$ (open endpoint $0^+$) tells us immediately where the graph begins ($x \to 0^+ \implies f(x) \to -\infty$), rather than searching for behavior as $x \to -\infty$.