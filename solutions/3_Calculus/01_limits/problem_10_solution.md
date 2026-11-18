### Exercise 10. Continuity of a Piecewise Function

#### Question

Find $a$ so that

$$
f(x) = \begin{cases}
ax + 1, & x < 2, \\
x^2 - 1, & x \ge 2
\end{cases}
$$

is continuous at $x = 2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

---

### Solution

#### Step 1. State the definition of continuity at $x = 2$

A function $f(x)$ is continuous at $x = 2$ if and only if three conditions hold simultaneously:
1. $f(2)$ is defined,
2. $\lim_{x \to 2} f(x)$ exists (meaning the left-hand and right-hand limits exist and are equal), and
3. $\lim_{x \to 2} f(x) = f(2)$.

Compactly, we require:

$$
\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2)
$$

---

#### Step 2. Evaluate the function value $f(2)$

Since $x = 2$ satisfies the condition $x \ge 2$, use the second branch $f(x) = x^2 - 1$:

$$
f(2) = 2^2 - 1 = 4 - 1 = 3
$$

---

#### Step 3. Compute the left-hand limit ($x \to 2^-$)

For $x < 2$, $f(x)$ is given by the linear branch $ax + 1$:

$$
\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} (ax + 1) = a(2) + 1 = 2a + 1
$$

---

#### Step 4. Compute the right-hand limit ($x \to 2^+$)

For $x > 2$, $f(x)$ is given by the quadratic branch $x^2 - 1$:

$$
\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (x^2 - 1) = 2^2 - 1 = 4 - 1 = 3
$$

---

#### Step 5. Compare the three quantities and solve for $a$

Compare the results obtained in Steps 2, 3, and 4:
- **Left-hand limit:** $\lim_{x \to 2^-} f(x) = 2a + 1$
- **Right-hand limit:** $\lim_{x \to 2^+} f(x) = 3$
- **Function value:** $f(2) = 3$

Notice that the right-hand limit and the function value already match ($\lim_{x \to 2^+} f(x) = f(2) = 3$), which means $f$ is automatically right-continuous at $x = 2$. To make the two-sided limit exist and equal $f(2)$, set the left-hand limit equal to $3$:

$$
\begin{aligned}
2a + 1 &= 3 \\
2a &= 2 \\
a &= 1
\end{aligned}
$$

---

#### Step 6. Verification

With $a = 1$, the piecewise function becomes:

$$
f(x) = \begin{cases}
x + 1, & x < 2, \\
x^2 - 1, & x \ge 2
\end{cases}
$$

Checking all three values at $x = 2$:

$$
\lim_{x \to 2^-} f(x) = 2 + 1 = 3, \qquad \lim_{x \to 2^+} f(x) = 2^2 - 1 = 3, \qquad f(2) = 2^2 - 1 = 3
$$

Since $\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2) = 3$, the function is continuous at $x = 2$ when **$a = 1$**.