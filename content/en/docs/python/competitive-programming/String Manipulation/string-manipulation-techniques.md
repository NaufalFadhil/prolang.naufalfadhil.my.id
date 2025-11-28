---
title: String Manipulation Techniques in Python for Competitive Programming
linkTitle: String Manipulation Techniques
date: 2025-11-27
weight: 52
---

## String Manipulation Techniques

### Reversing a String

```python
# Example of reversing a string
word = "hello"
reversed_word = word[::-1]
print(reversed_word)  # Output: olleh
```

### Checking for Substrings

```python
# Example of checking for substrings
word = "hello world"
contains_hello = "hello" in word
print(contains_hello)  # Output: True
```

```python
# Example of checking for substrings using find()
word = "hello world"
index = word.find("world")
if index != -1:
    print("Substring found at index:", index)  # Output: Substring found at index
else:
    print("Substring not found.")
```

### Stripping Whitespace

```python
# Example of stripping whitespace
word = "   hello world   "
stripped_word = word.strip()
print(stripped_word)  # Output: hello world
```

### Using Lambda Functions with Strings

```python
# Example of using lambda functions with strings
# Using lambda to convert a list of strings to uppercase
words = ["hello", "world", "python"]
upper_words = list(map(lambda x: x.upper(), words))
print(upper_words)  # Output: ['HELLO', 'WORLD', 'PYTHON']
```

### Joining Strings

```python
# Example of joining strings
words = ["hello", "world", "from", "python"]
joined_string = " ".join(words)
print(joined_string)  # Output: hello world from python
```

### Repeating Strings

```python
# Example of repeating strings
word = "ha"
repeated_word = word * 3
print(repeated_word)  # Output: hahaha
```
