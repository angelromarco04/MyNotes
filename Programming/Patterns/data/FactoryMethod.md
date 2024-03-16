---
Author: AAM
Date: 2024-03-16
tags:
  - "#programming"
  - other
  - programming
---
---
# Factory Method

[Back to index](../PATTERNS.md)

---

## Description

Encapsulates the instantiation of classes of the same type.
Use a method instead of direct instantiation.

## Characteristics

- 

## UML

```mermaid
classDiagram
Product <|.. A
Product <|.. B
Product <|.. C

class Product {
	<<interface>>
}

class A {
	<<class>>
	-A()
}

class B {
	<<class>>
	-B()
}

class C {
	<<class>>
	-C()
}

class Factory {
	<<class>>
	-createProduct()
}
```
## Code

```java
public class Class { 
 
}
```