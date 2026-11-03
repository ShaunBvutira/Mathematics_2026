### Exercise 7. Linear Dependence Without Heavy Computation

Given

$$
u = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}, \quad v = \begin{pmatrix} 2 \\ 4 \\ 6 \end{pmatrix}, \quad w = \begin{pmatrix} 0 \\ 1 \\ 1 \end{pmatrix}.
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

---

### Solution

#### Step 1. Identify the specific relation between $u$ and $v$

Observe the entries of $v$ relative to $u$:

$$
v = \begin{pmatrix} 2 \\ 4 \\ 6 \end{pmatrix} = 2 \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix} = 2u
$$

Thus, the exact linear relation between $u$ and $v$ is:

$$
v - 2u = 0 \quad (\text{or } v = 2u)
$$

---

#### Step 2. Decide linear dependence of the set $\{u, v, w\}$

The set of vectors $\{u, v, w\}$ is **linearly dependent** (they cannot be linearly independent).

---

#### Step 3. Explain why no long calculation is needed

By definition, a set of vectors is linearly dependent if at least one vector in the set can be expressed as a linear combination of the others, or equivalently, if there exist scalar coefficients $c_1, c_2, c_3$ (not all zero) such that:

$$
c_1 u + c_2 v + c_3 w = 0
$$

Using the relation $v = 2u$ found in Step 1, we can immediately write down a non-trivial linear combination with $c_1 = -2$, $c_2 = 1$, and $c_3 = 0$:

$$
(-2)u + (1)v + (0)w = -2u + 2u + 0 = 0
$$

Because a non-zero linear combination yielding the zero vector exists without involving $w$ at all, the presence of the pair $\{u, v\}$ alone guarantees that the entire set $\{u, v, w\}$ is linearly dependent. 

No matrix reduction, Gaussian elimination, or determinant calculation is required because scalar multiples among vectors can be recognized directly by inspection.