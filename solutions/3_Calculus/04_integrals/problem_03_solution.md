### Problem 3. Recognizing Basic Antiderivatives

#### Question

Compute

$$
\int (2e^x + 3\cos x - 4\sin x) \, dx.
$$

Match each term with a known derivative and verify the entire result with one differentiation.

---

### Solution

#### Step 1. Apply Linearity of Integration

Since all three terms are continuous on $\mathbb{R} = (-\infty, +\infty)$, split the integral into separate terms using the sum/difference rule and the constant multiple rule:

$$
\int (2e^x + 3\cos x - 4\sin x) \, dx = 2\int e^x \, dx + 3\int \cos x \, dx - 4\int \sin x \, dx
$$

---

#### Step 2. Match Each Term with a Known Derivative

Recall the elementary derivative formulas and reverse each one to obtain the corresponding basic antiderivative:

| Integrand Term | Known Derivative Formula | Basic Antiderivative |
| :--- | :--- | :--- |
| $e^x$ | $\frac{d}{dx}(e^x) = e^x$ | $\int e^x \, dx = e^x + C_1$ |
| $\cos x$ | $\frac{d}{dx}(\sin x) = \cos x$ | $\int \cos x \, dx = \sin x + C_2$ |
| $\sin x$ | $\frac{d}{dx}(-\cos x) = -(-\sin x) = \sin x$ | $\int \sin x \, dx = -\cos x + C_3$ |

*(Pay special attention to the sign on the third term: because $\frac{d}{dx}(\cos x) = -\sin x$, reversing the derivative of $\sin x$ introduces a negative sign, giving $-\cos x$.)*

---

#### Step 3. Combine the Antiderivatives

Substitute the three basic antiderivatives back into the linear combination and combine all arbitrary constants into a single constant $C \in \mathbb{R}$:

$$
\begin{aligned}
\int (2e^x + 3\cos x - 4\sin x) \, dx
&= 2(e^x) + 3(\sin x) - 4(-\cos x) + C \\
&= 2e^x + 3\sin x + 4\cos x + C, \qquad C \in \mathbb{R}
\end{aligned}
$$

---

#### Step 4. Verify the Entire Result with One Differentiation

Differentiate $F(x) = 2e^x + 3\sin x + 4\cos x + C$ with respect to $x$ in a single pass:

$$
\begin{aligned}
F'(x)
&= \frac{d}{dx}\bigl(2e^x + 3\sin x + 4\cos x + C\bigr) \\
&= 2\frac{d}{dx}(e^x) + 3\frac{d}{dx}(\sin x) + 4\frac{d}{dx}(\cos x) + \frac{d}{dx}(C) \\
&= 2e^x + 3\cos x + 4(-\sin x) + 0 \\
&= 2e^x + 3\cos x - 4\sin x
\end{aligned}
$$

Since $F'(x)$ matches the original integrand term for term, the antiderivative is verified.