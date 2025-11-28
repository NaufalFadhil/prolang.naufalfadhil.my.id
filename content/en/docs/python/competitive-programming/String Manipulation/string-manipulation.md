---
title: String Manipulation in Python for Competitive Programming
linkTitle: String Manipulation
date: 2025-11-27
weight: 50
---

## Basic String Operations

### Accessing Characters in a String

```python
# Example of accessing characters in a string
word = "hello"
first_letter = word[0]
print(first_letter)  # Output: h
```

### Slicing Strings

```python
# Example of slicing a string
word = "hello"
substring = word[1:4]
print(substring)  # Output: ell
```

### Concatenating Strings

```python
# Example of concatenating strings
greeting = "Hello"
name = "Alice"
full_greeting = greeting + ", " + name + "!"
print(full_greeting)  # Output: Hello, Alice!
```

### Formatting Strings

```python
# Example of formatting strings
name = "Bob"
age = 25
formatted_string = f"My name is {name} and I am {age} years old."
print(formatted_string)  # Output: My name is Bob and I am 25 years old.
```

```python
# Example of formatting strings
name = "Alice"
score = 95.5
formatted_string = "Name: {}, Score: {:.2f}".format(name, score)
print(formatted_string)  # Output: Name: Alice, Score: 95.50
```