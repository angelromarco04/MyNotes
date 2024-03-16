---
Author: AAM
Date: 2024-03-16
tags:
  - "#programming"
  - other
  - programming
---
---
# Factory

[Back to index](../PATTERNS.md)

---

# Description

Encapsulates the instantiation of classes of the same type.
Use a method instead of direct instantiation.

# Factory Method

## Characteristics

- We have some concrete classes (products) of the same type.
- We implement a creator class
	- Contains most of the program logic.
	- Contains the **abstract** Factory Method (`createProduct()`).
	- Should have no logic **FOR CREATION**.
	- Can be abstract.
- We implement a specific creators
	- One for each concrete product.
	- Contains all the logic for that product creation.
	- Contains a specific implementation of `createProduct()`.

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
Creator_B --|> Creator
Creator_C --|> Creator

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

## Use

```java
public void main(String[] args) {

	Creator creator1 = new Creator_A();
	Product product1 = creator1.createProduct();
}
```

# Simple Factory

## Characteristics

- Similar to Factory Method
- Has no specific creators but a general one.

## UML

```mermaid
classDiagram
direction LR
Creator .. Product
Product <|--  Product_A
Product <|-- Product_B

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

class Creator {
	<<class>>
	+createProduct() Product$
}
```
