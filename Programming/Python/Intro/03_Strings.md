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
# UPPERCASE AND LOWERCASE
myStr= "heLLo WorLd"
myStr.title()        # "Hello World"  (first uppercase)
myStr.upper()        # "HELLO WORLD"    (all uppercase)
myStr.lower()        # "hello world"    (all lowercase)
```

```python
# BLANK SPACES
myStr = " Python "   
myStr.rstrip()       # " Python"   Remove right space
myStr.lstrip()       # "Python "   Remove left  space
myStr.strip()        # "Python"    Remove both spaces
```