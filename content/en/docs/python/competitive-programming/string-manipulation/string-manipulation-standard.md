---
title: String Manipulation with Standard Library in Python for Competitive Programming
linkTitle: String Manipulation with Standard Library
date: 2025-11-27
weight: 51
---

## String Operations using Standard Library

### Uppercase Strings (`upper()` Method)

```python
# Example of using string methods
word = "hello world"
upper_word = word.upper()
print(upper_word)  # Output: HELLO WORLD
```

### Lowercase Strings (`lower()` Method)

```python
# Example of using string methods
word = "HELLO WORLD"
lower_word = word.lower()
print(lower_word)  # Output: hello world
```

### Capitalizing Strings (`capitalize()` Method)

```python
# Example of using string methods
word = "hello world"
capitalized_word = word.capitalize()
print(capitalized_word)  # Output: Hello world
```

### Title Case Strings (`title()` Method)

```python
# Example of using string methods
sentence = "this is a sample sentence."
title_sentence = sentence.title()
print(title_sentence)  # Output: This Is A Sample Sentence.
```

### Finding Substrings (`find()` Method)

```python
# Example of using string methods
word = "hello world"
index = word.find("world")
print(index) # Output: 6 

# 'world' starts at index 6
```

### Common String Operations (`len()`, `replace()` Methods)

```python
# Example of common string operations
word = "hello world"
length = len(word)
print(length)  # Output: 11

replaced_word = word.replace("world", "there")
print(replaced_word)  # Output: hello there
```

### Splitting and Joining Strings (`split()`, `join()` Methods)

```python
# Example of splitting and joining strings
sentence = "This is a sample sentence."
words = sentence.split(" ")
print(words)  # Output: ['This', 'is', 'a', 'sample', 'sentence.']

joined_sentence = " ".join(words)
print(joined_sentence)  # Output: This is a sample sentence.
```