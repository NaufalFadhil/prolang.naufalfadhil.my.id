---
title: Expressions in Python
linkTitle: Expressions
date: 2025-11-27
weight: 20
---

In Python, an expression is a combination of values, variables, operators, and function calls that can be evaluated to produce a result. Expressions are used to perform calculations, manipulate data, and make decisions in your code.

## Basic Expressions
A basic expression can consist of literals (like `numbers` and `strings`), variables, and operators. For
example:

```python
# Numeric expression
result = 5 + 3 * 2
print(result)  # Output: 11
# String expression
greeting = "Hello, " + "world!"
print(greeting)  # Output: Hello, world!
```

## Operator Precedence
Python follows a specific order of operations, known as operator precedence, to evaluate expressions. The order is as follows (from highest to lowest precedence):
1. Parentheses `()`
2. Exponentiation `**`
3. Multiplication `*`, Division `/`, Floor Division `//`, Modulus `%`
4. Addition `+`, Subtraction `-`
5. Comparison Operators (`==`, `!=`, `>`, `<`, `>=`, `<=`)
6. Logical Operators (`and`, `or`, `not`)
You can use parentheses to change the order of evaluation in an expression. For example:

```python
result = (5 + 3) * 2
print(result)  # Output: 16
```
## Function Calls in Expressions
You can also include function calls within expressions. The function will be evaluated first, and its return value will be used in the expression. For example: 

```python
def square(x):
    return x * x
result = square(4) + 2
print(result)  # Output: 18
```

## Combining Different Types
Python allows you to combine different data types in expressions, but you need to be careful with type compatibility. For example, you can concatenate strings using the `+` operator, but you cannot directly add a string and an integer without converting one of them:

```python
# Valid string concatenation
name = "Alice"
greeting = "Hello, " + name
print(greeting)  # Output: Hello, Alice

# Invalid operation (will raise TypeError)
age = 30
# greeting = "I am " + age  # Uncommenting this line will raise an error
# Correct way using type conversion
greeting = "I am " + str(age)
print(greeting)  # Output: I am 30
```

## Summary
Expressions in Python are a fundamental part of the language, allowing you to perform calculations, manipulate data, and make decisions. Understanding how to construct and evaluate expressions is essential for effective programming in Python.
