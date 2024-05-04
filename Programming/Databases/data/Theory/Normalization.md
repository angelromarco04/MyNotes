
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

---
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
#### Functional dependency set
Is a set with all the functional dependencies:
$$F = \{\:\alpha \to  \beta\quad,\quad\beta \to \gamma\quad,\quad...\:\}$$

---
### Closure of $F$ or $F^+$
#### Definition
$F^+$ is the set of all functional dependencies that can be implied from $F$.
#### Armstrong's Axioms
- **Reflexivity**
$$\beta \subseteq \alpha \implies \alpha \to \beta$$
- **Augmentation**
$$\alpha \to \beta \quad\text{ \& }\quad \delta \subseteq \mu \implies \alpha\:\mu \to \beta\:\delta$$
- **Transitive**
$$\alpha \to \beta \quad\text{ \& }\quad \beta \to \gamma \implies \alpha \to \gamma$$
#### Additional rules
From Armstrong's Axioms we can infer:
- **Union**
$$\alpha \to \beta \quad \& \quad \alpha \to \delta \implies \alpha \to\beta\:\delta$$
- **Decomposition**
$$\alpha \to\beta\:\delta \implies \alpha \to \beta \quad \& \quad \alpha \to \delta$$
- **Pseudo-transitive**
$$\alpha \to \beta \quad \& \quad \beta\:\delta \to \mu \implies \alpha\:\delta \to\mu$$
---
### Closure of Attribute Sets ( $\alpha^+$ )
#### Definition
$\alpha^+$ is the set of attributes that are functionally dependent from $\alpha$ under $F$.
#### Algorithm
1. Initially: $\text{Result} := \alpha$
2. For each functional dependency $\quad \beta \to \gamma \quad$ in $F$.
	1. If $\quad \beta \subseteq \text{result} \quad$ then $\quad \text{result} := \text{result} \:\cup\: \gamma\quad$
#### Applications
- **Finding super-keys**. All fields can be implied from the super-key field. 
$$\alpha \to R \in F^+$$
- **Checking if $\alpha \to \beta$ is in $F^+$**.
$$\beta \subseteq \alpha^+ \implies \{\:\alpha \to\beta\:\} \in F^+$$
- **Calculating $F^+$.**
	1. For each $\gamma \in R$ calculate $\gamma^+$.
	2. For each $S \in \gamma^+$ add $\gamma \to S$.
---
### Candidate Key
#### Complete functional dependencies
For $\alpha \to \beta$ to be complete
It cannot exist any $\delta$ such that $\delta \subseteq \alpha$ and $\delta \to \beta$.
#### Definition
For $\alpha\beta$ to be a candidate key it must fulfil:
- $\alpha\beta$ must be a super-key ( $\alpha\beta \to R \implies R \subseteq(\alpha\beta)^+$ ).
- $\alpha\beta \to R$ is a complete functional dependency.
	- Nor $\alpha^+$ nor $\beta^+$ are super-keys.
---
### Canonical Cover ( $F_c$ )
#### Trivial functional dependencies
For $\alpha \to \beta$ to be trivial it must fulfil that $\beta \subseteq \alpha$.
#### Definition
$F_c$ is the minimal set of functional dependencies of $F$ .
All $F_c$ functional dependencies are:
- Non-trivial
- Complete
- Non-redundant (cannot be inferred from others)
#### Algorithm
We