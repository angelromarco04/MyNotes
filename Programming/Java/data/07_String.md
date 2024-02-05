---
Author: AAM
Date: 2024-02-05
tags:
  - "#programming"
  - java
---
---
# 07 String

[Back to Java index](../JAVA.md)

---

`String` class is inmutable

```java
String myString1 = new String("Hello World");
String myString2 = "Hello World";
```

`StringBuffer` class is mutable

```java
StringBuffer mySB = new StringBuffer();
```

---

```java
String myStr = "Hello World";

//lenth() lleva parentesis
for(int i=0; i<myStr.lenth(); i++) {
		char myChar = myStr.charAt(i);
		System.out.println(myChar);
}
```