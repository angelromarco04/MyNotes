# Exceptions

[Back to Python3 index](../index.md)

---

## Simple try-except

````python
try:
	# Code to safely execute.
	# It will be executed until an exception is raised.
except:
	# Executed if any exception is raised.
````

## Multiple try-except

````python
try:
	# Code.
except ErrorType2:
	# Executed if an exception of the type ErrorType2 is raised.
except (ErrorType1, ErrorType1):
	# Multiple except with different exceptions can follow a try.
	# Multiple types of exceptions can be specified.
````

## Raise keyword
````python
raise Exception
# Raises an exception of the specified type.
````