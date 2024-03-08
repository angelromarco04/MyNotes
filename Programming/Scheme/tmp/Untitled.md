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
		- Grouping of two s-expressions.
		- Structure: `(s1 . s2)`
	
- **Lists**
	- Grouping of atoms.
	- The empty list `()` is an atom.
	- Structure: `(s1 . L)` where L is another list.
	- Note that `s1` can also be another list.

# Functions
- quote (`'`)
- car X
	- 
	- (car '(a b c)) -> a
- cdr X
- cons X, Y.
	- Returns the pair (X . Y)
	- (cons 'a 'b) -> (a . b)
	- (cons '(a b) '((c d) e)) -> ((a b) (c d) e)
- 

