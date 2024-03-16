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

- We have some concrete classes (products) of the same type.
- We implement a creator class that contains the Factory Method (`createProduct()`).
- We implement a specific  

## UML

```mermaid
classDiagram
direction TB
Product <|--  Product_A
Product <|-- Product_B
Product <|-- Product_C

Product_A .. Creator_A
Product_B .. Creator_B
Product_C .. Creator_C

Creator_A --|> Creator
Creator --|> Creator
Creator --|> Creator

class Product {
	<<interface>>
}

class Product_A {
	<<class>>
	~Product_A()
}

class Product_B {
	<<class>>
	~Product_B()
}

class Product_C {
	<<class>>
	~Product_C()
}

class Creator {
	<<class>>
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
public void main(String[] args) {

}
```