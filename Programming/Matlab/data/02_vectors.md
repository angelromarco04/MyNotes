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

## Vector Creation

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

>> V = [1 : 2 : 10]
V = 
	1    3    5    7    9
```

## Vector Access

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

## Matrix creation

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