### Exercise 5. Angle Between Vectors

Given $u = (1, 1, 0)^T$ and $v = (1, 0, 1)^T$:

1. Use the sign of $u \cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

---

### Solution

#### Step 1. Predict the type of angle using the sign of $u \cdot v$

Compute the dot product $u \cdot v$:

$$
\begin{aligned}
u \cdot v &= (1)(1) + (1)(0) + (0)(1) \\
          &= 1 + 0 + 0 \\
          &= 1
\end{aligned}
$$

- **Prediction:** Since $u \cdot v = 1 > 0$, the cosine of the angle between the vectors is positive ($\cos\theta > 0$). This predicts that the angle $\theta$ is **acute** ($0^\circ \le \theta < 90^\circ$ or $0 \le \theta < \frac{\pi}{2}$).

---

#### Step 2. Compute the exact angle $\theta$

1. **Calculate the magnitudes $\|u\|$ and $\|v\|$:**

$$
\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{1 + 1 + 0} = \sqrt{2}
$$

$$
\|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{1 + 0 + 1} = \sqrt{2}
$$

2. **Apply the geometric definition of the dot product ($u \cdot v = \|u\| \|v\| \cos\theta$):**

$$
\cos\theta = \frac{u \cdot v}{\|u\| \|v\|} = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}
$$

3. **Solve for $\theta$:**

$$
\theta = \arccos\left(\frac{1}{2}\right) = 60^\circ \quad \left(\text{or } \frac{\pi}{3} \text{ radians}\right)
$$

---

#### Step 3. Compare the result with the prediction

- **Calculated Angle:** $\theta = 60^\circ$
- **Comparison:** $60^\circ$ is strictly between $0^\circ$ and $90^\circ$, which confirms that the angle is acute. This completely matches the prediction made in Step 1 based on the positive sign of $u \cdot v$.