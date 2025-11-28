---
title: Variables in Python
linkTitle: Variables
date: 2025-11-27
weight: 5
---

In Python, a variable is a named location used to store data in memory. Variables are created when you assign a value to them, and they can hold different types of data, such as numbers, strings, lists, and more.

## Creating Variables
To create a variable in Python, you simply assign a value to a name using the equals sign (`=`). Here are some examples:

```python
# Creating an integer variable
age = 25
# Creating a float variable
height = 5.9
# Creating a string variable
name = "Alice"
# Creating a boolean variable
is_student = True
```

## Variable Naming Rules
When naming variables in Python, you should follow these rules:
- Variable names must start with a letter (a-z, A-Z) or an underscore (_).
- The rest of the variable name can contain letters, numbers (0-9), and underscores
- Variable names are case-sensitive (e.g., `age` and `Age` are different variables).
- Avoid using Python reserved keywords as variable names (e.g., `if`, `for`, `while`, etc.).

## Dynamic Typing
Python is a dynamically typed language, which means you do not need to declare the data type of a variable explicitly. The interpreter infers the type based on the assigned value. You can also change the type of a variable by assigning a new value of a different type:

```python
# Initially an integer
value = 10
print(type(value))  # Output: <class 'int'>
# Changing to a string
value = "Hello"
print(type(value))  # Output: <class 'str'>
```
## Multiple Assignments
Python allows you to assign values to multiple variables in a single line:
```python
x, y, z = 1, 2.5, "Python"
print(x)  # Output: 1
print(y)  # Output: 2.5
print(z)  # Output: Python
```
## Constants
While Python does not have built-in constant types, it is a common convention to use uppercase variable names to indicate that a variable should be treated as a constant and not modified:
```python
PI = 3.14159
GRAVITY = 9.81
```

Changing the value of these "constants" is possible, but it is discouraged by convention.
```python
PI = 3.14159

PI = 3.14  # This is possible but not recommended
```
## Summary
Variables are fundamental components in Python programming, allowing you to store and manipulate data. By following proper naming conventions and understanding dynamic typing, you can effectively use variables in your Python code.

### Best Practices for Variable Naming
- Use descriptive names that convey the purpose of the variable.
- Use underscores to separate words in variable names (e.g., `student_name`).
- Keep variable names concise but meaningful.
- Follow consistent naming conventions throughout your codebase.
