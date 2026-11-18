### Exercise 6. From a Sequence to a Function — Limit at Infinity

#### Question

Compute

$$
\lim_{x \to \infty} \frac{3x^2 - x + 1}{5x^2 + 4x - 2}.
$$

Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

---

### Solution

#### Step 1. Factor out the highest power of $x$ ($x^2$)

Identify the highest-degree term in both the numerator and the denominator, which is $x^2$. For $x > 0$, divide every term in the numerator and the denominator by $x^2$:

$$
\begin{aligned}
\lim_{x \to \infty} \frac{3x^2 - x + 1}{5x^2 + 4x - 2}
&= \lim_{x \to \infty} \frac{\frac{3x^2}{x^2} - \frac{x}{x^2} + \frac{1}{x^2}}{\frac{5x^2}{x^2} + \frac{4x}{x^2} - \frac{2}{x^2}} \\
&= \lim_{x \to \infty} \frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}}
\end{aligned}
$$

---

#### Step 2. Apply limit laws as $x \to \infty$

Since $\lim_{x \to \infty} \frac{1}{x} = 0$ and $\lim_{x \to \infty} \frac{1}{x^2} = 0$, every term with $x$ in the denominator approaches $0$:

$$
\begin{aligned}
\lim_{x \to \infty} \frac{3 - \frac{1}{x} + \frac{1}{x^2}}{5 + \frac{4}{x} - \frac{2}{x^2}}
&= \frac{3 - 0 + 0}{5 + 0 - 0} \\
&= \frac{3}{5}
\end{aligned}
$$

The limit of the function is **$\frac{3}{5}$**.

---

#### Step 3. Comparison with Exercise 1

In Exercise 1, we evaluated $\lim_{n \to \infty} \frac{4n^2 - 3n + 1}{2n^2 + 5n - 7} = \frac{4}{2} = 2$. Comparing that sequence problem with this function problem shows identical algebraic mechanics alongside a broader domain:

##### What Stays the Same
1. **Algebraic Technique:** In both cases, we identify the highest power of the variable ($n^2$ vs. $x^2$), divide numerator and denominator by that dominant power, and use the fact that $\frac{1}{n^k} \to 0$ and $\frac{1}{x^k} \to 0$ for all $k > 0$.
2. **Dominant-Term Principle:** Lower-degree terms become negligible compared to the leading quadratic terms, so the limit equals the ratio of the leading coefficients ($\frac{3}{5}$ here, just as it was $\frac{4}{2}$ in Exercise 1).
3. **Asymptotic Value:** Restricting $x$ to positive integers ($x = n \in \mathbb{N}$) produces the sequence $a_n = \frac{3n^2 - n + 1}{5n^2 + 4n - 2}$, which converges to the exact same limit $\frac{3}{5}$ (Heine's definition of function limits).

##### What Changes When Moving from $n$ to a Real Variable $x$
1. **Domain (Discrete vs. Continuous):** A sequence index $n \in \mathbb{N} = \{1, 2, 3, \dots\}$ takes only isolated natural-number steps, whereas $x \in \mathbb{R}$ varies continuously across all real numbers (including fractions and irrationals) beyond any threshold $M$.
2. **Direction of Infinity ($+\infty$ vs. $-\infty$):** Because $n$ represents a counting index, $n \to \infty$ always means $n \to +\infty$. For a real variable $x$, one can also study $x \to -\infty$ (here, $\lim_{x \to -\infty} \frac{3x^2 - x + 1}{5x^2 + 4x - 2} = \frac{3}{5}$ as well).
3. **Geometric Interpretation:** A sequence limit describes the long-term target of discrete plotted points $(n, a_n)$, whereas $\lim_{x \to \infty} f(x) = \frac{3}{5}$ defines a **horizontal asymptote** $y = \frac{3}{5}$ that the continuous curve $y = f(x)$ approaches as it extends rightward.
4. **Domain Singularities:** Unlike a sequence defined for all $n \in \mathbb{N}$ (once $n$ exceeds any roots of the denominator), a rational function of $x$ can have vertical asymptotes at real roots of $5x^2 + 4x - 2 = 0$ (specifically at $x = \frac{-2 \pm \sqrt{14}}{5} \approx 0.348$ and $-1.148$), though both lie well to the left of large positive $x$.