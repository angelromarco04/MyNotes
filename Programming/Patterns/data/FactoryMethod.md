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
concreteProduct_A --|> Product
concreteProduct_B --|> Product
concreteProduct_C --|> Product
Product .. Creator
Creator <|-- ConcreteCreator_A
Creator <|-- ConcreteCreator_B
Creator <|-- ConcreteCreator_C

class Product {
	<<interface>>
}

class concreteProduct_A {
	<<class>>
	+concreteProduct_A()
}

class ConcreteProduct_B {
	<<class>>
	+concreteProduct_B()
}

class ConcreteProduct_C {
	<<class>>
	+concreteProduct_C()
}

class Creator {
	<<class>>
	+createProduct() Product
}

class ConcreteCreator_A {
	<<class>>
	+createA()
}

class ConcreteCreator_B {
	<<class>>
	+createB()
}

class ConcreteCreator_C {
	<<class>>
	+createC()
}

```
## Code

```java
public class Class { 
 
}
```