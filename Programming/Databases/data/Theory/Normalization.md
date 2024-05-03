
---
# Normalization

[Back to index](../../index.md)

---

## Introduction

To obtain a good DDBB design we avoid:
- Information repetition.
- Consistency errors and information loss.
- Additional code.

---
## Functional dependencies

### Functional dependency definition
#### Having

| Field 1 | Field 2 |
| ------- | ------- |
| data 11 | data 12 |
| data 21 | data 22 |
| ...     | ...     |
The relation schema is $R = \{\text{ Field 1 }, \text{ Field 2 }\}$

### Definition
It is a functional dependency $\alpha \to \beta$  with  $\alpha, \beta  \in R$
If every pair of tuples $t_1$ , $t_2$  complies that:
$t_1[\:\{\alpha\}\:] = t_2[\:\{\alpha\}\:] \implies t_1[\:\{\text{ Field 2 }\}\:] = t_2[\:\{\text{ Field 2 }\}\:]$

#### Example
$\text{Field 1 } \to \text{Field 2}$ 
$t_1 = \{\text{ data 11}, \text{data 12 }\}$, $t_2 = \{\text{ data 21}, \text{data 22 }\}$

