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

## Basic Functions

- `atom? X`
	- Returns `#t` if `X` is an atom.

- `pair? X`
	- Returns `#t` if `X` is a pair.

- `list? X`
	- Returns `#t` if `X` is a list.

- `(quote X)`
	- Returns X as an s-expression.
	- `(quote a)` -> `a`
	- `'a` -> `a`

> [!NOTE]
> For the compiler `(X)` is a function, not an s-expression

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

- `list X Y ...`
	- Returns a list containing given args.
	- `(list 'a)` -> `(a)`
	- `(list 'a 'b)` -> `(a b)`

> [!NOTE]
> `cons` and `list` are not the same:
> `(cons 'a '(b c) )` -> `(a b c)`
> `(list 'a '(b c) )` -> `(a (b c) )`

- null?
- equal?
- eq?
## Function Definition
- define

(recursive)
```scheme
(define (compare a b)
  (if (null? a)
      '()
      (cons
       (cond
         ((< (car a) (car b)) -1)
         ((= (car a) (car b)) 0)
         ((> (car a) (car b)) 1)
         )
       (compare (cdr a) (cdr b))
       )
      )
  )
```

- lambda

## More functions
- if
- cond




