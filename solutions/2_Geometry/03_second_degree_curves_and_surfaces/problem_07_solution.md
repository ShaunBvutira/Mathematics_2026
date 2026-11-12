### Exercise 7. Classifying a Second-Degree Equation

Determine the type of object described by:

1. $4x^2 + 9y^2 = 36$
2. $x^2 - y^2 = 1$
3. $x^2 - 4y = 0$
4. $x^2 + y^2 + 1 = 0$

In the last case, explain why there are no real points.

---

### Solution

#### 1. Equation: $4x^2 + 9y^2 = 36$

- **Reduction to Canonical Form:**
  Divide both sides of the equation by $36$:

  $$
  \frac{4x^2}{36} + \frac{9y^2}{36} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
  $$

- **Classification:** **Ellipse** (centered at the origin).
- **Key Features:**
  - Both $x^2$ and $y^2$ appear with positive coefficients and unequal denominators ($9 \neq 4$).
  - Horizontal semi-major axis: $a = \sqrt{9} = 3$ (vertices at $(\pm 3, 0)$).
  - Vertical semi-minor axis: $b = \sqrt{4} = 2$ (co-vertices at $(0, \pm 2)$).

---

#### 2. Equation: $x^2 - y^2 = 1$

- **Canonical Form:**
  Matches the standard form $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ directly with $a = 1$ and $b = 1$:

  $$
  \frac{x^2}{1^2} - \frac{y^2}{1^2} = 1
  $$

- **Classification:** **Equilateral (Rectangular) Hyperbola** (centered at the origin).
- **Key Features:**
  - Both $x^2$ and $y^2$ appear with opposite signs ($+$ for $x^2$, $-$ for $y^2$).
  - Transverse axis lies along the $x$-axis with vertices at $(\pm 1, 0)$.
  - Asymptotes are the perpendicular lines $y = x$ and $y = -x$.

---

#### 3. Equation: $x^2 - 4y = 0$

- **Reduction to Canonical Form:**
  Isolate the squared variable $x^2$:

  $$
  x^2 = 4y
  $$

- **Classification:** **Parabola** (opening upward).
- **Key Features:**
  - Only one variable ($x$) is squared while the other ($y$) is linear, matching $x^2 = 4py$ with $4p = 4 \implies p = 1 > 0$.
  - Vertex at $(0, 0)$, symmetric across the vertical $y$-axis ($x = 0$).
  - Focus at $(0, 1)$ and directrix line $y = -1$.

---

#### 4. Equation: $x^2 + y^2 + 1 = 0$

- **Reduction:**
  Move the constant term to the right-hand side:

  $$
  x^2 + y^2 = -1
  $$

- **Classification:** **Empty real locus** (also referred to as an **imaginary circle**, since it defines no points in $\mathbb{R}^2$).

- **Explanation of why there are no real points:**
  1. **Non-negativity of Squares:** For every real number $x \in \mathbb{R}$ and $y \in \mathbb{R}$, squaring produces a non-negative value:
     
     $$
     x^2 \ge 0 \quad \text{and} \quad y^2 \ge 0
     $$

  2. **Lower Bound on the Sum:** The sum of two non-negative real numbers is always greater than or equal to zero:

     $$
     x^2 + y^2 \ge 0 \quad \text{for all } (x, y) \in \mathbb{R}^2
     $$

  3. **Contradiction:** Because the left-hand side satisfies $x^2 + y^2 \ge 0$ while the right-hand side is strictly negative ($-1 < 0$), the equality $x^2 + y^2 = -1$ cannot hold for any pair of real coordinates $(x, y)$. Consequently, the solution set in the real plane is empty.