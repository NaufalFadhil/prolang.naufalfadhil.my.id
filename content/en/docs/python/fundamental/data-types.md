---
title: Data Types in Python
linkTitle: Data Types
date: 2025-11-27
weight: 10
---

Python has several built-in data types that are used to store different kinds of data. Here are some of the most commonly used data types in Python:

## Numeric Types
Python has three main numeric types: `int`, `float`, and `complex`.

### Integer (`int`)
An integer is a whole number, positive or negative, without a decimal point. You can create an integer by simply assigning a whole number to a variable.

```python
my_int = 10
print(my_int)  # Output: 10
print(type(my_int))  # Output: <class 'int'>
```

### Float (`float`)
A float is a number that has a decimal point. You can create a float by assigning a number with a decimal point to a variable.

```python
my_float = 10.5
print(my_float)  # Output: 10.5
print(type(my_float))  # Output: <class 'float'>
```

### Complex (`complex`)
A complex number has a real and an imaginary part, represented as `a + bj`, where `a` is the real part and `b` is the imaginary part.

```python
my_complex = 2 + 3j
print(my_complex)  # Output: (2+3j)
print(type(my_complex))  # Output: <class 'complex'>
```

{{% alert color="secondary" %}}Complex numbers are often used in scientific and engineering applications where calculations involve imaginary numbers. You can access the real and imaginary parts of a complex number using the `.real` and `.imag` attributes, respectively.
{{% /alert %}}

```python
real_part = my_complex.real
imaginary_part = my_complex.imag
print(real_part)        # Output: 2.0
print(imaginary_part)   # Output: 3.0
print(type(my_complex))  # Output: <class 'complex'>
print(type(real_part))   # Output: <class 'float'>
```

## String Type / Text Type
The text type in Python is represented by the `str` class, which is used to store sequences of characters (strings).

```python
my_string = "Hello, World!"
print(my_string)  # Output: Hello, World!
print(type(my_string))  # Output: <class 'str'>
```

## Boolean Type
The boolean type in Python is represented by the `bool` class, which can have one of two values: `True` or `False`.
```python
my_bool = True
print(my_bool)  # Output: True
print(type(my_bool))  # Output: <class 'bool'>
```

## Summary
Python provides a variety of built-in data types to handle different kinds of data, including numeric types (integers, floats, complex numbers), text types (strings), and boolean types. Understanding these data types is essential for effective programming in Python.

### Best Practices for Using Data Types
- Choose the appropriate data type for your variables based on the kind of data you need to store.
- Use descriptive variable names to indicate the type of data they hold.
- Be mindful of type conversions when performing operations involving different data types.