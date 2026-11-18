### Problem 1. Motion — from Position to Velocity

#### Question

The position of a point is described by

$$
s(t) = t^3 - 6t^2 + 9t + 2, \qquad t \ge 0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

---

### Solution

#### 1. Determine the Velocity and Acceleration

- **Velocity $v(t)$:** Velocity is the first derivative of the position function $s(t)$ with respect to time $t$:

  $$
  \begin{aligned}
  v(t) &= s'(t) = \frac{d}{dt}(t^3 - 6t^2 + 9t + 2) \\
  &= 3t^2 - 12t + 9
  \end{aligned}
  $$

  Factoring out $3$ simplifies further calculations:

  $$
  v(t) = 3(t^2 - 4t + 3) = 3(t - 1)(t - 3), \qquad t \ge 0
  $$

- **Acceleration $a(t)$:** Acceleration is the first derivative of velocity $v(t)$ (the second derivative of position $s(t)$) with respect to time $t$:

  $$
  \begin{aligned}
  a(t) &= v'(t) = s''(t) = \frac{d}{dt}(3t^2 - 12t + 9) \\
  &= 6t - 12 = 6(t - 2), \qquad t \ge 0
  \end{aligned}
  $$

---

#### 2. Find the Times at Which the Point Stops

A point moving along a coordinate axis stops instantaneously when its velocity equals zero ($v(t) = 0$):

$$
\begin{aligned}
3(t - 1)(t - 3) &= 0 \\
t - 1 = 0 \quad &\text{or} \quad t - 3 = 0 \\
t_1 = 1 \quad &\text{or} \quad t_2 = 3
\end{aligned}
$$

Both $t_1 = 1$ and $t_2 = 3$ satisfy the domain condition $t \ge 0$. Thus, the point stops at **$t = 1$** (at position $s(1) = 1 - 6 + 9 + 2 = 6$) and at **$t = 3$** (at position $s(3) = 27 - 54 + 27 + 2 = 2$).

---

#### 3. Determine the Intervals of Motion in the Positive and Negative Directions

The direction of motion is determined by the sign of the velocity $v(t) = 3(t - 1)(t - 3)$:
- **$v(t) > 0$:** The position $s(t)$ is strictly increasing, so the point moves in the **positive direction**.
- **$v(t) < 0$:** The position $s(t)$ is strictly decreasing, so the point moves in the **negative direction**.

The stopping times $t = 1$ and $t = 3$ partition the domain $[0, +\infty)$ into three intervals: $[0, 1)$, $(1, 3)$, and $(3, +\infty)$. Test the sign of $v(t) = 3(t - 1)(t - 3)$ on each interval:

| Time Interval | Test Time | Sign of $(t - 1)$ | Sign of $(t - 3)$ | Sign of $v(t)$ | Direction of Motion |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $[0, 1)$ | $t = 0$ | $-$ | $-$ | **$+$** ($v(0) = 9 > 0$) | **Positive direction** |
| $(1, 3)$ | $t = 2$ | $+$ | $-$ | **$-$** ($v(2) = -3 < 0$) | **Negative direction** |
| $(3, +\infty)$ | $t = 4$ | $+$ | $+$ | **$+$** ($v(4) = 9 > 0$) | **Positive direction** |

**Summary of Motion:**
- The point moves in the **positive direction** on **$[0, 1)$** and on **$(3, +\infty)$** (from $s(0) = 2$ forward to $s(1) = 6$, and from $s(3) = 2$ forward toward $+\infty$).
- The point moves in the **negative direction** on **$(1, 3)$** (reversing backward from $s(1) = 6$ to $s(3) = 2$).