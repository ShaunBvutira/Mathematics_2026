### Problem 7. A Trigonometric Function

#### Question

On $[0, 2\pi]$, find the intervals of monotonicity and the extrema of

$$
f(x) = \sin x + \cos x.
$$

Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

---

### Solution

#### Step 1. Domain and First Derivative

The function $f(x) = \sin x + \cos x$ is continuous on the closed interval $[0, 2\pi]$ and differentiable everywhere on the open interval $(0, 2\pi)$.

Differentiate $f(x)$ term by term:

$$
f'(x) = \frac{d}{dx}(\sin x + \cos x) = \cos x - \sin x
$$

---

#### Step 2. Find the Critical Points in $(0, 2\pi)$

Set $f'(x) = 0$ to find all stationary points inside $(0, 2\pi)$:

$$
\cos x - \sin x = 0 \implies \sin x = \cos x
$$

Since $\cos x = 0$ yields $\sin x = \pm 1 \neq 0$, we can divide both sides by $\cos x$:

$$
\tan x = 1
$$

On the interval $(0, 2\pi)$, $\tan x = 1$ has two solutions (in Quadrant I and Quadrant III):

$$
x_1 = \frac{\pi}{4}, \qquad x_2 = \frac{5\pi}{4}
$$

---

#### Step 3. Sign Analysis of $f'(x)$ and Monotonicity on $[0, 2\pi]$

The critical numbers $x_1 = \frac{\pi}{4}$ and $x_2 = \frac{5\pi}{4}$ partition $[0, 2\pi]$ into three subintervals: $\left[0, \frac{\pi}{4}\right]$, $\left[\frac{\pi}{4}, \frac{5\pi}{4}\right]$, and $\left[\frac{5\pi}{4}, 2\pi\right]$. Test the sign of $f'(x) = \cos x - \sin x$ on each open subinterval:

| Subinterval | Test Point | $\cos x$ | $\sin x$ | Value and Sign of $f'(x) = \cos x - \sin x$ | Behavior of $f(x)$ |
| :--- | :--- | :--- | :--- | :--- | :--- |
| $\left(0, \frac{\pi}{4}\right)$ | $x = \frac{\pi}{6}$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $\frac{\sqrt{3} - 1}{2} > 0$ (**$+$**) | **Strictly increasing** |
| $\left(\frac{\pi}{4}, \frac{5\pi}{4}\right)$ | $x = \frac{\pi}{2}$ | $0$ | $1$ | $-1 < 0$ (**$-$**) | **Strictly decreasing** |
| $\left(\frac{5\pi}{4}, 2\pi\right)$ | $x = \frac{3\pi}{2}$ | $0$ | $-1$ | $+1 > 0$ (**$+$**) | **Strictly increasing** |

**Summary of Monotonicity (including endpoints):**
- **$f(x)$ is strictly increasing** on $\left[0, \frac{\pi}{4}\right]$ and on $\left[\frac{5\pi}{4}, 2\pi\right]$.
- **$f(x)$ is strictly decreasing** on $\left[\frac{\pi}{4}, \frac{5\pi}{4}\right]$.

---

#### Step 4. Evaluate $f(x)$ at Critical Points and Endpoints

Compute the exact value of $f(x) = \sin x + \cos x$ at both critical points and both endpoints of $[0, 2\pi]$:

1. **Left Endpoint ($x = 0$):**
   $$
   f(0) = \sin(0) + \cos(0) = 0 + 1 = 1
   $$

2. **First Critical Point ($x = \frac{\pi}{4}$):**
   $$
   f\!\left(\frac{\pi}{4}\right) = \sin\!\left(\frac{\pi}{4}\right) + \cos\!\left(\frac{\pi}{4}\right) = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} = \sqrt{2} \approx 1.414
   $$

3. **Second Critical Point ($x = \frac{5\pi}{4}$):**
   $$
   f\!\left(\frac{5\pi}{4}\right) = \sin\!\left(\frac{5\pi}{4}\right) + \cos\!\left(\frac{5\pi}{4}\right) = -\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2} = -\sqrt{2} \approx -1.414
   $$

4. **Right Endpoint ($x = 2\pi$):**
   $$
   f(2\pi) = \sin(2\pi) + \cos(2\pi) = 0 + 1 = 1
   $$

---

#### Step 5. Compare Values and Classify All Local and Global Extrema

Ordering the four candidate values from smallest to largest gives:

$$
-\sqrt{2} < 1 < \sqrt{2} \implies f\!\left(\frac{5\pi}{4}\right) < f(0) = f(2\pi) < f\!\left(\frac{\pi}{4}\right)
$$

| Point $x$ | Type of Point | Value $f(x)$ | Extremum Classification on $[0, 2\pi]$ |
| :--- | :--- | :--- | :--- |
| $x = 0$ | Left endpoint | $1$ | **Local minimum** (since $f$ increases on $\left[0, \frac{\pi}{4}\right]$) |
| $x = \frac{\pi}{4}$ | Interior critical point | $\sqrt{2}$ | **Local and global (absolute) maximum** |
| $x = \frac{5\pi}{4}$ | Interior critical point | $-\sqrt{2}$ | **Local and global (absolute) minimum** |
| $x = 2\pi$ | Right endpoint | $1$ | **Local maximum** (since $f$ increases on $\left[\frac{5\pi}{4}, 2\pi\right]$) |

**Final Summary:**
- **Global (Absolute) Maximum:** $f_{\max} = \sqrt{2}$ at $x = \frac{\pi}{4}$ (strictly higher than the endpoint value $1$).
- **Global (Absolute) Minimum:** $f_{\min} = -\sqrt{2}$ at $x = \frac{5\pi}{4}$ (strictly lower than the endpoint value $1$).
- **Endpoint Local Extrema:** Because the interval $[0, 2\pi]$ is closed, the left endpoint $(0, 1)$ is a local minimum and the right endpoint $(2\pi, 1)$ is a local maximum, though neither is a global extremum.