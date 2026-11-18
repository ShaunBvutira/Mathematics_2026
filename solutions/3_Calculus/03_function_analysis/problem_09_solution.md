### Problem 9. An Oblique Asymptote

#### Question

Analyze the asymptotes of

$$f(x) = \frac{x^2 + 1}{x - 1}.$$

Perform polynomial division and explain why the remainder term vanishes for large $\vert{}x\vert{}$.

---

### Solution

#### Step 1. Domain and Vertical Asymptote

Since $f(x) = \frac{x^2 + 1}{x - 1}$ is a rational function, it is defined for all real numbers $x \in \mathbb{R}$ except where the denominator equals zero:

$$x - 1 = 0 \implies x = 1 \implies D_f = (-\infty, 1) \cup (1, +\infty)$$

Check the one-sided limits as $x$ approaches the excluded value $x = 1$:
- **As $x \to 1^-$:** The numerator $x^2 + 1 \to 2 > 0$, while the denominator $x - 1 \to 0^-$, so:

  $$\lim_{x \to 1^-} \frac{x^2 + 1}{x - 1} = -\infty$$

- **As $x \to 1^+$:** The numerator $x^2 + 1 \to 2 > 0$, while the denominator $x - 1 \to 0^+$, so:

  $$\lim_{x \to 1^+} \frac{x^2 + 1}{x - 1} = +\infty$$

Therefore, the vertical line **$x = 1$** is a **vertical asymptote**.

---

#### Step 2. Check for a Horizontal Asymptote

Because the degree of the numerator ($\deg(x^2 + 1) = 2$) is greater than the degree of the denominator ($\deg(x - 1) = 1$), the function grows without bound as $x \to \pm\infty$:

$$\lim_{x \to +\infty} \frac{x^2 + 1}{x - 1} = +\infty, \qquad \lim_{x \to -\infty} \frac{x^2 + 1}{x - 1} = -\infty$$

Since neither limit at infinity is finite, $f(x)$ has **no horizontal asymptote**. However, because $\deg(\text{numerator}) - \deg(\text{denominator}) = 2 - 1 = 1$, $f(x)$ approaches a straight slanted line—an **oblique (slant) asymptote**.

---

#### Step 3. Perform Polynomial Division

Divide $x^2 + 1$ by $x - 1$ using polynomial long division (or algebraic splitting):

```text
          x + 1
        _____________
x - 1 ) x^2 + 0x + 1
      -(x^2 -  x)
      -----------
               x + 1
             -(x - 1)
             --------
                   2