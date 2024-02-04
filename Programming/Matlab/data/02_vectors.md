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

>> V = [3 : 2 : 11]
V = 
	3    5    7    9    11
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
```