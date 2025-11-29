---
title: Inserting Arrays in Python for Competitive Programming
linkTitle: Inserting Arrays
date: 2025-11-27
weight: 30
---

## Inserting Arrays

### Using _sliding window_ to insert elements

```python
# Example of inserting elements into an array using sliding window
def insert_elements(arr, to_insert):
    result = arr.copy()
    for element in to_insert:
        result.append(element)
    return result
arr = [10, 20, 30]
to_insert = [40, 50]
new_arr = insert_elements(arr, to_insert)
print(new_arr)

# Output:
# [10, 20, 30, 40, 50]
```

### Using `.append()`

```python
# Example of inserting an element at *** the end of an array *** using append()
arr = [10, 20, 30]
arr.append(40)
print(arr)

# Output:
# [10, 20, 30, 40]
```

### Using `.insert()`

```python
# Example of inserting an element at a *** specific index *** using insert()
arr = [10, 20, 30]
arr.insert(1, 15)  # Insert 15 at index 1
print(arr)

# Output:
# [10, 15, 20, 30]
```
### Using `.extend()`

```python
# Example of inserting multiple elements at the *** end of an array *** using extend()
arr = [10, 20, 30]
arr.extend([40, 50, 60])
print(arr)

# Output:
# [10, 20, 30, 40, 50, 60]
```

### Using Slicing `[:]`

```python
# Example of inserting elements using slicing
arr = [10, 20, 30]
arr[1:1] = [15, 17]  # Insert 15 and
print(arr)
# Output:
# [10, 15, 17, 20, 30]
```

### Using `+` Operator

```python
# Example of inserting elements using the + operator
arr = [10, 20, 30]
arr = arr[:1] + [15, 17] + arr[1:]
print(arr)
# Output:
# [10, 15, 17, 20, 30]
```

### Using `numpy.insert()`

```python
import numpy as np
# Example of inserting elements in a numpy array
arr = np.array([10, 20, 30])
new_arr = np.insert(arr, 1, [15, 17])  # Insert
print(new_arr)
# Output:
# [10 15 17 20 30]
```

### Using `pandas.Series.insert()`

```python
import pandas as pd
# Example of inserting elements in a pandas Series
arr = pd.Series([10, 20, 30])
arr = arr.append(pd.Series([15, 17]), ignore_index=True)
arr = arr.sort_index().reset_index(drop=True)
print(arr)
# Output:
# 0    10
# 1    15
# 2    17
# 3    20
# 4    30
# dtype: int64
```

## Conclusion
Inserting elements into arrays is a common operation in competitive programming. Python provides multiple methods to achieve this, including built-in list methods like `append()`, `insert()`, and `extend()`, as well as slicing techniques. For more advanced use cases, libraries like `numpy` and `pandas` offer additional functionality for array manipulation.
