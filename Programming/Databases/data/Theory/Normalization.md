
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

Having a table:

| Field 1 | Field 2 |
| ------- | ------- |
| data 11 | data 12 |
| ...     | ...     |
The relation schema is $R = \{\text{ Field 1 }, \text{ Field 2 }\}$

If every pair of tuples ($t_1$, $t_2$) complies that:
$t_1[\:\{\text{ Field 1 }\}\:] = t_2[\:\{\text{ Field 1 }\}\:] \implies t_1[\:\{\text{ Field 2 }\}\:] = t_2[\:\{\text{ Field 2 }\}\:]$

It is a functional dependency ( $\text{Field 1 } \to \text{Field 2}$ )



