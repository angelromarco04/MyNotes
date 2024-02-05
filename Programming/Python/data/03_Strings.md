---
Author: AAM
Date: 2024-02-05
tags:
  - "#programming"
  - python
---
---
# 03 Strings

[HOME](/README.md)
[Back to index](../PYTHON.md)

---

## Especial Characters

Special characters start always with a backslash ( `\` )

| Character | Description    |
|-----------|----------------|
| `\n`      | Line break     |
| `\t`      | Tabulation     |
| `\\`      | Backslash      |
| `\’`      | Single quotes  |
| `\”`      | Double quotes  |

## Formatting

Replace in a string the variables between curly brackets ( `{` and `}` )

```python
myStr = f" text {variable1} text {variable2} text"
```

## Other Methods

### Uppercase and lowercase

Input :  `str = "heLLo WorLd"`.

| Method | Description | Output |
| ---- | ---- | ---- |
| ``str.title()`` | First letter of each word uppercase | ``"Hello World"`` |
| ``str.capitalize()`` | First letter uppercase | ``"Hello World"`` |
| ``str.upper()`` | All uppercase | ``"HELLO WORLD"`` |
| ``str.lower()`` | All lowercase | ``"hello world"`` |
| `str.swapcase()` | Swaps cases of all letters. | `"HEllO wORlD"` |

### Blank Spaces

Input :  `str = "    Hello World    "`.

| Method | Description |
| ---- | ---- |
| `str.rstrip(char)` | Remove characters from right.<br>By default blank spaces. |
| `str.lstrip(char)` | Remove characters from left.<br>By default blank spaces. |
| `str.strip(char)` | Remove characters from left and right.<br>By default blank spaces. |
| `str.center(int n, char c)` | Centers a string.<br>Uses `n` characters at maximum.<br>Fills with character `c` (Blank space by default).<br> |

### Boolean methods

| Method | Description |
| ---- | ---- |
| `str.isalnum()` | True if only alpha-numerical characters. |
| `str.isalpha()` | True if  letters only. |
| `str.isdigit()` | True if numbers only. |
| `str.islower()` | True if lowercase letters only. |
| `str.isupper` | True if uppercase only. |
| `str.isspace()` | True if spaces only. |

### Other
| Method | Description |
| ---- | ---- |
| `str.join(list)` | Joins all elements of a list.<br>Uses `str` as the separator. |
| `str.replace(a, b, num)` | Replaces a number `num` occurrences of `a` by `b`.<br>If `num = None`, replaces all . |
| `str.split(a)` | Splits into a list using `a` as separator.<br>By default uses blank spaces. |
| `str.count(char)` | Counts occurrences of a given `char`. |

