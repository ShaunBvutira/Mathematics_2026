### Exercise 4. Dot Product and Perpendicularity

For $u = (1, 2, -1)^T$ and $v = (2, -1, 3)^T$, compute $u \cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w = (2, -1, a)^T$ is perpendicular to $u$, and check the result.

---

### Solution

#### Step 1. Compute $u \cdot v$ and check perpendicularity

The dot product of two vectors $u = (u_1, u_2, u_3)^T$ and $v = (v_1, v_2, v_3)^T$ is defined as:

$$
u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3
$$

Substituting $u = (1, 2, -1)^T$ and $v = (2, -1, 3)^T$:

$$
\begin{aligned}
u \cdot v &= (1)(2) + (2)(-1) + (-1)(3) \\
          &= 2 - 2 - 3 \\
          &= -3
\end{aligned}
$$

- **Perpendicularity Check:** 
  Two non-zero vectors are orthogonal (perpendicular) if and only if their dot product is zero ($u \cdot v = 0$). 
  Because $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**.

---

#### Step 2. Find $a$ such that $w = (2, -1, a)^T$ is perpendicular to $u$

For $w$ to be perpendicular to $u$, we require $u \cdot w = 0$:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 0
$$

Simplify the equation:

$$
\begin{aligned}
2 - 2 - a &= 0 \\
-a &= 0 \\
a &= 0
\end{aligned}
$$

Thus, $w = (2, -1, 0)^T$.

---

#### Step 3. Verify the result

Substitute $a = 0$ into $w$ and compute $u \cdot w$:

$$
\begin{aligned}
u \cdot w &= (1)(2) + (2)(-1) + (-1)(0) \\
          &= 2 - 2 + 0 \\
          &= 0
\end{aligned}
$$

Since $u \cdot w = 0$, the vector $w = (2, -1, 0)^T$ is indeed perpendicular to $u$.
