---
Author: AAM
Date: 2024-03-25
tags:
  - ComputerScience
  - OperatingSystems
---
---
# Processes Control

[Back to index](../OS.md)

---
## Process Typology

```mermaid
---
displayMode: compact
---
gantt
    title CPU intensive
    dateFormat X
    axisFormat %s
    
    exec    : a, 0, 4
    IO      : crit, b, 4, 6
    exec    : a, 6, 10
    IO      : crit, b, 10, 12
    exec    : a, 12, 16
    IO      : crit, b, 16, 18
    exec    : a, 18, 22
```
- More CPU use than I/O.
- Few CPU strikes with long duration.

```mermaid
---
displayMode: compact
---
gantt
    title IO intensive
    dateFormat X
    axisFormat %s
    
    exec    : a1, 0, 1
    IO      : crit, b1, after a1, 3
    exec    : a2, after b1, 4
    IO      : crit, b2, after a2, 6
    exec    : a3, after b2, 7
    IO      : crit, b3, after a3, 9
    exec    : a4, after b3, 10
```
- More I/O than CPU use.
- Many CPU strikes with short duration.

---
## Long term scheduler

---
## Mid term scheduler

---
## Process Switching

---
## Process Shutdown

---