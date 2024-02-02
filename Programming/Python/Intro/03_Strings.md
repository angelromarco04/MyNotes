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

```python
# Method application
myStr= "heLLo WorLd"
myStr.method()
```

### Uppercase and lowercase

Input :  `"heLLo WorLd"`.

| Method | Description | Output |
| ---- | ---- | ---- |
| ``title()`` | first letter of each word uppercase | ``"Hello World"`` |
| ``capitalize()`` | first letter uppercase | ``"Hello World"`` |
| ``upper()`` | all uppercase | ``"HELLO WORLD"`` |
| ``lower()`` | all lowercase | ``"hello world"`` |

### Blank Spaces

Input :  `"    Hello World    "`.

| Method | Description | Output |
| ---- | ---- | ---- |
| `rstrip()` | Remove right space | `"    Hello World"` |
| `lstrip()` | Remove left  space | `"Hello World    "` |
| `strip()` | Remove left and right spaces | `"Hello World"` |
| `center(int n, char c)` | Centers a string<br>Uses n characters at maximum.<br>Fills with character c.<br> |  |

