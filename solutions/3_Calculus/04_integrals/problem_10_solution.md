### Problem 10. Definite Integral and Checking the Result

#### Question

Before carrying out the exact calculation, estimate the possible range of values of the integral

$$
\int_{0}^{2} (x^2 + 1) \, dx,
$$

using

$$
1 \le x^2 + 1 \le 5
$$

on $[0, 2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

---

### Solution

#### Step 1. Estimate the Range of Values Before Computing the Integral

1. **Apply the Comparison (Bounding) Property of Definite Integrals:**
   If $m \le f(x) \le M$ for all $x \in [a, b]$ with $a \le b$, then the area under $y = f(x)$ on $[a, b]$ must lie between the area of the inscribed rectangle of height $m$ and the circumscribed rectangle of height $M$:

   $$
   m(b - a) \le \int_{a}^{b} f(x) \, dx \le M(b - a)
   $$

2. **Substitute the Given Bounds and Interval Endpoints:**
   On the interval $[a, b] = [0, 2]$ (whose width is $b - a = 2 - 0 = 2$), the integrand $f(x) = x^2 + 1$ increases monotonically from $f(0) = 1$ to $f(2) = 5$, so:

   $$
   1 \le x^2 + 1 \le 5 \qquad \text{for all } x \in [0, 2]
   $$

   Integrating across the inequality over $[0, 2]$ yields:

   $$
   \begin{aligned}
   \int_{0}^{2} 1 \, dx &\le \int_{0}^{2} (x^2 + 1) \, dx \le \int_{0}^{2} 5 \, dx \\
   1 \cdot (2 - 0) &\le \int_{0}^{2} (x^2 + 1) \, dx \le 5 \cdot (2 - 0) \\
   2 &\le \int_{0}^{2} (x^2 + 1) \, dx \le 10
   \end{aligned}
   $$

   *(Furthermore, because $f(x) = x^2 + 1$ is strictly greater than $1$ for $x > 0$ and strictly less than $5$ for $x < 2$, the exact value must lie strictly inside the open interval $(2, 10)$.)*

---

#### Step 2. Compute the Definite Integral Exactly

Find an antiderivative of $f(x) = x^2 + 1$:

$$
F(x) = \int (x^2 + 1) \, dx = \frac{x^3}{3} + x
$$

Apply the Fundamental Theorem of Calculus (Newton–Leibniz formula) on $[0, 2]$:

$$
\begin{aligned}
\int_{0}^{2} (x^2 + 1) \, dx
&= \left[ \frac{x^3}{3} + x \right]_{0}^{2} \\
&= \left( \frac{2^3}{3} + 2 \right) - \left( \frac{0^3}{3} + 0 \right) \\
&= \left( \frac{8}{3} + 2 \right) - 0 \\
&= \frac{8}{3} + \frac{6}{3} \\
&= \frac{14}{3} = 4\frac{2}{3} \approx 4.67
\end{aligned}
$$

---

#### Step 3. Compare the Exact Result with the Earlier Estimate

Convert the exact value $\frac{14}{3}$ to a mixed number or decimal and place it within the estimated range $[2, 10]$:

$$
2 < \frac{14}{3} \approx 4.67 < 10
$$

- **Lower bound check:** $\frac{14}{3} = 4.67 > 2$ (exceeds the minimum rectangle area by $2.67$).
- **Upper bound check:** $\frac{14}{3} = 4.67 < 10$ (falls safely below the maximum rectangle area by $5.33$).
- **Geometric reasonableness:** Because $y = x^2 + 1$ is concave up ($f''(x) = 2 > 0$), the curve bows below the straight secant line connecting $(0, 1)$ and $(2, 5)$ (whose trapezoid area is $\frac{1 + 5}{2} \cdot 2 = 6$). Thus, getting $\frac{14}{3} \approx 4.67 < 6$ confirms both the bounding check and the concavity geometry.

---

#### Step 4. Explain What Types of Computational Errors This Check Can Detect

Bounding a definite integral before calculating acts as an immediate **sanity check** that catches gross algebraic and arithmetic mistakes whenever an answer falls outside $[2, 10]$:

1. **Sign Errors in the Antiderivative or Evaluation:**
   - Accidentally subtracting instead of adding when evaluating $F(2)$ (e.g., $\frac{8}{3} - 2 = \frac{2}{3} \approx 0.67 < 2$) or reversing the limits $F(0) - F(2) = -\frac{14}{3} < 0$ immediately violates the lower bound $2$.
2. **Missing or Inverted Factors in the Power Rule:**
   - Multiplying by the exponent instead of dividing (differentiating instead of integrating: $[2x]_{0}^{2} = 4$, or writing $3x^3 + x \implies 26 > 10$) or forgetting to divide by $3$ ($\left[x^3 + x\right]_{0}^{2} = 10$, hitting the strict upper boundary) gets flagged immediately.
3. **Omission of Constant Terms or Limit Substitution Mistakes:**
   - Forgetting to integrate the $+1$ term (giving $\frac{8}{3} \approx 2.67$, close to the lower edge) or substituting the wrong upper limit (e.g., plugging in $x = 3$ instead of $x = 2$, yielding $\frac{27}{3} + 3 = 12 > 10$) produces an out-of-range result.
4. **Order-of-Magnitude / Decimal-Point Errors:**
   - Any arithmetic slip that shifts a decimal place (such as $0.467$ or $46.7$) falls outside $[2, 10]$ and is instantly exposed.

*(Note on limitation: While bounding guarantees detection of any error that pushes the result outside $[2, 10]$, a small internal arithmetic slip that leaves the value inside $(2, 10)$—such as obtaining $\frac{13}{3} \approx 4.33$—requires direct differentiation of the antiderivative $F'(x) = f(x)$ for complete verification.)*