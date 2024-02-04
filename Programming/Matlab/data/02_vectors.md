---
Author: AAM
Date: 2024-02-04
tags:
  - "#matlab"
  - "#programming"
---
---
# 02 Vectors & Matrices

[Back to index](../index.md)

---

## Vectors
### Creation

```matlab
>> V = [1 2 3]
V = 
	1    2    3
    
>> V = [1, 2, 3]
V = 
	1    2    3
	
% initial : increment : end

>> V = [1 : 2 : 10]
V = 
	1    3    5    7    9

>> V = [11 : -2 : 3]
V = 
	11    9    7    5    3

% Increment by default is 1 or -1

>> V = [1 : 5]
V = 
	1    2    3    4    5
```

### Access

```matlab
>> V = [3, 1, 2, 5, 4];

>> V (2)
ans =
	1

>> V ([3 5 1])
ans =
	2    4    3

>> V ([1 : 2 : 5])
ans =
	3    2    4

% end keyword is substituted by the last index of the vector

>> V(end)
ans =
	4

>> V(end - 2)
ans =
	2

>> V ([3 : 1 : end])
ans =
	2    5    4
```

## Matrix
### Creation

```matlab
>> A = [0 1 2; 2 3 5; 3 4 6]
A =
	0    1    2
	2    3    5
	3    4    6

>> B = [6, 7; 7, 8; 8, 9]
B =
	6    7
	7    8
	8    9

% Matrixes can be concatenated

>> C = [A B]
C =
	0    1    2    6    7
	2    3    5    7    8
	3    4    6    8    9
```

### Access

```matlab
>> A = [0 1 2; 3 4 5; 6 7 8];

>> A (2 , 3)
ans =
	5

>> A ([1 2] , 1)
ans =
	0
	3

>> A (1 , 2:3)
ans =
	1    2

% : can be used to specify the whole row/columm

>> A (1 , :)
ans =
	0    1    2
```


## Operations

| Symbol | Description |
| ---- | ---- |
| + | Matrix addition.  |
| - | Matrix subtraction.  |
| * | Standard matrix multiplication. |
| .* | Elementwise multiplication. |
| A/B | Equivalent to `A * inv(B)`. |
| ./ | Elementwise right division. |
| \ | Equivalent to `inv(A) * B`. |
| .\ | Elementwise left division. |
| .^ | Elementwise power. |

## Some Functions

### Creation
| Function | Description |
| ---- | ---- |
| `ones (n , m)` | Creates a `n x m `matrix full of `1`.<br>If `m` is not specified it will have the value of `n`. |
| `zeros (n , m)` | Creates a `n x m` matrix full of `0`.<br>If `m` is not specified it will have the value of `n`. |
| `eye(n , m)` | Creates a `n x m` matrix with `1` in the main diagonal and `0` elsewhere.<br>If `m` is not specified it will have the value of `n`. |
| `diag(v)` | Creates a matrix with the vector `v` as main diagonal and `0` elsewhere |
| `linspace(a, y, z)` | Creates a vector with y  |
### Other
#TODO