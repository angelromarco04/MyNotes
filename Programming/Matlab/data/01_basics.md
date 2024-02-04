---
Author: AAM
Date: 2024-02-04
tags:
  - "#matlab"
  - "#programming"
---
---
# 01 Basics

[Back to index](../index.md)

---

### Basic operations
| Name | Symbol |
| ---- | ---- |
| Parenthesis | `( )` |
| Power | `^` |
| Addition | `+` |
| Substraction | `-` |
| Multiplication | `*` |
| Division | `/` |
## Variables

```matlab
% Simple variable
var = 1

% Symbolic variables
syms x y
f(x, y) = x + 3*y
```
## Predefined Variables
| Variable | Description |
| ---- | ---- |
| `ans` | Last result not assigned to a variable. |
| `pi` | Value of pi. |
| `i` -  `j` | Imaginary units. |
| `+inf` -  `-inf` | Infinity. |
| `NaN` | Not a number. |
## Some basic commands
| Command | Description |
| ---- | ---- |
| `whos` | Displays all variables in current session. |
| `clear` | Remove all variables from current session. |
| `date` | Current date. |
| `disp( A )` | Displays contents of A in the console |
## Use of semicolons

In a Matlab script each operation displays its result in the console. To prevent the console from being illegible, each script line ending with a semicolon will not be displayed when executed.