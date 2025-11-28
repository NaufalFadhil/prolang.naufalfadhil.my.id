---
title: Data Types Collection in Python
linkTitle: Data Types Collection
date: 2025-11-27
weight: 12
---

Python provides several built-in data types to store collections of data. The most commonly used collection data types are: lists, dictionaries, tuples, and sets.

## List
In Python, a list is an ordered collection of items that can be of different types. Lists are mutable, meaning you can change their content after creation. You can create a list using square brackets `[]`.

```python
my_list = [1, "hello", 3.14, True]
print(my_list)  # Output: [1, 'hello', 3.14, True]
print(type(my_list))  # Output: <class 'list'>
```

## Dictionary
A dictionary in Python is an unordered collection of key-value pairs. Dictionaries are mutable and can store values of any data type. You can create a dictionary using curly braces `{}`.

```python
my_dict = {"name": "Alice", "age": 30, "is_student": False}
print(my_dict)  # Output: {'name': 'Alice', 'age': 30, 'is_student': False}
print(type(my_dict))  # Output: <class 'dict'>
```

## Tuple
A tuple is an ordered collection of items that can be of different types, similar to a list. However, tuples are immutable, meaning once they are created, their content cannot be changed. You can create a tuple using parentheses `()`.

```python
my_tuple = (1, "hello", 3.14, True)
print(my_tuple)  # Output: (1, 'hello', 3.14, True)
print(type(my_tuple))  # Output: <class 'tuple'>
```

## Set
A set is an unordered collection of unique items. Sets are mutable, but they do not allow duplicate values. You can create a set using curly braces `{}` or the `set()` function.

```python
my_set = {1, 2, 3, 4, 4}
print(my_set)  # Output: {1, 2, 3, 4}
print(type(my_set))  # Output: <class 'set'>
```
