### Problem 8. Number of Requests Handled by a Server

#### Question

The rate at which requests arrive at a server during the first $5$ minutes is described by the function

$$
r(t) = 100 + 20t \quad [\text{requests/min}], \qquad 0 \le t \le 5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

---

### Solution

#### 1. Compute the Total Number of Requests That Arrived During $[0, 5]$

Because $r(t)$ measures the **instantaneous arrival rate** (in $\text{requests/min}$) and $r(t) = 100 + 20t > 0$ on the entire interval $[0, 5]$, the total number of accumulated requests $N$ over the first $5$ minutes is given by the definite integral of $r(t)$ from $t = 0$ to $t = 5$:

$$
N = \int_{0}^{5} r(t) \, dt = \int_{0}^{5} (100 + 20t) \, dt
$$

Find an antiderivative of $100 + 20t$ and apply the Fundamental Theorem of Calculus:

$$
\begin{aligned}
N
&= \left[ 100t + 20 \cdot \frac{t^2}{2} \right]_{0}^{5} \\
&= \left[ 100t + 10t^2 \right]_{0}^{5} \\
&= \bigl(100(5) + 10(5)^2\bigr) - \bigl(100(0) + 10(0)^2\bigr) \\
&= (500 + 250) - 0 \\
&= 750 \text{ requests}
\end{aligned}
$$

*(Geometric check: On $[0, 5]$, the graph of $r(t) = 100 + 20t$ forms a trapezoid of width $5\text{ min}$ and parallel vertical heights $r(0) = 100\text{ requests/min}$ and $r(5) = 200\text{ requests/min}$, giving $N = \frac{100 + 200}{2} \cdot 5 = 150 \cdot 5 = 750\text{ requests}$.)*

---

#### 2. Compute the Average Rate of Incoming Requests Over $[0, 5]$

The average rate $r_{\text{avg}}$ over the interval $[a, b] = [0, 5]$ is the total number of requests divided by the total elapsed time:

$$
\begin{aligned}
r_{\text{avg}}
&= \frac{1}{5 - 0} \int_{0}^{5} r(t) \, dt \\
&= \frac{750 \text{ requests}}{5 \text{ min}} \\
&= 150 \text{ requests/min}
\end{aligned}
$$

---

#### 3. Compare the Average Rate with the Values $r(0)$ and $r(5)$

Evaluate the arrival rate at the two endpoints of the interval $[0, 5]$:
- **Initial rate at $t = 0$:**
  $$
  r(0) = 100 + 20(0) = 100 \text{ requests/min}
  $$
- **Final rate at $t = 5$:**
  $$
  r(5) = 100 + 20(5) = 200 \text{ requests/min}
  $$

**Comparison and Interpretation:**
1. **Strict Ordering:**
   $$
   r(0) = 100 < r_{\text{avg}} = 150 < r(5) = 200 \quad [\text{requests/min}]
   $$
2. **Exact Arithmetic Mean (Midpoint Property of Linear Functions):**
   Notice that $r_{\text{avg}} = 150\text{ requests/min}$ is the **exact arithmetic mean** of the endpoint rates:

   $$
   \frac{r(0) + r(5)}{2} = \frac{100 + 200}{2} = 150 = r_{\text{avg}}
   $$

   This happens because $r(t) = 100 + 20t$ is a **linear function**—its rate of increase ($20\text{ requests/min}^2$) is constant, so the deficit in requests during the first half of the interval ($t \in [0, 2.5]$, where $r(t) < 150$) is equal in magnitude to the surplus during the second half ($t \in [2.5, 5]$, where $r(t) > 150$). Consequently, the average rate is achieved precisely at the time midpoint $t = 2.5\text{ min}$ ($r(2.5) = 150$).