### Exercise 1. Recognizing Curves from Canonical Form

Recognize the curves:

1. $x^2 + y^2 = 9$
2. $\frac{x^2}{16} + \frac{y^2}{9} = 1$
3. $y^2 = 8x$
4. $\frac{x^2}{9} - \frac{y^2}{4} = 1$

For each curve, identify its most important features and describe its geometric shape. Explain which parts of the equation let you recognize the type of curve.

---

### Overview of Conic Section Canonical Forms

<Image src="image_agent_tag_17670900378636376908" alt="Mathematical diagram displaying standard conic sections including circle, ellipse, parabola, and hyperbola with their canonical equations" caption="Standard Conic Sections and Canonical Forms" />

---

### Solution

#### 1. Curve: $x^2 + y^2 = 9$

- **Type of Curve:** **Circle** (centered at the origin).

- **Recognition Key:**
  - Both variables $x$ and $y$ are squared ($x^2, y^2$).
  - The coefficients of $x^2$ and $y^2$ are **equal** and have the **same sign** (both $+1$).
  - Matches the standard form $x^2 + y^2 = R^2$.

- **Key Features:**
  - **Center:** $(0, 0)$
  - **Radius:** $R = \sqrt{9} = 3$
  - **Intercepts:** $(3, 0)$, $(-3, 0)$, $(0, 3)$, and $(0, -3)$

- **Sketch / Visual Description:**
  - Draw a perfectly symmetrical round loop centered at $(0,0)$.
  - Mark key points on the axes at $x = \pm 3$ and $y = \pm 3$.

---

#### 2. Curve: $\frac{x^2}{16} + \frac{y^2}{9} = 1$

- **Type of Curve:** **Horizontal Ellipse** (centered at the origin).

- **Recognition Key:**
  - Both $x^2$ and $y^2$ are present with a **plus sign** ($+$) between them.
  - The denominators are **positive and unequal** ($a^2 \neq b^2$), meaning the curve is stretched unevenly along the coordinate axes.
  - Matches the standard form $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$.

- **Key Features:**
  - **Center:** $(0, 0)$
  - **Semi-major axis ($a$):** $a = \sqrt{16} = 4$ along the $x$-axis.
  - **Semi-minor axis ($b$):** $b = \sqrt{9} = 3$ along the $y$-axis.
  - **Vertices (Major axis):** $(\pm 4, 0)$
  - **Co-vertices (Minor axis):** $(0, \pm 3)$
  - **Focal Distance ($c$):** $c = \sqrt{a^2 - b^2} = \sqrt{16 - 9} = \sqrt{7} \approx 2.65$
  - **Foci:** $(\pm\sqrt{7}, 0)$

- **Sketch / Visual Description:**
  - Draw an oval flattened vertically, wider along the horizontal axis ($x$-axis) than it is tall along the vertical axis ($y$-axis).
  - Pass the curve through $(-4,0)$, $(4,0)$, $(0,-3)$, and $(0,3)$.

---

#### 3. Curve: $y^2 = 8x$

- **Type of Curve:** **Parabola** (opening to the right).

- **Recognition Key:**
  - **Only one variable is squared** ($y^2$), while the other variable ($x$) is linear (first degree).
  - Matches the standard form $y^2 = 4px$ with $4p = 8 > 0$.

- **Key Features:**
  - **Vertex:** $(0, 0)$
  - **Axis of Symmetry:** The $x$-axis ($y = 0$).
  - **Focal Parameter ($p$):** $4p = 8 \implies p = 2$
  - **Focus:** $(p, 0) = (2, 0)$
  - **Directrix Line:** $x = -p \implies x = -2$
  - **Opening Direction:** Rightward (since $p > 0$).

- **Sketch / Visual Description:**
  - Place the vertex at the origin $(0,0)$.
  - Draw a smooth U-shaped curve opening to the right around the positive $x$-axis.
  - Pass the curve through reference points $(2, 4)$ and $(2, -4)$ (since $y^2 = 8(2) = 16 \implies y = \pm 4$).

---

#### 4. Curve: $\frac{x^2}{9} - \frac{y^2}{4} = 1$

- **Type of Curve:** **Horizontal Hyperbola** (centered at the origin).

- **Recognition Key:**
  - Both $x^2$ and $y^2$ are present, but separated by a **minus sign** ($-$); one term is positive and the other is negative.
  - The positive term ($\frac{x^2}{9}$) indicates the transverse axis lies along the $x$-axis.
  - Matches the standard form $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$.

- **Key Features:**
  - **Center:** $(0, 0)$
  - **Semi-transverse axis ($a$):** $a = \sqrt{9} = 3$ (distance to vertices along $x$-axis).
  - **Semi-conjugate axis ($b$):** $b = \sqrt{4} = 2$.
  - **Vertices:** $(\pm 3, 0)$
  - **Focal Distance ($c$):** $c = \sqrt{a^2 + b^2} = \sqrt{9 + 4} = \sqrt{13} \approx 3.61$
  - **Foci:** $(\pm\sqrt{13}, 0)$
  - **Asymptotes:** $y = \pm \frac{b}{a} x = \pm \frac{2}{3} x$

- **Sketch / Visual Description:**
  - Draw a central rectangle bounded by $x = \pm 3$ and $y = \pm 2$.
  - Extend diagonal dashed lines through opposite corners of the rectangle to form the asymptotes $y = \pm \frac{2}{3}x$.
  - Draw two separate smooth curves opening left and right starting from vertices $(-3, 0)$ and $(3, 0)$, approaching the asymptote lines as $x \to \pm \infty$.