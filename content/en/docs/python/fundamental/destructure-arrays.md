---
title: Destructuring Arrays in Python using Looping
linkTitle: Destructuring Arrays
date: 2025-11-27
weight: 32
---

## Destructuring Arrays

In Python, destructuring (or unpacking) allows you to assign elements of an array (list or tuple) to multiple variables in a single statement. This can be particularly useful when working with arrays of fixed sizes.

### Using `for` Loop

```python
# Example of destructuring arrays using for loop
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]
for number, letter in pairs:
    print(f'Number: {number}, Letter: {letter}')

# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```

### Using `while` Loop

```python
# Example of destructuring arrays using while loop
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]
index = 0
while index < len(pairs):
    number, letter = pairs[index]
    print(f'Number: {number}, Letter: {letter}')
    index += 1

# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```

## Alternative Methods for Destructuring Arrays

### Using List Comprehension

```python
# Example of destructuring arrays using list comprehension
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]
destructured = [f'Number: {number}, Letter: {letter}' for number, letter in pairs]
for item in destructured:
    print(item)

# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```

### Using `map()` Function

```python
# Example of destructuring arrays using map()
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]
def format_pair(pair):
    number, letter = pair
    return f'Number: {number}, Letter: {letter}'
formatted_pairs = map(format_pair, pairs)
for item in formatted_pairs:
    print(item)

# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```

### Using `zip()` Function

```python
# Example of destructuring arrays using zip()
numbers = [1, 2, 3]
letters = ['a', 'b', 'c']
for number, letter in zip(numbers, letters):
    print(f'Number: {number}, Letter: {letter}')
# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```

### Using `enumerate()` Function

```python
# Example of destructuring arrays using enumerate()
letters = ['a', 'b', 'c']
for index, letter in enumerate(letters):
    print(f'Index: {index}, Letter: {letter}')
# Output:
# Index: 0, Letter: a
# Index: 1, Letter: b
# Index: 2, Letter: c
```
### Using `itertools.starmap()`

```python
import itertools
# Example of destructuring arrays using itertools.starmap()
pairs = [(1, 'a'), (2, 'b'), (3, 'c)]
def format_pair(number, letter):
    return f'Number: {number}, Letter: {letter}'
formatted_pairs = itertools.starmap(format_pair, pairs)
for item in formatted_pairs:
    print(item)

# Output:
# Number: 1, Letter: a
# Number: 2, Letter: b
# Number: 3, Letter: c
```
