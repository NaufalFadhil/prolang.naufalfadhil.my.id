---
title: Iterating Arrays in Python for Competitive Programming
linkTitle: Iterating Arrays
date: 2025-11-27
weight: 10
---

## Iterating Arrays

### Using `for` Loop

```python
# Example of iterating over an array using for loop
arr = [10, 20, 30, 40, 50]
for element in arr:
    print(element)

# Output:
# 10
# 20
# 30
# 40
# 50
```

### Using `while` Loop

```python
# Example of iterating over an array using while loop
arr = [10, 20, 30, 40, 50]
index = 0
while index < len(arr):
    print(arr[index])
    index += 1

# Output:
# 10
# 20
# 30
# 40
# 50
```

## Alternative Methods for Iterating Arrays

### Using `enumerate()`

```python
# Example of iterating over an array using enumerate()
arr = [10, 20, 30, 40, 50]
for index, element in enumerate(arr):
    print(f'Index: {index}, Element: {element}')

# Output:
# Index: 0, Element: 10
# Index: 1, Element: 20
# Index: 2, Element: 30
# Index: 3, Element: 40
# Index: 4, Element: 50
```

### Using List Comprehension

```python
# Example of iterating over an array using list comprehension
arr = [10, 20, 30, 40, 50]
squared = [element ** 2 for element in arr]
for value in squared:
    print(value)

# Output:
# 100
# 400
# 900
# 1600
# 2500
```

### Using `map()` Function

```python
# Example of iterating over an array using map()
arr = [10, 20, 30, 40, 50]
def square(x):
    return x ** 2
squared = map(square, arr)
for value in squared:
    print(value)

# Output:
# 100
# 400
# 900
# 1600
# 2500
```

### Using `filter()` Function

```python
# Example of iterating over an array using filter()
arr = [10, 15, 20, 25, 30]
def is_even(x):
    return x % 2 == 0
even_numbers = filter(is_even, arr)
for value in even_numbers:
    print(value)

# Output:
# 10
# 20
# 30
```

### Using `zip()` Function

```python
# Example of iterating over two arrays using zip()
arr1 = [1, 2, 3]
arr2 = ['a', 'b', 'c']
for num, char in zip(arr1, arr2):
    print(f'Number: {num}, Character: {char}')
# Output:
# Number: 1, Character: a
# Number: 2, Character: b
# Number: 3, Character: c
```

### Using `itertools.cycle()`

```python
import itertools
# Example of iterating over an array infinitely using itertools.cycle()
arr = [1, 2, 3]
counter = 0
for element in itertools.cycle(arr):
    if counter >= 10:  # Limit to 10 iterations for demonstration
        break
    print(element)
    counter += 1
# Output:
# 1
# 2
# 3
# 1
# 2
# 3
# 1
# 2
# 3
# 1
```

### Using `reversed()` Function

```python
# Example of iterating over an array in reverse order using reversed()
arr = [10, 20, 30, 40, 50]
for element in reversed(arr):
    print(element)
# Output:
# 50
# 40
# 30
# 20
# 10
```
### Using `numpy` Arrays

```python
import numpy as np
# Example of iterating over a numpy array
arr = np.array([10, 20, 30, 40, 50])
for element in arr:
    print(element)
# Output:
# 10
# 20
# 30
# 40
# 50
```

### Using `pandas` Series

```python
import pandas as pd
# Example of iterating over a pandas Series
arr = pd.Series([10, 20, 30, 40, 50])
for element in arr:
    print(element)
# Output:
# 10
# 20
# 30
# 40
# 50
```

### Using `array` Module

```python
import array
# Example of iterating over an array using array module
arr = array.array('i', [10, 20, 30, 40, 50])
for element in arr:
    print(element)
# Output:
# 10
# 20
# 30
# 40
# 50
```
