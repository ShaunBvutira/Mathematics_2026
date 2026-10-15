### Matrix Multiplicability & Size Determination

The dimension compatibility condition states that two matrices $M_{m \times n}$ and $N_{p \times q}$ can be multiplied into $MN$ if and only if the number of columns in $M$ equals the number of rows in $N$ ($n = p$). If this condition holds, the resulting matrix has size $m \times q$.

---

### Analysis of Each Product

* **$AB$**
  * **Dimensions:** $(2 \times 3) \times (3 \times 4)$
  * **Compatibility:** **Defined** (inner dimensions match: $3 = 3$)
  * **Resulting Size:** **$2 \times 4$**

* **$BA$**
  * **Dimensions:** $(3 \times 4) \times (2 \times 3)$
  * **Compatibility:** **Undefined** (inner dimensions do not match: $4 \neq 2$)
  * **Resulting Size:** N/A

* **$BC$**
  * **Dimensions:** $(3 \times 4) \times (4 \times 2)$
  * **Compatibility:** **Defined** (inner dimensions match: $4 = 4$)
  * **Resulting Size:** **$3 \times 2$**

* **$CB$**
  * **Dimensions:** $(4 \times 2) \times (3 \times 4)$
  * **Compatibility:** **Undefined** (inner dimensions do not match: $2 \neq 3$)
  * **Resulting Size:** N/A

* **$AC$**
  * **Dimensions:** $(2 \times 3) \times (4 \times 2)$
  * **Compatibility:** **Undefined** (inner dimensions do not match: $3 \neq 4$)
  * **Resulting Size:** N/A

* **$CA$**
  * **Dimensions:** $(4 \times 2) \times (2 \times 3)$
  * **Compatibility:** **Defined** (inner dimensions match: $2 = 2$)
  * **Resulting Size:** **$4 \times 3$**

* **$AD$**
  * **Dimensions:** $(2 \times 3) \times (2 \times 2)$
  * **Compatibility:** **Undefined** (inner dimensions do not match: $3 \neq 2$)
  * **Resulting Size:** N/A

* **$DA$**
  * **Dimensions:** $(2 \times 2) \times (2 \times 3)$
  * **Compatibility:** **Defined** (inner dimensions match: $2 = 2$)
  * **Resulting Size:** **$2 \times 3$**

---

### Summary Table

| Product | Defined? | Inner Dimensions | Resulting Size |
| :--- | :--- | :--- | :--- |
| **$AB$** | **Yes** | $3 = 3$ | **$2 \times 4$** |
| **$BA$** | **No** | $4 \neq 2$ | N/A |
| **$BC$** | **Yes** | $4 = 4$ | **$3 \times 2$** |
| **$CB$** | **No** | $2 \neq 3$ | N/A |
| **$AC$** | **No** | $3 \neq 4$ | N/A |
| **$CA$** | **Yes** | $2 = 2$ | **$4 \times 3$** |
| **$AD$** | **No** | $3 \neq 2$ | N/A |
| **$DA$** | **Yes** | $2 = 2$ | **$2 \times 3$** |
