### Exercise 1. Dominant Terms in a Sequence

#### Question

Compute

$$
\lim_{n \to \infty} \frac{4n^2 - 3n + 1}{2n^2 + 5n - 7}.
$$

Explain why the highest-degree terms determine the result.

---

### Solution

#### Step 1. Factor out the highest power of $n$ ($n^2$)

Identify the highest-degree term in both the numerator and the denominator, which is $n^2$. Divide every term in the numerator and the denominator by $n^2$ (valid for $n \neq 0$):

$$
\begin{aligned}
\lim_{n \to \infty} \frac{4n^2 - 3n + 1}{2n^2 + 5n - 7}
&= \lim_{n \to \infty} \frac{\frac{4n^2}{n^2} - \frac{3n}{n^2} + \frac{1}{n^2}}{\frac{2n^2}{n^2} + \frac{5n}{n^2} - \frac{7}{n^2}} \\
&= \lim_{n \to \infty} \frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}
\end{aligned}
$$

---

#### Step 2. Apply limit laws as $n \to \infty$

Since $\lim_{n \to \infty} \frac{1}{n} = 0$ and $\lim_{n \to \infty} \frac{1}{n^2} = 0$, every fraction with $n$ in the denominator vanishes as $n$ grows without bound:

$$
\begin{aligned}
\lim_{n \to \infty} \frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}
&= \frac{4 - 3(0) + 0}{2 + 5(0) - 7(0)} \\
&= \frac{4}{2} = 2
\end{aligned}
$$

The limit of the sequence is **$2$**.

---

#### Step 3. Why the highest-degree terms determine the result

1. **Relative Growth Rates:** As $n$ becomes very large, $n^2$ grows vastly faster than lower-degree terms ($n$ and constants). For instance, when $n = 1{,}000$, $4n^2 = 4{,}000{,}000$, whereas $-3n + 1 = -2{,}999$ contributes less than $0.08\%$ of the numerator's value.
2. **Vanishing Lower-Order Ratios:** Factoring out the highest power $n^2$ rewrites the numerator as $n^2\left(4 - \frac{3}{n} + \frac{1}{n^2}\right)$ and the denominator as $n^2\left(2 + \frac{5}{n} - \frac{7}{n^2}\right)$. The common $n^2$ factors cancel, while all lower-degree terms become inverse powers of $n$ ($\frac{1}{n}, \frac{1}{n^2}$) that shrink to $0$ as $n \to \infty$.
3. **Asymptotic Equivalence:** Consequently, for large $n$, the sequence behaves asymptotically like the ratio of its leading terms:

   $$
   \frac{4n^2 - 3n + 1}{2n^2 + 5n - 7} \sim \frac{4n^2}{2n^2} = \frac{4}{2} = 2
   $$