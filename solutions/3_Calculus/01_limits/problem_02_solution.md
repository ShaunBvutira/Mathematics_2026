### Exercise 2. Different Growth Rates

#### Question

Compute

$$
\lim_{n \to \infty} \frac{3n + 1}{n^2 + 4}, \qquad \lim_{n \to \infty} \frac{2n^3 - n}{5n^2 + 1}.
$$

Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

---

### Solution

#### Part 1. First Limit: $\lim_{n \to \infty} \frac{3n + 1}{n^2 + 4}$

Divide every term in the numerator and the denominator by $n^2$, the highest power of $n$ in the denominator:

$$
\begin{aligned}
\lim_{n \to \infty} \frac{3n + 1}{n^2 + 4}
&= \lim_{n \to \infty} \frac{\frac{3n}{n^2} + \frac{1}{n^2}}{\frac{n^2}{n^2} + \frac{4}{n^2}} \\
&= \lim_{n \to \infty} \frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}}
\end{aligned}
$$

Since $\lim_{n \to \infty} \frac{1}{n} = 0$ and $\lim_{n \to \infty} \frac{1}{n^2} = 0$:

$$
\lim_{n \to \infty} \frac{\frac{3}{n} + \frac{1}{n^2}}{1 + \frac{4}{n^2}} = \frac{0 + 0}{1 + 0} = \frac{0}{1} = 0
$$

The first limit is **$0$**.

---

#### Part 2. Second Limit: $\lim_{n \to \infty} \frac{2n^3 - n}{5n^2 + 1}$

Divide every term in the numerator and the denominator by $n^2$, the highest power of $n$ in the denominator:

$$
\begin{aligned}
\lim_{n \to \infty} \frac{2n^3 - n}{5n^2 + 1}
&= \lim_{n \to \infty} \frac{\frac{2n^3}{n^2} - \frac{n}{n^2}}{\frac{5n^2}{n^2} + \frac{1}{n^2}} \\
&= \lim_{n \to \infty} \frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}}
\end{aligned}
$$

As $n \to \infty$:
- The numerator $2n - \frac{1}{n} \to +\infty$ because $2n \to +\infty$ while $\frac{1}{n} \to 0$.
- The denominator $5 + \frac{1}{n^2} \to 5 + 0 = 5 > 0$.

Therefore:

$$
\lim_{n \to \infty} \frac{2n - \frac{1}{n}}{5 + \frac{1}{n^2}} = +\infty
$$

The second limit diverges to **$+\infty$**.

---

#### Part 3. Comparison of the Two Cases

1. **In Case 1 ($\frac{3n + 1}{n^2 + 4}$):** The denominator has degree $2$, while the numerator has degree $1$. Because quadratic growth ($n^2$) outpaces linear growth ($3n$), the denominator grows vastly faster than the numerator, pulling the quotient down to $0$.
2. **In Case 2 ($\frac{2n^3 - n}{5n^2 + 1}$):** The numerator has degree $3$, while the denominator has degree $2$. Because cubic growth ($2n^3$) outpaces quadratic growth ($5n^2$), the numerator grows vastly faster than the denominator, driving the quotient to $+\infty$.

---

#### Part 4. General Observation for Rational Sequences

For a rational sequence $\frac{P(n)}{Q(n)}$ where $P(n) = a_p n^p + \dots + a_0$ (with $a_p \neq 0$) has degree $p$ and $Q(n) = b_q n^q + \dots + b_0$ (with $b_q \neq 0$) has degree $q$:

1. **Denominator degree is larger ($p < q$):**
   The denominator dominates, and the sequence converges to zero:

   $$
   \lim_{n \to \infty} \frac{P(n)}{Q(n)} = 0
   $$

2. **Numerator and denominator degrees are equal ($p = q$):**
   The leading powers cancel out, and the sequence converges to the ratio of the leading coefficients:

   $$
   \lim_{n \to \infty} \frac{P(n)}{Q(n)} = \frac{a_p}{b_q}
   $$

3. **Numerator degree is larger ($p > q$):**
   The numerator dominates, and the sequence diverges to $\pm\infty$ (with the sign matching the sign of $\frac{a_p}{b_q}$):

   $$
   \lim_{n \to \infty} \frac{P(n)}{Q(n)} = \begin{cases} +\infty & \text{if } \frac{a_p}{b_q} > 0, \\ -\infty & \text{if } \frac{a_p}{b_q} < 0. \end{cases}
   $$