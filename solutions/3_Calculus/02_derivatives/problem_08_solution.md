### Problem 8. Two Exponential Functions

#### Question

For

$$
f(x) = e^{2x - 3} + 5^x
$$

compute the derivative. Explain why the factor $2$ appears in the first term and why $\ln 5$ appears in the second.

---

### Solution

#### Step 1. Differentiate $f(x)$ term by term

Apply the sum rule $\frac{d}{dx}\left(e^{2x - 3} + 5^x\right) = \frac{d}{dx}\left(e^{2x - 3}\right) + \frac{d}{dx}\left(5^x\right)$:

1. **First term ($e^{2x - 3}$) via the Chain Rule:**
   Set the outer function as $g(u) = e^u$ (so $g'(u) = e^u$) and the inner exponent as $u(x) = 2x - 3$ (so $u'(x) = 2$):

   $$
   \frac{d}{dx}\left(e^{2x - 3}\right) = e^{2x - 3} \cdot \frac{d}{dx}(2x - 3) = e^{2x - 3} \cdot 2 = 2e^{2x - 3}
   $$

2. **Second term ($5^x$) via the General Exponential Rule:**
   Using $\frac{d}{dx}(a^x) = a^x \ln a$ with base $a = 5$:

   $$
   \frac{d}{dx}\left(5^x\right) = 5^x \ln 5
   $$

---

#### Step 2. Combine the derivatives

Adding the two results gives:

$$
f'(x) = 2e^{2x - 3} + 5^x \ln 5
$$

---

#### Step 3. Explain why the factor $2$ appears in the first term

1. **Chain Rule from the Linear Exponent:**
   The natural exponential function $e^u$ is its own derivative only when differentiated with respect to its exponent $u$ ($\frac{d}{du}(e^u) = e^u$). Here, the exponent is not $x$, but the inner linear function $u(x) = 2x - 3$.
2. **Rate Scaling:**
   Because $u(x) = 2x - 3$ increases twice as fast as $x$ ($\frac{du}{dx} = 2$), the Chain Rule multiplies the outer derivative $e^{2x - 3}$ by the inner derivative $2$:

   $$
   \frac{d}{dx}\left(e^{2x - 3}\right) = \frac{d}{du}(e^u) \cdot \frac{du}{dx} = e^{2x - 3} \cdot 2 = 2e^{2x - 3}
   $$

   *(Equivalently, rewriting $e^{2x - 3} = e^{-3}(e^2)^x$ shows that the effective growth base is $e^2$, whose natural logarithm is $\ln(e^2) = 2$.)*

---

#### Step 4. Explain why the factor $\ln 5$ appears in the second term

1. **Rewriting Base $5$ in Natural Base $e$:**
   Using the inverse identity $5 = e^{\ln 5}$, the function $5^x$ can be expressed as a natural exponential with a scaled exponent:

   $$
   5^x = \left(e^{\ln 5}\right)^x = e^{(\ln 5)x}
   $$

2. **Applying the Chain Rule to $e^{(\ln 5)x}$:**
   Now $5^x$ has the outer function $e^u$ and the inner linear function $u(x) = (\ln 5)x$, whose derivative is the constant $\ln 5$. Applying the Chain Rule yields:

   $$
   \frac{d}{dx}\left(5^x\right) = \frac{d}{dx}\left(e^{(\ln 5)x}\right) = e^{(\ln 5)x} \cdot \ln 5 = 5^x \ln 5
   $$

3. **Geometric Meaning:**
   Only base $e \approx 2.718$ has a slope at $x = 0$ equal to $1$. Because $5 > e$, the curve $y = 5^x$ grows steeper than $y = e^x$—its slope at $x = 0$ is $\ln 5 \approx 1.609$, which scales the derivative at every point $x$.