---
title: Error Handling in Python
linkTitle: Error Handling
date: 2025-11-27
weight: 40
---

Error handling in Python is done using the `try`, `except`, `else`, and `finally` blocks. This allows you to gracefully handle exceptions that may occur during the execution of your program.

## `try` and `except` Blocks
The `try` block is used to wrap code that may potentially raise an exception. If an exception occurs, the code in the `except` block is executed.

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero is not allowed.")

# Output: Error: Division by zero is not allowed.
```

You can also catch multiple exceptions by specifying them in a tuple:

```python
try:
    value = int("abc")
except (ValueError, TypeError):
    print("Error: Invalid value or type.")

# Output: Error: Invalid value or type.
```

## `else` Block
The `else` block is executed if no exceptions are raised in the `try` block.
```python
try:
    result = 10 / 2
except ZeroDivisionError:
    print("Error: Division by zero is not allowed.")
else:
    print("Result is:", result)

# Output: Result is: 5.0
```

## `finally` Block
The `finally` block is executed regardless of whether an exception was raised or not. It is
typically used for cleanup actions.

```python
try:
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("Error: File not found.")
finally:
    print("Execution completed.")
    if 'file' in locals():
        file.close()

# Output:
# Error: File not found.
# Execution completed.
```

## Raising Exceptions
You can raise exceptions manually using the `raise` statement.
```python
def divide(a, b):
    if b == 0:
        raise ValueError("Denominator cannot be zero.")
    return a / b
try:
    result = divide(10, 0)
except ValueError as e:
    print("Error:", e)

# Output: Error: Denominator cannot be zero.
```

## Custom Exceptions
You can create your own custom exception classes by inheriting from the built-in `Exception` class.
```python
class CustomError(Exception):
    pass


def risky_function():
    raise CustomError("This is a custom error.")


try:
    risky_function()
except CustomError as e:
    print("Caught a custom error:", e)

# Output: Caught a custom error: This is a custom error.
```

## Summary
Error handling in Python is essential for building robust applications. By using `try`, `except`, `else`, and `finally` blocks, you can manage exceptions effectively and ensure that your program behaves gracefully in the face of errors.

### Best Practices for Error Handling
- Be specific with exception handling: Catch only the exceptions you expect.
- Avoid using bare `except:` clauses, as they can catch unexpected exceptions.
- Use the `finally` block for cleanup actions that must be executed.
- Document custom exceptions to clarify their purpose and usage.
- Log exceptions for debugging and monitoring purposes.