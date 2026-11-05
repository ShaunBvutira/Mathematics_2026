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
  Divide both sides by $36$:

  $$
  \frac{4x^2}{36} + \frac{9y^2}{36} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
  $$

- **Classification:** **Ellipse** (centered at the origin).
- **Key Features:**
  - Horizontal semi-axis $a = \sqrt{9} = 3$
  - Vertical semi-axis $b = \sqrt{4} = 2$
  - Both $x^2$ and $y^2$ terms have positive coefficients with $a \neq b$.

---

#### 2. Equation: $x^2 - y^2 = 1$

- **Canonical Form:**
  Matches $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ directly with $a = 1$ and $b = 1$:

  $$
  \frac{x^2}{1^2} - \frac{y^2}{1^2} = 1
  $$

- **Classification:** **Equilateral (Rectangular) Hyperbola** (centered at the origin).
- **Key Features:**
  - Vertices at $(\pm 1, 0)$ along the $x$-axis.
  - Asymptotes are perpendicular lines $y = \pm x$.
  - The minus sign between $x^2$ and $y^2$ identifies it as a hyperbola.

---

#### 3. Equation: $x^2 - 4y = 0$

- **Reduction to Canonical Form:**
  Isolate $x^2$:

  $$
  x^2 = 4y
  $$

- **Classification:** **Parabola** (opening upward).
- **Key Features:**
  - Vertex at $(0, 0)$.
  - Symmetric with respect to the vertical $y$-axis ($x = 0$).
  - Focal parameter $p = 1$ (since $4p = 4 \implies p = 1$), with focus at $(0, 1)$ and directrix $y = -1$.
  - Only one variable ($x$) is squared, while the other ($y$) is linear.

---

#### 4. Equation: $x^2 + y^2 + 1 = 0$

- **Reduction:**
  Subtract $1$ from both sides:

  $$
  x^2 + y^2 = -1
  $$

- **Classification:** **Empty Set / Degenerate Conic** (No real points).

- **Explanation of why there are no real points:**
  1. **Non-negativity of Real Squares:** For any real numbers $x, y \in \mathbb{R}$, their squares are non-negative: $x^2 \ge 0$ and $y^2 \ge 0$.
  2. **Sum of Non-negative Quantities:** Adding two non-negative terms yields a non-negative result:

     $$
     x^2 + y^2 \ge 0 \quad \text{for all } x, y \in \mathbb{R}
     $$

  3. **Contradiction:** The equation demands that $x^2 + y^2 = -1$. Because a non-negative real sum can never equal a strictly negative number ($-1$), no real pair $(x, y)$ can satisfy the equation. 
  
  *(Geometrically, this represents an imaginary circle with radius $R = \sqrt{-1} = i$, containing no points in the real Cartesian plane $\mathbb{R}^2$.)*