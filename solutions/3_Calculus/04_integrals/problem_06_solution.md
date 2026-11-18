### Problem 6. When Does a Logarithm Appear from an Integral?

#### Question

Compute

$$
\int \frac{2x}{x^2 + 5} \, dx.
$$

Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

---

### Solution

#### Step 1. Identify the Denominator as a Candidate for Substitution

Examine the integrand $\frac{2x}{x^2 + 5}$. It is a rational function whose denominator is a quadratic expression:

$$
u(x) = x^2 + 5
$$

Because $x^2 + 5 \ge 5 > 0$ for all real numbers $x \in \mathbb{R}$, the denominator never vanishes, making the integrand continuous and defined everywhere on $(-\infty, +\infty)$.

---

#### Step 2. Compare the Numerator with the Derivative of the Denominator

Differentiate the chosen substitution $u = x^2 + 5$ with respect to $x$:

$$
\frac{du}{dx} = \frac{d}{dx}(x^2 + 5) = 2x \implies du = 2x \, dx
$$

**Comparison:**
- The **numerator** of the integrand is $2x$.
- The **derivative of the denominator** is $u'(x) = 2x$.
- They match **exactly** (not merely up to a constant factor, but with a $1:1$ ratio). Thus, the integral has the exact structural form:

  $$
  \int \frac{u'(x)}{u(x)} \, dx
  $$

---

#### Step 3. Compute the Integral via Substitution

Substitute $u = x^2 + 5$ and $du = 2x \, dx$ into the integral:

$$
\begin{aligned}
\int \frac{2x}{x^2 + 5} \, dx
&= \int \frac{1}{u} \, du \\
&= \ln|u| + C \\
&= \ln|x^2 + 5| + C
\end{aligned}
$$

Since $x^2 + 5 > 0$ for all real numbers $x$, the absolute value bars are redundant ($|x^2 + 5| = x^2 + 5$), giving the final simplified antiderivative:

$$
\int \frac{2x}{x^2 + 5} \, dx = \ln(x^2 + 5) + C, \qquad C \in \mathbb{R}
$$

---

#### Step 4. Explain the Source of the Logarithm in the Result

1. **Failure of the Power Rule for $n = -1$:**
   For any power $u^n$ with $n \neq -1$, integration raises the exponent by $1$ via $\int u^n \, du = \frac{u^{n+1}}{n+1} + C$. When $n = -1$ (i.e., $\frac{1}{u} = u^{-1}$), that formula would divide by $-1 + 1 = 0$, so no power function can differentiate to $u^{-1}$.
2. **Inverting the Chain Rule Derivative of $\ln|u(x)|$:**
   By the Chain Rule, differentiating the natural logarithm of a positive differentiable function $u(x)$ produces:

   $$
   \frac{d}{dx}\bigl[\ln\bigl(u(x)\bigr)\bigr] = \frac{1}{u(x)} \cdot u'(x) = \frac{u'(x)}{u(x)}
   $$

   Integration reverses differentiation. Whenever an integrand consists of a **derivative in the numerator** divided by the **original function in the denominator** ($\frac{u'(x)}{u(x)}$), reversing the Chain Rule immediately yields $\ln|u(x)| + C$.
3. **Verification by Differentiation:**
   Differentiating our answer confirms how the numerator $2x$ is recovered:

   $$
   \frac{d}{dx}\bigl[\ln(x^2 + 5) + C\bigr] = \frac{1}{x^2 + 5} \cdot \frac{d}{dx}(x^2 + 5) = \frac{2x}{x^2 + 5}
   $$