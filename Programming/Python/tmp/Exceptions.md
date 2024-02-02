# Exceptions

[Back to Python3 index](../index.md)

---

## Try-catch

````python
try:
	# Code to safely execute.
	# It will be executed until an exception is raised.
except ExceptionType:
	# Executed if an exception of the type ExceptionType is raised.
	# If not specified it will be executed with any exception.
	# Multiple except with different exceptions can follow a try.
```