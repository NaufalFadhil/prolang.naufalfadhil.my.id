---
title: Operators in Python
linkTitle: Operators
date: 2025-11-27
weight: 21
---

In Python, an expression is a combination of values, variables, operators, and function calls that can be evaluated to produce a result. Expressions are used to perform calculations, manipulate data, and make decisions in your code.

## Basic Operators
Python provides a variety of operators to perform different operations. Here are some of the most commonly used operators:

| Operator | Description               | Example          | Output  |
|----------|---------------------------|------------------|---------|
| `+`      | Addition                  | `5 + 3`          | `8`     |
| `-`      | Subtraction               | `5 - 3`          | `2`     |
| `*`      | Multiplication            | `5 * 3`          | `15`    |
| `/`      | Division                  | `5 / 2`          | `2.5`   |
| `//`     | Floor Division            | `5 // 2`         | `2`     |
| `%`      | Modulus (Remainder)      | `5 % 2`          | `1`     |
| `**`     | Exponentiation            | `5 ** 2`         | `25`    |


You can use these operators in expressions to perform calculations. For example:

```python
result = 5 + 3 * 2
print(result)  # Output: 11
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