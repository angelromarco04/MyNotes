---
Author: AAM
Date: 2024-02-07
tags:
---
---
# Title

[HOME](/README.md)

---


# Data types

- **S-expressions**
	- **Atoms**
		- Independent values
		- Examples: `a`, `B`, `#t`, `#f`
	- **Pairs**
		- Grouping of two atoms.
		- Structure: `(s1 . s2)`
	
- **Lists**
	- Grouping of atoms.
	- The empty list `()` is an atom.
	- Structure: `(s1 . L)` where L is another list.
	- Note that `s1` can also be another list.

# Basic functions

| Function | Return value |
| ---- | ---- |
| `const(x, y)` | A pair `(x . y)` |
| `car(x)` | First element of the S-expression / list `x` |
| `cdr(x)` | Second element of the S-expression / list `x` |
| `atom?(x)` | `#t` if `x` is an atom, `#f` otherwise |
| `list?(x)` | `#t` if `x` is a list, `#f` otherwise |
| `pair?(x)` | `#t` if `x` is a pair, `#f` otherwise |
| `eq?(x, y)` | `#t` if `x` is an atom equal to `y`, `#f` otherwise |
| `null?(x)` | `#t` if `x` is the empty list, `#f` otherwise |
#### Arithmetic, Logic and Relational operations
(+ z …) (and z …) (or z …) (not z) (> x y…) (<= x y …) (<> x y…)
