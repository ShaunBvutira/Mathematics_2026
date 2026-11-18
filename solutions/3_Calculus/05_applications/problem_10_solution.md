### Problem 10. A Cable Through Water and Land

#### Question

Point $A$ lies on one bank of a river of width $100\text{ m}$, and point $B$ lies on the other bank, $500\text{ m}$ along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

---

### Solution

#### Step 1. Set Up the Geometry and Define the Variable

Let $O$ be the point on the opposite bank directly across the river from $A$ (so the segment $AO$ is perpendicular to both riverbanks and has length $100\text{ m}$), and let $P$ be the point along the opposite bank between $O$ and $B$ where the cable comes out of the water.

```text
  Opposite bank:  O -------- x -------- P ------------ (500 - x) ------------ B
                  |                    /
                  |                   /
  River (100 m)   | 100 m            /  Underwater cable: sqrt(100^2 + x^2)
                  |                 /
                  |                /
  Near bank:      A --------------+