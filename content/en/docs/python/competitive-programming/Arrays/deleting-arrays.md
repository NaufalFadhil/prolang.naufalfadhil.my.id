---
title: Deleting Arrays in Python for Competitive Programming
linkTitle: Deleting Arrays
date: 2025-11-27
weight: 31
---

## Deleting Arrays

### Using _sliding window_ to delete elements

```python
# Example of deleting elements from an array using sliding window
def delete_elements(arr, to_delete):
    result = []
    for element in arr:
        if element not in to_delete:
            result.append(element)
    return result
arr = [10, 20, 30, 40, 50]
to_delete = [20, 40]
new_arr = delete_elements(arr, to_delete)
print(new_arr)

# Output:
# [10, 30, 50]
```

### Using `.del` Statement

```python
# Example of deleting an element at a specific index using del
arr = [10, 20, 30, 40, 50]
del arr[2]  # Delete element at index 2
print(arr)

# Output:
# [10, 20, 40, 50]
```

### Using `.remove()`

```python
# Example of deleting an element by value using remove()
arr = [10, 20, 30, 40, 50]
arr.remove(30)  # Remove the first occurrence of value 30
print(arr)

# Output:
# [10, 20, 40, 50]
```

### Using `.pop()`

```python
# Example of deleting an element at a specific index using pop()
arr = [10, 20, 30, 40, 50]
removed_element = arr.pop(2)  # Remove and return element at index 2
print(arr)
print("Removed element:", removed_element)

# Output:
# [10, 20, 40, 50]
# Removed element: 30
```

### Using Slicing `[:]`

```python
# Example of deleting multiple elements using slicing
arr = [10, 20, 30, 40, 50]
arr[1:3] = []  # Delete elements from index 1 to 2
print(arr)

# Output:
# [10, 40, 50]
```

### Using `.clear()`

```python
# Example of deleting all elements in the array using clear()
arr = [10, 20, 30, 40, 50]
arr.clear()  # Remove all elements
print(arr)

# Output:
# []
```

### Using `.numpy.delete()`

```python
import numpy as np
# Example of deleting elements in a numpy array
arr = np.array([10, 20, 30, 40, 50])
new_arr = np.delete(arr, 2)  # Delete element at index 2
print(new_arr)
# Output:
# [10 20 40 50]
```

### Using `pandas` DataFrame `.drop()`

```python
import pandas as pd
# Example of deleting rows in a pandas DataFrame
df = pd.DataFrame({'A': [10, 20, 30], 'B
: [40, 50, 60]})
df = df.drop(1)  # Delete row with index 1
print(df)
# Output:
#     A   B
# 0  10  40
# 2  30  60
```

### Using `pandas` Series `.drop()`

```python
import pandas as pd
# Example of deleting elements in a pandas Series
arr = pd.Series([10, 20, 30, 40, 50])
arr = arr.drop(2)  # Delete element at index 2
print(arr)
# Output:
# 0    10
# 1    20
# 3    40
# 4    50
```
