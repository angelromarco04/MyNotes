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
| ``str.title()`` | first letter of each word uppercase | ``"Hello World"`` |
| ``str.capitalize()`` | first letter uppercase | ``"Hello World"`` |
| ``str.upper()`` | all uppercase | ``"HELLO WORLD"`` |
| ``str.lower()`` | all lowercase | ``"hello world"`` |

### Blank Spaces

Input :  `str = "    Hello World    "`.

| Method | Description |
| ---- | ---- |
| `str.rstrip(cha)` | Remove characters from right. |
| `str.lstrip()` | Remove characters from left. |
| `str.strip()` | Remove characters from left and right. |
| `str.center(int n, char c)` | Centers a string.<br>Uses `n` characters at maximum.<br>Fills with character `c` (Blank space by default).<br> |

### Boolean methods

| Method | Description |
| ---- | ---- |
| `str.isalnum()` | true if only alpha-numerical characters. |
| `str.isalpha()` | true if  letters only. |
| `str.isdigit()` | true if numbers only. |
| `str.islower()` | true if lowercase letters only |
| `str.isupper` | true if uppercase only |
| `str.isspace()` | true if spaces only |

### Other
| Method | Description |
| ---- | ---- |
| `str.join(list)` | Joins all elements of a list<br>Uses `str` as the separator. |