### Problem 7. Exponential Growth

#### Question

Assume the model

$$
N(t) = N_0 e^{kt}, \qquad k > 0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t) = kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

---

### Solution

#### 1. Verify by Differentiation That $N'(t) = kN(t)$

Differentiate $N(t) = N_0 e^{kt}$ with respect to $t$, treating $N_0$ and $k$ as constants and applying the Chain Rule to the composite exponential function $e^{kt}$:

$$
\begin{aligned}
N'(t)
&= \frac{d}{dt}\left(N_0 e^{kt}\right) \\
&= N_0 \cdot \frac{d}{dt}\left(e^{kt}\right) \\
&= N_0 \cdot e^{kt} \cdot \frac{d}{dt}(kt) \\
&= N_0 e^{kt} \cdot k \\
&= k\left(N_0 e^{kt}\right)
\end{aligned}
$$

Recognizing that $N_0 e^{kt} = N(t)$, substitute $N(t)$ back into the expression:

$$
N'(t) = kN(t)
$$

Thus, $N(t) = N_0 e^{kt}$ satisfies the differential equation $N'(t) = kN(t)$ for all $t$.

---

#### 2. Find the Population Doubling Time

Assume a non-trivial positive initial population $N_0 > 0$. The **doubling time** $T_d$ is the time elapsed from $t = 0$ until the population reaches twice its initial size, i.e., $N(T_d) = 2N_0$:

$$
N_0 e^{k T_d} = 2N_0
$$

Divide both sides by $N_0$ ($N_0 \neq 0$):

$$
e^{k T_d} = 2
$$

Take the natural logarithm ($\ln$) of both sides to isolate the exponent:

$$
\begin{aligned}
\ln\left(e^{k T_d}\right) &= \ln 2 \\
k T_d &= \ln 2
\end{aligned}
$$

Since $k > 0$, divide both sides by $k$:

$$
T_d = \frac{\ln 2}{k}
$$

---

#### 3. Explain Why the Doubling Time Does Not Depend on $N_0$

1. **Algebraic Cancellation (Multiplicative Scaling):**
   In $N(t) = N_0 e^{kt}$, the initial population $N_0$ acts strictly as a **vertical scaling factor**, whereas the exponential term $e^{kt}$ governs the **relative growth factor** over time $t$:

   $$
   \frac{N(t + \Delta t)}{N(t)} = \frac{N_0 e^{k(t + \Delta t)}}{N_0 e^{kt}} = \frac{e^{kt} \cdot e^{k\Delta t}}{e^{kt}} = e^{k\Delta t}
   $$

   Because $N_0$ cancels out completely in any ratio of populations, the time $\Delta t = T_d$ required for the population to multiply by $2$ (or by any fixed factor) depends solely on the growth rate constant $k$.

2. **Proportional Rate Interpretation ($N'(t) = kN(t)$):**
   The differential equation $N'(t) = kN(t)$ states that the instantaneous rate of growth is **directly proportional to the current population size** (i.e., the relative per-capita growth rate $\frac{N'(t)}{N(t)} = k$ is constant).
   - If you start with a population $10$ times larger, the initial growth rate $N'(0) = kN_0$ is also $10$ times faster—producing $10$ times as many new individuals per unit time, which is the exact extra amount needed to double that $10$-times-larger starting population in the **same time** $T_d = \frac{\ln 2}{k}$.