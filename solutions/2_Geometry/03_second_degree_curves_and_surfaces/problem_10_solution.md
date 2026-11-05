### Exercise 10. Paraboloids

Compare the surfaces:

1. Surface 1: $z = x^2 + y^2$ (Circular Paraboloid)
2. Surface 2: $z = x^2 - y^2$ (Hyperbolic Paraboloid / Saddle Surface)

For each surface, describe the cross-sections for $x = 0$, $y = 0$, and $z = c$, and provide a qualitative description for a sketch.

---

### Solution

#### Part 1. Surface 1: $z = x^2 + y^2$ (Circular Paraboloid)

##### 1. Cross-section $x = 0$ ($yz$-plane)
Substitute $x = 0$ into $z = x^2 + y^2$:

$$
z = y^2
$$

- **Type of Curve:** A vertical **parabola** in the $yz$-plane.
- **Features:** Vertex at $(0,0,0)$, opening upward along the positive $z$-axis.

##### 2. Cross-section $y = 0$ ($xz$-plane)
Substitute $y = 0$ into $z = x^2 + y^2$:

$$
z = x^2
$$

- **Type of Curve:** A vertical **parabola** in the $xz$-plane.
- **Features:** Vertex at $(0,0,0)$, opening upward along the positive $z$-axis.

##### 3. Cross-sections $z = c$ (Horizontal planes)
Substitute $z = c$ into $z = x^2 + y^2$:

$$
x^2 + y^2 = c
$$

- **For $c > 0$:** A **circle** in the plane $z = c$ centered at $(0, 0, c)$ with radius $R = \sqrt{c}$. As $c$ increases, the circle expands.
- **For $c = 0$:** A single **point** at the origin $(0, 0, 0)$ (the lowest vertex of the surface).
- **For $c < 0$:** **No real points** (the empty set), since $x^2 + y^2 \ge 0$.

##### 4. Qualitative Sketch / Visual Description
- **Shape:** A smooth, bowl-like surface extending infinitely upward from its vertex at the origin $(0,0,0)$.
- **Vertical profile:** U-shaped parabolic curves opening upward along both principal vertical axis cuts.
- **Horizontal profile:** Circular horizontal rings growing wider as height $z$ increases.

---

#### Part 2. Surface 2: $z = x^2 - y^2$ (Hyperbolic Paraboloid)

##### 1. Cross-section $x = 0$ ($yz$-plane)
Substitute $x = 0$ into $z = x^2 - y^2$:

$$
z = -y^2
$$

- **Type of Curve:** A vertical **parabola** in the $yz$-plane.
- **Features:** Vertex at $(0,0,0)$, opening **downward** along the negative $z$-axis.

##### 2. Cross-section $y = 0$ ($xz$-plane)
Substitute $y = 0$ into $z = x^2 - y^2$:

$$
z = x^2
$$

- **Type of Curve:** A vertical **parabola** in the $xz$-plane.
- **Features:** Vertex at $(0,0,0)$, opening **upward** along the positive $z$-axis.

##### 3. Cross-sections $z = c$ (Horizontal planes)
Substitute $z = c$ into $z = x^2 - y^2$:

$$
x^2 - y^2 = c
$$

- **For $c > 0$:** A **hyperbola** in the plane $z = c$ with vertices at $(\pm\sqrt{c}, 0, c)$, opening left and right along the $x$-direction.
- **For $c = 0$:** A pair of intersecting lines $y = \pm x$ in the plane $z = 0$, forming an "X" through the origin.
- **For $c < 0$:** Rewrite as $y^2 - x^2 = |c|$. A **hyperbola** in the plane $z = c$ with vertices at $(0, \pm\sqrt{|c|}, c)$, opening front and back along the $y$-direction.

##### 4. Qualitative Sketch / Visual Description
- **Shape:** A classic **saddle-shaped surface** (or mountain pass).
- **Saddle Point:** The origin $(0,0,0)$ acts as a stationary point: it is a minimum along the $xz$-parabola ($z = x^2$) and a maximum along the $yz$-parabola ($z = -y^2$).
- **Contour profile:** Horizontal cross-sections form family of hyperbolas that flip their direction of opening as $z$ passes through $0$.

---

### Comparison Table

| Feature | Circular Paraboloid ($z = x^2 + y^2$) | Hyperbolic Paraboloid ($z = x^2 - y^2$) |
| :--- | :--- | :--- |
| **Origin $(0,0,0)$** | Absolute Minimum (Bowl Bottom) | Saddle Point (Min in $x$, Max in $y$) |
| **$x = 0$ Cross-Section** | Upward Parabola ($z = y^2$) | Downward Parabola ($z = -y^2$) |
| **$y = 0$ Cross-Section** | Upward Parabola ($z = x^2$) | Upward Parabola ($z = x^2$) |
| **$z = c > 0$ Cross-Section** | Circle ($x^2 + y^2 = c$) | Hyperbola ($x^2 - y^2 = c$) opening along $x$ |
| **$z = c < 0$ Cross-Section** | No Real Points | Hyperbola ($y^2 - x^2 = \|c\|$) opening along $y$ |