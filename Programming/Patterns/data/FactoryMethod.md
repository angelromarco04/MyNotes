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
direction TB
Product_A --|> Product
Product_B --|> Product
Product_C --|> Product
Product .. Creator
Creator <|-- Creator_A
Creator <|-- Creator_B
Creator <|-- Creator_C

class Product {
	<<interface>>
}

class Product_A {
	<<class>>
	+Product_A()
}

class Product_B {
	<<class>>
	+Product_B()
}

class Product_C {
	<<class>>
	+Product_C()
}

class Creator {
	<<abstract class>>
	+createProduct() Product$
}

class Creator_A {
	<<class>>
	+createA() Product_A
}

class Creator_B {
	<<class>>
	+createB() Product_B
}

class Creator_C {
	<<class>>
	+createC() Product_C
}

```
## Code

```java
public class Class { 
 
}
```