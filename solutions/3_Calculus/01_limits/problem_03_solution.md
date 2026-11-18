### Exercise 3. A Square Root and Removing an Indeterminate Form

#### Question

Compute

$$
\lim_{n \to \infty} \left(\sqrt{n^2 + 5n} - n\right).
$$

Use the conjugate expression and explain why this transformation removes the difficulty.

---

### Solution

#### Step 1. Identify the indeterminate form

As $n \to \infty$, both $\sqrt{n^2 + 5n} \to +\infty$ and $n \to +\infty$. Consequently, the expression takes the indeterminate form $\infty - \infty$, which cannot be evaluated directly by subtracting limits.

---

#### Step 2. Multiply and divide by the conjugate expression

Multiply $\left(\sqrt{n^2 + 5n} - n\right)$ by $\frac{\sqrt{n^2 + 5n} + n}{\sqrt{n^2 + 5n} + n} = 1$ (valid for all $n \ge 1$, where the denominator is strictly positive):

$$
\begin{aligned}
\lim_{n \to \infty} \left(\sqrt{n^2 + 5n} - n\right)
&= \lim_{n \to \infty} \frac{\left(\sqrt{n^2 + 5n} - n\right)\left(\sqrt{n^2 + 5n} + n\right)}{\sqrt{n^2 + 5n} + n}
\end{aligned}
$$

Apply the difference of squares identity $(A - B)(A + B) = A^2 - B^2$ to the numerator:

$$
\begin{aligned}
\lim_{n \to \infty} \frac{\left(\sqrt{n^2 + 5n}\right)^2 - n^2}{\sqrt{n^2 + 5n} + n}
&= \lim_{n \to \infty} \frac{(n^2 + 5n) - n^2}{\sqrt{n^2 + 5n} + n} \\
&= \lim_{n \to \infty} \frac{5n}{\sqrt{n^2 + 5n} + n}
\end{aligned}
$$

---

#### Step 3. Factor out the dominant power $n$ and evaluate the limit

For $n > 0$, factor $n^2$ out from inside the square root ($\sqrt{n^2} = n$):

$$
\sqrt{n^2 + 5n} = \sqrt{n^2\left(1 + \frac{5}{n}\right)} = n\sqrt{1 + \frac{5}{n}}
$$

Substitute this back into the denominator and divide numerator and denominator by $n$:

$$
\begin{aligned}
\lim_{n \to \infty} \frac{5n}{n\sqrt{1 + \frac{5}{n}} + n}
&= \lim_{n \to \infty} \frac{5n}{n\left(\sqrt{1 + \frac{5}{n}} + 1\right)} \\
&= \lim_{n \to \infty} \frac{5}{\sqrt{1 + \frac{5}{n}} + 1}
\end{aligned}
$$

Since $\lim_{n \to \infty} \frac{5}{n} = 0$:

$$
\lim_{n \to \infty} \frac{5}{\sqrt{1 + \frac{5}{n}} + 1} = \frac{5}{\sqrt{1 + 0} + 1} = \frac{5}{1 + 1} = \frac{5}{2}
$$

The limit of the sequence is **$\frac{5}{2}$**.

---

#### Step 4. Explanation of why the conjugate transformation removes the difficulty

1. **Cancels the Leading Growing Terms:** Initially, $\sqrt{n^2 + 5n}$ grows at roughly the same rate as $n$, creating a subtle difference between two diverging quantities ($\infty - \infty$). Applying $(A - B)(A + B) = A^2 - B^2$ squares the radical, turning $\sqrt{n^2 + 5n}$ into $n^2 + 5n$ so that the dominant $n^2$ terms cancel out algebraically ($n^2 - n^2 = 0$), leaving only the lower-order term $5n$ in the numerator.
2. **Converts Subtraction into Addition in the Denominator:** Moving the conjugate to the denominator replaces the unstable subtraction $\sqrt{n^2 + 5n} - n$ with a sum of two positive terms $\sqrt{n^2 + 5n} + n$. A sum of positive terms growing to $+\infty$ has no cancellation and behaves predictably like $n + n = 2n$.
3. **Reveals Balanced Degrees:** Once rewritten as $\frac{5n}{\sqrt{n^2 + 5n} + n}$, both the numerator ($5n$) and the denominator ($\approx 2n$) grow linearly at rate $n^1$, allowing the common factor $n$ to cancel cleanly and yield the finite ratio $\frac{5}{2}$.