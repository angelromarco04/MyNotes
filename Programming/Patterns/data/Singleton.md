---
Author: AAM
Date: 2024-03-16
tags:
  - programming
  - other
  - "#programming"
  - python
---
---
# Singleton

[Back to index](../PATTERNS.md)

---

## Description

Guaranties only one instance of a class and provide global access to it.

## Characteristics

```mermaid
classDiagram
class Singleton {
	Singleton : - Singleton instance$
	Singleton : - Singleton()$
	Singleton : + getInstance()
```
## Code

```java
public class Singleton { 

	private Singleton() {}
	
	private static Singleton instance = null;
	
	public static Singleton getInstance() {
		if (instance == null)
			instance = new Singleton();
		return instance;
	}
}
```