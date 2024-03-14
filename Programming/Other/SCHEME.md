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

- `(atom? X)`
	- Returns `#t` if `X` is an atom.

- `(pair? X)`
	- Returns `#t` if `X` is a pair.

- `(list? X)`
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

- `(list X Y ...)`
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
- if
- cond

## Variable Definition & let
- `(let [(a X) (b Y)] (func a b))`
	- Let us define some variables in a local scope. `a=X` and `b=Y`.
	- The binding is done in parallel (all at the same time)
	- To use sequential binding use `let*`.
	- `(let [(a 3) (b 2)] (* a b))` -> 3 x 2 = 6
	- `(let [(a 3) (b (+ a 1))] (* a b))` -> ERROR. `a` not defined

- `(let* [(a X) (b Y)] (func a b))`
	- Same as `let` but with sequential binding.
	- `(let* [(a 3) (b (+ a 1))] (* a b))` -> 3 x (3 + 1) = 12

- `(letrec [(a X) (b Y)] (func a b))`
	- Same as `let` but allows recursive calls
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

## Higher Order Functions (HOF)

- `(map func X Y ...)`
	- Applies given function to each element of one or more lists IN ORDER.
	- `(map max '(1 2) '(3 4) '(5 6))` -> `(list (max 1 3 5) (max 2 4 6))`

- `(apply func X Y)`
	- Applies given function to all elements. If a list is provided it unpacks it.
	- `(apply * 5 '(2 3))` -> 5 x 2 x 3 = 30

- `(lambda X func)`
	- Creates a function that does something with a set of variables `X`.
	- `((lambda (x y) (+ x y)) 2 3)` -> `(x y)` = `(2 3)` -> 5
	- `((lambda (x . y) (apply + x y)) 2 3 4)` -> `(x . y)` = `(2 . (3 4))` -> 9
> [!NOTE]
> In lambdas the arguments are passed as a list. For example:
> `(lambda (x y) ... )` is explicitly asking for 2 arguments.
> `(lambda (x . y) ... )` is asking for 1 or more args. (y = rest of args)

- `(filter func X)`
	- Filters a list by a provided boolean function
	- `(filter (lambda x (list? x)) '(1 (2) 3))` -> `(1 3)`

- `((curry func X) Y)`
	- Allows creating a function without an argument.
	- Same as doing `(func X Y)`+
	- `((curry / 2) 3)` -> `(/ 2 3)` -> `2/3`

- `((curryr func X) Y)`
	- Similar to curry but the argument is inserted the first.
	- Same as doing `(func Y X)`
	- `((curryr / 2) 3)` -> `(/ 3 2)` -> `3/2`

- `(compose func1 func2 ...)`
	- Allows to apply functions one after another.
	- `((compose add1 *) 2 3)` -> `(add1 (* 2 3))` -> (2 x 3) + 1 = 7




