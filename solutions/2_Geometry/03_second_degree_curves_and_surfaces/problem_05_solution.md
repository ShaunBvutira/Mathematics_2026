### Exercise 5. Hyperbola and Asymptotes

For the equation

$$
\frac{x^2}{16} - \frac{y^2}{9} = 1
$$

find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

---

### Solution

#### Step 1. Find the intercepts with the coordinate axes

1. **$x$-intercepts (set $y = 0$):**

   $$
   \frac{x^2}{16} - \frac{0^2}{9} = 1 \implies \frac{x^2}{16} = 1 \implies x^2 = 16 \implies x = \pm 4
   $$

   The $x$-intercepts are the vertices at **$(4, 0)$** and **$(-4, 0)$**.

2. **$y$-intercepts (set $x = 0$):**

   $$
   \frac{0^2}{16} - \frac{y^2}{9} = 1 \implies -\frac{y^2}{9} = 1 \implies y^2 = -9
   $$

   Since $y^2 = -9$ has no real solutions, there are **no $y$-intercepts**. The hyperbola does not cross the vertical axis.

---

#### Step 2. Determine the semi-axes, foci, and asymptotes

1. **Semi-axes:**
   - Semi-transverse axis: $a = \sqrt{16} = 4$
   - Semi-conjugate axis: $b = \sqrt{9} = 3$

2. **Foci distance ($c$):**

   $$
   c = \sqrt{a^2 + b^2} = \sqrt{16 + 9} = \sqrt{25} = 5
   $$

   The foci are located at $F_1(-5, 0)$ and $F_2(5, 0)$.

3. **Asymptotes:**
   For a horizontal hyperbola $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$, the asymptotic lines pass through the origin with equations $y = \pm \frac{b}{a} x$.

   Substitute $a = 4$ and $b = 3$:

   $$
   y = \frac{3}{4}x \quad \text{and} \quad y = -\frac{3}{4}x
   $$

---

#### Step 3. Sketch / Visual Description

<Image src="image_agent_tag_14922563873613633285" alt="Diagram showing the geometric structure of a hyperbola with asymptotes and central rectangle" caption="Asymptotic behavior of a canonical hyperbola" />

- **Central Guide Box:** Draw a rectangle centered at $(0,0)$ with horizontal bounds at $x = \pm 4$ and vertical bounds at $y = \pm 3$.
- **Asymptote Lines:** Draw two diagonal dashed lines extending infinitely through opposite corners of the guide box, given by $y = \pm \frac{3}{4}x$.
- **Vertices:** Plot $(-4, 0)$ and $(4, 0)$ on the $x$-axis.
- **Hyperbola Branches:** Draw two separate smooth curves opening outward to the left and right. Each curve starts at its vertex and bends outward, approaching the dashed asymptote lines closely as $|x|$ increases.

---

#### Step 4. Explanation of asymptotic behavior far from the center

Isolate $y$ in the hyperbola equation $\frac{x^2}{16} - \frac{y^2}{9} = 1$:

$$
\frac{y^2}{9} = \frac{x^2}{16} - 1 \implies y^2 = \frac{9}{16}x^2 - 9 \implies y = \pm \sqrt{\frac{9}{16}x^2 - 9}
$$

Factor out $\frac{9}{16}x^2$ from under the square root:

$$
y = \pm \sqrt{\frac{9}{16}x^2 \left(1 - \frac{16}{x^2}\right)} = \pm \frac{3}{4} |x| \sqrt{1 - \frac{16}{x^2}}
$$

As $|x| \to \infty$ (far from the center):
- The term $\frac{16}{x^2} \to 0$.
- Consequently, $\sqrt{1 - \frac{16}{x^2}} \to \sqrt{1} = 1$.

Therefore, for very large values of $|x|$, the expression simplifies to:

$$
y \approx \pm \frac{3}{4} x
$$

The constant term $-1$ becomes negligible relative to the growing $x^2$ term as $x$ moves far from the origin, causing the hyperbola to become virtually indistinguishable from its asymptote lines $y = \pm \frac{3}{4}x$.