### Exercise 3. When Can Matrices Be Multiplied?

The matrix sizes are

$$
A_{2 \times 3}, \quad B_{3 \times 4}, \quad C_{4 \times 2}, \quad D_{2 \times 2}
$$

For the products

$$
AB, \quad BA, \quad BC, \quad CB, \quad AC, \quad CA, \quad AD, \quad DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

---

### Solution

#### Compatibility Rule
The product of two matrices $M_{m \times n}$ and $N_{p \times q}$ is defined if and only if the number of columns in $M$ equals the number of rows in $N$ ($n = p$). When defined, the resulting matrix has size $m \times q$.

#### Step 1: Product $AB$
- Dimensions: $A_{2 \times 3}$ and $B_{3 \times 4}$.
- Inner dimensions match ($3 = 3$).
- **Defined**: Resulting size is $2 \times 4$.

#### Step 2: Product $BA$
- Dimensions: $B_{3 \times 4}$ and $A_{2 \times 3}$.
- Inner dimensions do not match ($4 \neq 2$).
- **Not defined**.

#### Step 3: Product $BC$
- Dimensions: $B_{3 \times 4}$ and $C_{4 \times 2}$.
- Inner dimensions match ($4 = 4$).
- **Defined**: Resulting size is $3 \times 2$.

#### Step 4: Product $CB$
- Dimensions: $C_{4 \times 2}$ and $B_{3 \times 4}$.
- Inner dimensions do not match ($2 \neq 3$).
- **Not defined**.

#### Step 5: Product $AC$
- Dimensions: $A_{2 \times 3}$ and $C_{4 \times 2}$.
- Inner dimensions do not match ($3 \neq 4$).
- **Not defined**.

#### Step 6: Product $CA$
- Dimensions: $C_{4 \times 2}$ and $A_{2 \times 3}$.
- Inner dimensions match ($2 = 2$).
- **Defined**: Resulting size is $4 \times 3$.

#### Step 7: Product $AD$
- Dimensions: $A_{2 \times 3}$ and $D_{2 \times 2}$.
- Inner dimensions do not match ($3 \neq 2$).
- **Not defined**.

#### Step 8: Product $DA$
- Dimensions: $D_{2 \times 2}$ and $A_{2 \times 3}$.
- Inner dimensions match ($2 = 2$).
- **Defined**: Resulting size is $2 \times 3$.