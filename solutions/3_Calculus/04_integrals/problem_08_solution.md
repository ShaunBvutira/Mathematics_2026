### Problem 8. Choosing the Factors in Integration by Parts

#### Question

Compute

$$
\int x \cos x \, dx.
$$

Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

---

### Solution

#### Step 1. Justify the Choice of $u$ and $dv$

In the integration-by-parts formula $\int u \, dv = uv - \int v \, du$, we transfer a derivative from $dv$ onto $u$. Comparing the two possible assignments for $\int x \cos x \, dx$ shows why one simplifies the integral while the other complicates it:

1. **Recommended Choice ($u = x$ and $dv = \cos x \, dx$):**
   - **Differentiating $x$ lowers its polynomial degree:** $\frac{d}{dx}(x) = 1$, which eliminates the algebraic variable factor completely.
   - **Integrating $\cos x$ does not increase complexity:** $\int \cos x \, dx = \sin x$, which stays a simple elementary trigonometric function of the same complexity.
   - **Resulting new integral:** $\int v \, du = \int \sin x \cdot 1 \, dx = \int \sin x \, dx$, which can be evaluated immediately in one step.

2. **Opposite Choice ($u = \cos x$ and $dv = x \, dx$):**
   - **Differentiating $\cos x$ cycles without simplifying:** $\frac{d}{dx}(\cos x) = -\sin x$, which is just as complex as $\cos x$.
   - **Integrating $x$ raises its polynomial degree:** $\int x \, dx = \frac{1}{2}x^2$, turning a linear factor into a quadratic factor.
   - **Resulting new integral:** $\int v \, du = \int \frac{1}{2}x^2(-\sin x) \, dx = -\frac{1}{2}\int x^2 \sin x \, dx$, which is strictly **harder** than the original integral because the power of $x$ increased from $1$ to $2$.

*(This follows the standard **LIATE** priority heuristic—Logarithmic, Inverse trigonometric, Algebraic, Trigonometric, Exponential—where the **Algebraic** factor $x$ comes before the **Trigonometric** factor $\cos x$ as the choice for $u$.)*

---

#### Step 2. Set Up the Components for Integration by Parts

Using $u = x$ and $dv = \cos x \, dx$:

$$
\begin{aligned}
u &= x &\implies& du = 1 \, dx = dx \\
dv &= \cos x \, dx &\implies& v = \int \cos x \, dx = \sin x
\end{aligned}
$$

---

#### Step 3. Compute the Integral

Substitute $u$, $v$, $du$, and $dv$ into the integration-by-parts formula $\int u \, dv = uv - \int v \, du$:

$$
\begin{aligned}
\int x \cos x \, dx
&= x \cdot \sin x - \int \sin x \, dx \\
&= x \sin x - (-\cos x) + C \\
&= x \sin x + \cos x + C, \qquad C \in \mathbb{R}
\end{aligned}
$$

---

#### Step 4. Verify the Result by Differentiation

Differentiate $F(x) = x \sin x + \cos x + C$ with respect to $x$ using the Product Rule on $x \sin x$:

$$
\begin{aligned}
F'(x)
&= \frac{d}{dx}\bigl(x \sin x + \cos x + C\bigr) \\
&= \left[\frac{d}{dx}(x) \cdot \sin x + x \cdot \frac{d}{dx}(\sin x)\right] + \frac{d}{dx}(\cos x) + \frac{d}{dx}(C) \\
&= \bigl(1 \cdot \sin x + x \cdot \cos x\bigr) - \sin x + 0 \\
&= \sin x + x \cos x - \sin x \\
&= x \cos x
\end{aligned}
$$

Because $F'(x)$ reproduces the original integrand identically, the antiderivative is verified.