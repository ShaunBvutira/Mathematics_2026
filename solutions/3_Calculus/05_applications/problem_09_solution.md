### Problem 9. Minimizing the Material Used for a Can

#### Question

A closed cylinder has fixed volume $V$.
1. Write the volume constraint.
2. Eliminate one of the variables.
3. Express the surface area as a function of the radius $r$.
4. Find the relation between the height $h$ and the radius $r$ for which the material usage is minimal.

Interpret the obtained relation geometrically.

---

### Solution

#### 1. Write the Volume Constraint

Let $r > 0$ be the radius of the circular base and $h > 0$ be the height of the closed right circular cylinder.

The volume of a cylinder is the product of its base area ($\pi r^2$) and its height ($h$), which equals the fixed constant $V > 0$:

$$
\pi r^2 h = V
$$

---

#### 2. Eliminate One of the Variables

Solve the volume constraint $\pi r^2 h = V$ for the height $h$ in terms of the radius $r$ (since $r > 0$, dividing by $\pi r^2$ is valid):

$$
h = \frac{V}{\pi r^2}
$$

---

#### 3. Express the Surface Area as a Function of the Radius $r$

For a **closed** cylinder (having both a top lid and a bottom base), the total material usage is proportional to its total surface area $S$, which consists of:
- **Two circular bases (top and bottom):** $2 \cdot (\pi r^2) = 2\pi r^2$
- **Lateral (curved) side wall:** circumference $\times$ height $= (2\pi r)h = 2\pi rh$

Adding both parts gives the total surface area in two variables:

$$
S(r, h) = 2\pi r^2 + 2\pi rh
$$

Substitute $h = \frac{V}{\pi r^2}$ from Step 2 to express the surface area $S(r)$ as a single-variable function of $r$ on the physical domain $r \in (0, +\infty)$:

$$
\begin{aligned}
S(r)
&= 2\pi r^2 + 2\pi r \left( \frac{V}{\pi r^2} \right) \\
&= 2\pi r^2 + \frac{2V}{r}, \qquad r > 0
\end{aligned}
$$

---

#### 4. Find the Relation Between $h$ and $r$ for Minimal Material Usage

1. **Differentiate $S(r)$ and Find the Critical Point:**
   Rewrite $\frac{2V}{r} = 2V r^{-1}$ and differentiate with respect to $r$ (treating $V$ as a positive constant):

   $$
   \begin{aligned}
   S'(r)
   &= \frac{d}{dr}\left(2\pi r^2 + 2V r^{-1}\right) \\
   &= 4\pi r - 2V r^{-2} \\
   &= 4\pi r - \frac{2V}{r^2}
   \end{aligned}
   $$

   Set $S'(r) = 0$ to locate the critical radius inside $(0, +\infty)$:

   $$
   \begin{aligned}
   4\pi r - \frac{2V}{r^2} &= 0 \\
   4\pi r &= \frac{2V}{r^2} \\
   4\pi r^3 &= 2V \\
   r^3 &= \frac{V}{2\pi} \\
   r &= \sqrt[3]{\frac{V}{2\pi}}
   \end{aligned}
   $$

2. **Verify That This Radius Gives a Global Minimum:**
   Compute the second derivative $S''(r)$:

   $$
   \begin{aligned}
   S''(r)
   &= \frac{d}{dr}\left(4\pi r - 2V r^{-2}\right) \\
   &= 4\pi + 4V r^{-3} \\
   &= 4\pi + \frac{4V}{r^3}
   \end{aligned}
   $$

   Since $V > 0$ and $r > 0$, we have $S''(r) > 0$ for **all** $r \in (0, +\infty)$. Thus, $S(r)$ is strictly convex (concave up) everywhere on $(0, +\infty)$—and since $\lim_{r \to 0^+} S(r) = +\infty$ and $\lim_{r \to +\infty} S(r) = +\infty$—the critical point $r = \sqrt[3]{\frac{V}{2\pi}}$ yields the unique **global minimum** of surface area.

3. **Determine the Optimal Relation Between $h$ and $r$:**
   Substitute $V = 2\pi r^3$ (from $4\pi r^3 = 2V$) back into the height expression $h = \frac{V}{\pi r^2}$:

   $$
   \begin{aligned}
   h
   &= \frac{2\pi r^3}{\pi r^2} \\
   &= 2r
   \end{aligned}
   $$

   Therefore, material usage is minimal when:

   $$
   h = 2r
   $$

---

#### Geometric Interpretation

1. **Height Equals Diameter ($h = d$):**
   Since the diameter of the circular base is $d = 2r$, the optimality condition $h = 2r$ states that **the height of the can must equal the diameter of its base ($h = d$)**.

2. **Square Cross-Section:**
   Slicing the optimal closed cylinder vertically through its central axis produces a **square** cross-section of side length $d \times h = 2r \times 2r$. Among all closed right circular cylinders enclosing a fixed volume $V$, the "square-profile" cylinder minimizes the surface-area-to-volume ratio by balancing the cost of the top/bottom circular lids ($2\pi r^2$) against the cost of the curved side wall ($2\pi r(2r) = 4\pi r^2$, making the side wall area exactly twice the combined area of the two lids).