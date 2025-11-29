---
title: Array Utilities in Standard Library of Python
linkTitle: Array Utilities
description: Overview of array utility functions available in Python's standard library.
date: 2025-11-27
weight: 10
---

In Python, the standard library provides several utilities for working with arrays. Below are some commonly used array utility functions and methods:

| Function/Method | Description | Example |
|-----------------|-------------|---------|
| `array.array(typecode, initializer)` | Creates a new array with specified type and initial values | `import array`<br>`arr = array.array('i', [1, 2, 3])` |
| `array.append(x)` | Appends an item to the end of the array | `arr.append(4)` |
| `array.extend(iterable)` | Extends the array by appending elements from the iterable | `arr.extend([5, 6])` |
| `array.insert(i, x)` | Inserts an item at a given position | `arr.insert(0, 0)` |
| `array.remove(x)` | Removes the first occurrence of an item | `arr.remove(2)` |
| `array.pop([i])` | Removes and returns item at index i (default last) | `arr.pop()` |
| `array.index(x[, start[, end]])` | Returns the index of the first occurrence of an item | `index = arr.index(3)` |
| `array.count(x)` | Returns the number of occurrences of an item | `count = arr.count(3)` |
| `array.reverse()` | Reverses the order of the array | `arr.reverse()` |
| `array.buffer_info()` | Returns a tuple (address, length) giving the current memory address and length of the array | `info = arr.buffer_info()` |
| `array.tolist()` | Converts the array to a regular Python list | `lst = arr.tolist()` |
| `array.fromlist(list)` | Appends items from the list to the end of the array | `arr.fromlist([7, 8, 9])` |
| `array.tobytes()` | Converts the array to a bytes object | `b = arr.tobytes()` |
| `array.frombytes(bytes)` | Appends items from the bytes object to the end of the array | `arr.frombytes(b)` |
| `array.typecode` | Returns the type code of the array | `typecode = arr.typecode` |
| `array.itemsize` | Returns the size in bytes of one array item | `itemsize = arr.itemsize` |
| `array.buffer_info()` | Returns a tuple (address, length) giving the current memory address and length of the array | `info = arr.buffer_info()` |
| `array.clear()` | Removes all items from the array | `arr.clear()` |

These utilities provide a robust set of tools for manipulating arrays in Python, making it easier to perform various operations efficiently.

## Example Usage

```python
import array

# Create an array of integers
arr = array.array('i', [1, 2, 3, 4, 5])

# Append an element
arr.append(6) #  arr = [1, 2, 3, 4, 5, 6]

# Insert an element at index 0
arr.insert(0, 0) # arr = [0, 1, 2, 3, 4, 5, 6]

# Remove an element
arr.remove(3) # arr = [0, 1, 2, 4, 5, 6]

# Pop the last element
last_element = arr.pop() # arr = [0, 1, 2, 4, 5], last_element = 6

# Convert to list
lst = arr.tolist() # lst = [0, 1, 2, 4, 5]

print("Array:", arr)
print("Last Element:", last_element)
print("List:", lst)

# Output:
# Array: array('i', [0, 1, 2, 4, 5])
# Last Element: 6
# List: [0, 1, 2, 4, 5]
```
