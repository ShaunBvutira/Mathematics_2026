### . Matrix Size and Entries

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

---

## Important Formulas

### 1. Matrix Size (Dimension)

The size or dimension of a matrix $M$ is written as $m \times n$, where:

$$
m = \mathrm{number\ of\ rows}, \quad n = \mathrm{number\ of\ columns}
$$

### 2. Matrix Entries

The entry $m_{ij}$ denotes the element located at row $i$ and column $j$:

$$
M = \begin{pmatrix}
m_{11} & m_{12} & \cdots & m_{1n} \\
m_{21} & m_{22} & \cdots & m_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
m_{m1} & m_{m2} & \cdots & m_{mn} \\
\end{pmatrix}
$$

### 3. Row and Column Vectors

The $i$-th row vector of $M$ is formed by taking all elements in row $i$:

$$
\mathbf{r}_i = \begin{pmatrix} m_{i1} & m_{i2} & \cdots & m_{in} \end{pmatrix}
$$

The $j$-th column vector of $M$ is formed by taking all elements in column $j$:

$$
\mathbf{c}_j = \begin{pmatrix} m_{1j} \\ m_{2j} \\ \vdots \\ m_{mj} \end{pmatrix}
$$

---

## Step-by-Step Solution

### Step 1: Determine the Sizes of $A$ and $B$

* Matrix $A$ has $2$ rows and $3$ columns. Therefore, the size of $A$ is $2 \times 3$.
* Matrix $B$ has $3$ rows and $2$ columns. Therefore, the size of $B$ is $3 \times 2$.

### Step 2: Read Off the Requested Entries

Using the entry definition $m_{ij}$ (row $i$, column $j$):

* **$a_{12}$** (Entry in row 1, column 2 of $A$):

$$
a_{12} = -1
$$

* **$a_{23}$** (Entry in row 2, column 3 of $A$):

$$
a_{23} = 5
$$

* **$b_{21}$** (Entry in row 2, column 1 of $B$):

$$
b_{21} = -2
$$

* **$b_{32}$** (Entry in row 3, column 2 of $B$):

$$
b_{32} = 1
$$

### Step 3: Write Row and Column Vectors

* **Second row of $A$** as a row vector:

$$
\mathbf{r}_2 = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}
$$

* **First column of $B$** as a column vector:

$$
\mathbf{c}_1 = \begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}
$$
