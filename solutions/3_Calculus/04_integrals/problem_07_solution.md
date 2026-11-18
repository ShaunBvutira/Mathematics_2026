### Problem 7. Integration by Parts as Reversing the Product Rule

#### Question

Compute

$$
\int x e^x \, dx.
$$

First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

---

### Solution

#### Step 1. Product Differentiation Rule and Meaning of Integration by Parts

1. **Product Differentiation Rule:**
   For two differentiable functions $u(x)$ and $v(x)$, the derivative of their product $u(x)v(x)$ is:

   $$
   \frac{d}{dx}\bigl[u(x)v(x)\bigr] = u'(x)v(x) + u(x)v'(x)
   $$

   *(In differential notation: $d(uv) = v \, du + u \, dv$.)*

2. **Deriving and Explaining the Integration-by-Parts Formula:**
   Integrate both sides of the product rule with respect to $x$:

   $$
   \int \frac{d}{dx}\bigl[u(x)v(x)\bigr] \, dx = \int u'(x)v(x) \, dx + \int u(x)v'(x) \, dx
   $$

   Since integration undoes differentiation on the left-hand side, we obtain:

   $$
   u(x)v(x) = \int v(x)u'(x) \, dx + \int u(x)v'(x) \, dx
   $$

   Rearranging to isolate $\int u(x)v'(x) \, dx$ gives the **Integration-by-Parts Formula**:

   $$
   \int u(x)v'(x) \, dx = u(x)v(x) - \int v(x)u'(x) \, dx
   $$

   *(Or in shorthand differential form: $\int u \, dv = uv - \int v \, du$.)*

   **Meaning:** Integration by parts transfers the derivative from one factor ($v' \to v$) onto the other factor ($u \to u'$). When an integrand is a product of two functions and $u$-substitution does not apply (because neither factor is the derivative of an inner function of the other), we choose $u$ so that differentiating it ($u'$) simplifies the expression, and choose $dv = v'(x) \, dx$ so that integrating it ($v$) does not make the expression harder.

---

#### Step 2. Choose $u$ and $dv$ for $\int x e^x \, dx$

Examine the two factors in the integrand $x \cdot e^x$:
- If we differentiate $x$, it simplifies to the constant $1$.
- If we integrate $e^x$, it stays $e^x$ without growing more complicated.

Therefore, make the following choices:

$$
\begin{aligned}
u &= x &\implies& du = 1 \, dx = dx \\
dv &= e^x \, dx &\implies& v = \int e^x \, dx = e^x
\end{aligned}
$$

---

#### Step 3. Compute the Integral

Substitute $u = x$, $v = e^x$, $du = dx$, and $dv = e^x \, dx$ into $\int u \, dv = uv - \int v \, du$:

$$
\begin{aligned}
\int x e^x \, dx
&= x \cdot e^x - \int e^x \, dx \\
&= x e^x - e^x + C \\
&= (x - 1)e^x + C, \qquad C \in \mathbb{R}
\end{aligned}
$$

---

#### Step 4. Verify the Result by Differentiation

Differentiate $F(x) = x e^x - e^x + C$ with respect to $x$ using the Product Rule on the first term $x e^x$:

$$
\begin{aligned}
F'(x)
&= \frac{d}{dx}\bigl(x e^x - e^x + C\bigr) \\
&= \left[\frac{d}{dx}(x) \cdot e^x + x \cdot \frac{d}{dx}(e^x)\right] - \frac{d}{dx}(e^x) + \frac{d}{dx}(C) \\
&= \bigl(1 \cdot e^x + x \cdot e^x\bigr) - e^x + 0 \\
&= e^x + x e^x - e^x \\
&= x e^x
\end{aligned}
$$

Because $F'(x)$ matches the original integrand identically, the antiderivative is verified.