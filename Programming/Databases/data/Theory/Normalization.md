
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

### Functional dependency
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
$$t_1[\:\alpha\:] = t_2[\:\alpha\:] \implies t_1[\:\beta\:] = t_2[\:\beta\:]$$
#### Example
For $\text{Field 1 } \to \text{Field 2}$ to be true:
Having $t_1 = \{\text{ data 11}, \text{ data 12 }\}$, $t_2 = \{\text{ data 21}, \text{ data 22 }\}$
Satisfy that: $\quad\text{data 11} = \text{data 21} \implies \text{data 21} = \text{data 22}$
#### Implication
Having the set of functional dependencies:
$$F = \{\alpha \to  \beta\:,\:\beta \to \gamma\}$$
We can imply that $\alpha\to\gamma$ .

### Closure of $F$ or $F^+$
#### Definition
$F^+$ is the set of all functional dependencies that can be implied from $F$.
#### Armstrong's Axioms
- Reflexivity
$$\beta \subseteq \alpha \implies \alpha \to \beta$$
- Augmentation
$$\alpha \to \beta$$
- Transitive