---
title: Data Types Conversion in Python
linkTitle: Data Types Conversion
date: 2025-11-27
weight: 11
---

In Python, you can convert between different data types using built-in functions. Here are some common conversions:

## Numberic conversions
You can convert between integers and floats using the `int()` and `float()` functions.

### Converting to Integer
You can convert a value to an integer using the `int()` function.
```python
# From float to int
float_value = 10.5
int_value = int(float_value)
print(int_value)  # Output: 10
```

```python
# From string to int
string_value = "20"
int_value = int(string_value)
print(int_value)  # Output: 20
```
### Converting to Float
You can convert a value to a float using the `float()` function.

```python
# From int to float
int_value = 10
float_value = float(int_value)
print(float_value)  # Output: 10.0
```

```python
# From string to float
string_value = "20.5"
float_value = float(string_value)
print(float_value)  # Output: 20.5
```

## String conversions
You can convert other data types to strings using the `str()` function.

### Converting to String
```python
# From int to string
int_value = 10
string_value = str(int_value)
print(string_value)  # Output: "10"
```

```python
# From float to string
float_value = 10.5
string_value = str(float_value)
print(string_value)  # Output: "10.5"
```

## Data Type Transformations
You can also convert between complex data types like lists, tuples, sets, and dictionaries.

### Converting List to Tuple
```python
my_list = [1, 2, 3]
my_tuple = tuple(my_list)
print(my_tuple)  # Output: (1, 2, 3)
```

### Converting Tuple to List
```python
my_tuple = (1, 2, 3)
my_list = list(my_tuple)
print(my_list)  # Output: [1, 2, 3]
```

### Converting List to Set
```python
my_list = [1, 2, 2, 3]
my_set = set(my_list)
print(my_set)  # Output: {1, 2, 3}
```

### Converting Set to List
```python
my_set = {1, 2, 3}
my_list = list(my_set)
print(my_list)  # Output: [1, 2, 3]
```

### Converting Dictionary Keys to List
```python
my_dict = {"a": 1, "b": 2, "c": 3}
keys_list = list(my_dict.keys())
print(keys_list)  # Output: ['a', 'b', 'c']
```

### Converting Dictionary Values to List
```python
my_dict = {"a": 1, "b": 2, "c": 3}
values_list = list(my_dict.values())
print(values_list)  # Output: [1, 2, 3]
```

These conversions are useful when you need to manipulate data in different formats or when interfacing with functions that require specific data types.


