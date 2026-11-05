### Exercise 6. Angle Between Planes

Given

$$
\Pi_1: x + y + z = 1, \quad \Pi_2: x - y = 2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

---

### Solution

#### Step 1. Extract normal vectors and check for parallelism

Extract the normal vectors $n_1$ and $n_2$ directly from the coefficients of $x, y, z$ in each plane equation:

$$
n_1 = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}, \quad n_2 = \begin{pmatrix} 1 \\ -1 \\ 0 \end{pmatrix}
$$

Check if $n_1$ is a scalar multiple of $n_2$ ($n_1 = k n_2$):

- For the $z$-component: $1 = k(0)$, which is impossible.

Since $n_1$ and $n_2$ are not parallel (not scalar multiples), the planes $\Pi_1$ and $\Pi_2$ are **not parallel** and must intersect along a line.

---

#### Step 2. Compute the angle $\theta$ between the planes

The acute angle $\theta$ between two intersecting planes is defined as the acute angle between their normal vectors $n_1$ and $n_2$:

$$
\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \|n_2\|}
$$

1. **Compute the dot product $n_1 \cdot n_2$:**
   $$
   n_1 \cdot n_2 = (1)(1) + (1)(-1) + (1)(0) = 1 - 1 + 0 = 0
   $$

2. **Compute the magnitudes $\|n_1\|$ and $\|n_2\|$:**
   $$
   \|n_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}
   $$
   $$
   \|n_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{2}
   $$

3. **Calculate $\cos\theta$:**
   $$
   \cos\theta = \frac{|0|}{\sqrt{3} \cdot \sqrt{2}} = 0
   $$

4. **Solve for $\theta$:**
   $$
   \theta = \arccos(0) = 90^\circ \quad \left(\text{or } \frac{\pi}{2} \text{ radians}\right)
   $$

The angle between the two planes is **$90^\circ$** (they are perpendicular planes).

---

#### Step 3. Explain why normal vectors alone are enough

1. **Geometric Rigidity:** A normal vector $n$ completely dictates the spatial tilt and orientation of its plane in 3D space ($\mathbb{R}^3$), as every vector lying inside the plane is strictly orthogonal to $n$.
2. **Invariance under Translation:** Shifting a plane parallel to itself (changing the constant $D$ in $Ax + By + Cz = D$) changes its position in space but does not alter its direction or inclination angle. 
3. **Identical Angle of Inclination:** Tilting a flat surface by an angle $\theta$ tilts its perpendicular normal line by the exact same angle $\theta$. Thus, measuring the angle between the two perpendicular normal vectors $n_1$ and $n_2$ directly measures the dihedral angle between the planes $\Pi_1$ and $\Pi_2$.