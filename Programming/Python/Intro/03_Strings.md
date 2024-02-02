# 03 Strings

[Back to Python3 index](../index.md)

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
| str.replace(a, b) | Replaces every ocurrence of `a` by `b`. |