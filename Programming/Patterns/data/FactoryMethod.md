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
A --|> Product
B --|> Product
C --|> Product
Product .. Factory
Factory <|-- ConcreteCreatorA
Factory <|-- ConcreteCreatorB
Factory <|-- ConcreteCreatorC

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

class ConcreteCreatorA {
	<<class>>
	-createA()
}

class ConcreteCreatorB {
	<<class>>
	-createB()
}

class ConcreteCreatorC {
	<<class>>
	-createC()
}

```
## Code

```java
public class Class { 
 
}
```