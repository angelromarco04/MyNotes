
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
## PART 1

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
#### Objectives
Try to eliminate extraneous attributes for each $\alpha \to \beta$.
- Test if $A \in \alpha$ is extraneous in $\alpha$.
$$\beta \in(\{\alpha\} - A)^+$$
- Test if $A \in \beta$ is extraneous in $\beta$.
$$
\begin{align}
F' = (F-\{\alpha\to\beta\})\quad\cup\quad\{\alpha\to(\beta-A)\}
\end{align}
$$
	(Replace $\alpha \to \gamma \:A\quad$ by $\quad\alpha \to\gamma$. Note that $\beta = \gamma\:A$)
#### Algorithm
1. Apply union rule. Replace $\alpha \to \beta$ and $\alpha \to \delta$ with $\alpha \to \beta\:\delta$.
2. Find and delete all extraneous attributes.
---
## PART 2

---
### Decomposition of relations
#### Definition

- The whole set of attributes $R$ is divided into several $R_i$ .
$$R = R_1\:\cup\:R_2\:\cup\:\:...\:\cup\:R_n$$
- R is always contained in the junction of all $R_i$ but not necessary equal.
$$r \subseteq r_1\:\triangleright\triangleleft\:\:r_2\:\triangleright\triangleleft\:\:...\:\triangleright\triangleleft\:r_n$$
- We try to obtain a equivalent (lossless) decomposition:
	- No information loss ( $r = r_1\:\triangleright\triangleleft\:\:r_2\:\triangleright\triangleleft\:\:...\:\triangleright\triangleleft\:r_n$ )
	- Preserve dependencies ( $F^+_R = F_1\:\:\cup\:\:...\:\cup\:\:F_n$ )
- Lossy decompositions generate fake tuples on join.
#### Principle of Rissanen
- Check if $R$ decomposition in $R_1$ and $R_2$ is lossless. ($n = 2$).
- $R_1 \subseteq (R_1 \cap R_2)^+ \quad$ OR $\quad R_2 \subseteq (R_1 \cap R_2)^+$.
#### Algorithm for $n > 2$
1. We have $R$, $F$ and $R_i : i \in [1, n]$.
$$
\begin{align}
&R = (A,\:B,\:C,\:D,\:E)\\
&F = \{A \to B,\:D \to E,\:A\}\\\\
&F_1 = (A, \:B)\\
&F_2 = (A,\:D,\:E)\\
&F_3 = (C,\:D)
\end{align}
$$
2. Create a table with n rows and as many columns as attributes in R

| $R_i$   | A   | B   | C   | D   | E   |
| ------- | --- | --- | --- | --- | --- |
| A, B    |     |     |     |     |     |
| A, D, E |     |     |     |     |     |
| C, D    |     |     |     |     |     |
3. Mark the attributes contained in each $R_i$
	(for clarity we mark with a + the column number).

| $R_i$   | A   | B   | C   | D   | E   |
| ------- | --- | --- | --- | --- | --- |
| A, B    | a1  | a2  |     |     |     |
| A, D, E | a1  |     |     | a4  | a5  |
| C, D    |     |     | a3  | a4  |     |

4. Apply the relations in $F$ one by one
	(taking into account the marked attributes, NOT the ones in $R_i$).

| $D \to E, \:A$ | A      | B   | C   | D   | E      |
| -------------- | ------ | --- | --- | --- | ------ |
| A, B           | a1     | a2  |     |     |        |
| A, D, E        | a1     |     |     | a4  | a5     |
| C, D           | **a1** |     | a3  | a4  | **a5** |

| $A \to B$ | A   | B      | C   | D   | E   |
| --------- | --- | ------ | --- | --- | --- |
| A, B      | a1  | a2     |     |     |     |
| A, D, E   | a1  | **a2** |     | a4  | a5  |
| C, D      | a1  | **a2** | a3  | a4  | a5  |
5. If a full row is marked then the decomposition is lossless
---
### Dependency Preservation
- Having $R$ decomposed in $R_1,\:...,\:R_n$, all dependencies are preserved if:
$$F^+ = (F_1\:\cup\:...\:\cup\:F_n)^+ \quad\text{where}\quad F_i=F^+ \cap\:R_i$$
- To check if a concrete dependency $\alpha \to \beta$  is preserved:
	1. $\text{result} = \alpha$
	2. For each $R_i$ do $\text{result} = result \cup ((\text{result} \cap R_i)^+\cap R_i)$
	3. It must fulfil $\beta \in \text{result}$.
---
### First Normal Form (1FN)
- Multi-values are not allowed.
- Relation $A \to B,\:C$ is transformed to $A \to B$ and $A \to C$.
