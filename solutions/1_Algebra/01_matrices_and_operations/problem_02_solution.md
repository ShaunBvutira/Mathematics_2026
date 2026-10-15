### 1. Computations

#### **A + B**
Matrix addition is performed entry by entry:

$$
A + B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
$$

---

#### **A - B**
Matrix subtraction is performed by subtracting corresponding entries:

$$
A - B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
$$

---

#### **3A - 2B**
First, scale each matrix by its respective scalar multiplier:

$$
3A = 3 \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
$$

$$
2B = 2 \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

Now perform the subtraction:

$$
3A - 2B = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

---

### 2. Why Matrix Addition Requires Identical Matrix Sizes

Matrix addition (and subtraction) is defined **element-wise**. Specifically, for any entry in position $(i, j)$ of the resulting matrix $C = A + B$:

$$
c_{ij} = a_{ij} + b_{ij}
$$

For this operation to be mathematically valid:
* Every entry $a_{ij}$ in matrix $A$ must pair with a corresponding entry $b_{ij}$ in matrix $B$ at the exact same row and column position.
* If two matrices have different dimensions (for example, a $2 \times 3$ matrix and a $2 \times 2$ matrix), some entries will lack a corresponding pair to add with, leaving the addition undefined.
