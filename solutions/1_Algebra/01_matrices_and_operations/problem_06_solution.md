### 1. Computations

#### **Transposes $A^T$ and $B^T$**
To find the transpose of a matrix, convert its rows into columns:

$$
A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

$$
B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
$$

---

#### **Product $AB$**

$$
AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

* **Row 1, Column 1:** $(1 \times 1) + (2 \times 2) + (3 \times -1) = 1 + 4 - 3 = 2$
* **Row 1, Column 2:** $(1 \times 0) + (2 \times 1) + (3 \times 3) = 0 + 2 + 9 = 11$
* **Row 2, Column 1:** $(4 \times 1) + (5 \times 2) + (6 \times -1) = 4 + 10 - 6 = 8$
* **Row 2, Column 2:** $(4 \times 0) + (5 \times 1) + (6 \times 3) = 0 + 5 + 18 = 23$
