### Exercise 8. A Square Root in a Function Limit

#### Question

Compute

$$
\lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4}
$$

by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

---

### Solution

#### Step 1. Check direct substitution (identify the indeterminate form)

Substitute $x = 4$ into the numerator and denominator separately:
- **Numerator:** $\sqrt{4} - 2 = 2 - 2 = 0$
- **Denominator:** $4 - 4 = 0$

Because both approach $0$, the expression yields the indeterminate form $\frac{0}{0}$ and cannot be evaluated by direct substitution.

---

#### Step 2. Rationalize the numerator using the conjugate

Multiply both the numerator and the denominator by the conjugate of the numerator, $\sqrt{x} + 2$ (which is strictly positive near $x = 4$):

$$
\begin{aligned}
\lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4}
&= \lim_{x \to 4} \frac{(\sqrt{x} - 2)(\sqrt{x} + 2)}{(x - 4)(\sqrt{x} + 2)}
\end{aligned}
$$

Apply the difference of squares identity $(A - B)(A + B) = A^2 - B^2$ to the numerator:

$$
\begin{aligned}
\lim_{x \to 4} \frac{(\sqrt{x})^2 - 2^2}{(x - 4)(\sqrt{x} + 2)}
&= \lim_{x \to 4} \frac{x - 4}{(x - 4)(\sqrt{x} + 2)}
\end{aligned}
$$

---

#### Step 3. Cancel the common factor and evaluate the limit

Since $x \to 4$ means $x \neq 4$, the factor $(x - 4)$ is non-zero and cancels cleanly from the numerator and denominator:

$$
\begin{aligned}
\lim_{x \to 4} \frac{x - 4}{(x - 4)(\sqrt{x} + 2)}
&= \lim_{x \to 4} \frac{1}{\sqrt{x} + 2}
\end{aligned}
$$

Now apply direct substitution at $x = 4$:

$$
\lim_{x \to 4} \frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{2 + 2} = \frac{1}{4}
$$

The limit of the function is **$\frac{1}{4}$**.

*(Note: Alternatively, factoring the denominator as a difference of squares $x - 4 = (\sqrt{x} - 2)(\sqrt{x} + 2)$ immediately reveals the same cancellation.)*

---

#### Step 4. Comparison with Exercise 3 (Sequence Limit)

In Exercise 3, we evaluated $\lim_{n \to \infty} (\sqrt{n^2 + 5n} - n) = \frac{5}{2}$ by multiplying and dividing by $\sqrt{n^2 + 5n} + n$. Comparing both problems highlights how the same algebraic tool resolves two different types of indeterminate forms:

1. **Shared Algebraic Mechanism (Difference of Squares):**
   In both exercises, a difference involving a square root ($A - B$) traps the essential behavior inside a radical. Multiplying by the conjugate ($A + B$) uses $(A - B)(A + B) = A^2 - B^2$ to eliminate the square root from the numerator and replace the subtraction with an addition ($A + B$) in the denominator, where no cancellation can occur.
2. **Different Indeterminate Forms Resolved:**
   - **Exercise 3 ($\infty - \infty$ as $n \to \infty$):** Both terms grew toward $+\infty$ at the same linear rate. Rationalizing canceled the leading $n^2$ terms ($n^2 + 5n - n^2 = 5n$), exposing the surviving lower-order rate.
   - **Exercise 8 ($\frac{0}{0}$ as $x \to 4$):** Both numerator and denominator approached $0$ simultaneously. Rationalizing converted $\sqrt{x} - 2$ into $x - 4$, exposing the hidden zero-causing factor $(x - 4)$ so it could be canceled with the denominator.
3. **Domain Behavior ($n \to \infty$ vs. $x \to 4$):**
   Exercise 3 examined global asymptotic behavior across discrete integers $n \to \infty$, whereas Exercise 8 examines local behavior near a finite point $x = 4$ (in fact, $\lim_{x \to 4} \frac{\sqrt{x} - \sqrt{4}}{x - 4} = \frac{1}{4}$ is precisely the derivative $f'(4)$ of $f(x) = \sqrt{x}$).