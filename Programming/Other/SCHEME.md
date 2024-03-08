---
Author: AAM
Date: 2024-02-07
tags:
  - programming
  - other
---

---
# SCHEME

[HOME](/README.md)

---

## Data types

- **S-expressions**
	- **Atoms**
		- Independent values
		- Examples: `a`, `B`, `#t`, `#f`
	- **Pairs**
		- Grouping of two s-expressions.
			- Can be atoms or another pairs.
		- Structure: `(s1 . s2)`
	
- **Lists**
	- Grouping of atoms.
	- The empty list `()` is an atom.
	- Structure: `(s1 . L)` where L is another list.
	- Note that `s1` can also be another list.

## Functions

- `atom? X`
	- Returns `#t` if `X` is an atom.

- `pair? X`
	- Returns `#t` if `X` is a pair.

- `list? X`
	- Returns `#t` if `X` is a list.

- `(quote X)`
	- Returns X as an s-expression.
	- `(X)` is a function, not an s-expression
	- `(quote a)` -> `a`
	- `'a` -> `a`

- `(car X)`
	- Returns first element of a pair.
	- `(car '(a . b))` -> `a`
	- `(car '(a b c))` -> `a`
	- `(car '((a b) c))` -> `(a b)`

- `(cdr X)`
	- Returns second element of a pair.
	- `(cdr '(a . b))` -> `b`
	- `(cdr '(a b c))` -> `(b c)`
	- `(cdr '((a b) c))` -> `(c)` (NOT `c`)

> [!NOTE]
> `car` and `cdr` can be combined.
> `(car (car (cdr X)))` = `(caadr X)`

- `(cons X Y)`
	- Returns the pair `(X . Y)`
	- (cons 'a 'b) -> (a . b)
	- (cons '(a b) '((c d) e)) -> ((a b) (c d) e)

- null?
- equal?
- eq?
- if
- cond


- define

