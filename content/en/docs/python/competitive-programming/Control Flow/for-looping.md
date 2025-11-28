---
title: For Looping in Python for Competitive Programming
linkTitle: For Looping
date: 2025-11-27
weight: 30
---

## `for` Loop

### Iterating over a `list`

```python
# Example of a for loop iterating over a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Output:
# apple
# banana
# cherry
```

### Iterating using `range()`

```python
# Example of a for loop using range()
for i in range(5):
    print(i)

# Output:
# 0
# 1
# 2
# 3
# 4
```


### Iterating using `len()`

```python
# Example of a for loop using len() and range()
fruits = ["apple", "banana", "cherry"]
for i in range(len(fruits)):
    print(i, fruits[i])
# Output:
# 0 apple
# 1 banana
# 2 cherry      
```

### Iterating over a `string`

```python
# Example of a for loop iterating over a string
word = "hello"
for letter in word:
    print(letter)
# Output:
# h
# e
# l
# l
# o
```

### Iterating over a `dictionary`

```python
# Example of a for loop iterating over a dictionary
person = {"name": "Alice", "age": 30, "city": "New York"}
for key in person:
    print(key, ":", person[key])
# Output:
# name : Alice
# age : 30
# city : New York   
```

### Iterating with `enumerate()`

```python
# Example of a for loop using enumerate()
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(index, fruit)

# Output:
# 0 apple
# 1 banana
# 2 cherry
```

### Iterating with `zip()`

```python
# Example of a for loop using zip()
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]
for name, age in zip(names, ages):
    print(name, "is", age, "years old.")

# Output:
# Alice is 25 years old.
# Bob is 30 years old.
# Charlie is 35 years old.
```

### Iterating with `reversed()`

```python
# Example of a for loop using reversed()
numbers = [1, 2, 3, 4, 5]
for num in reversed(numbers):
    print(num)

# Output:
# 5
# 4
# 3
# 2
# 1
```

### Iterating with `sorted()`

```python
# Example of a for loop using sorted()
numbers = [5, 2, 9, 1, 5, 6]
for num in sorted(numbers):
    print(num)
# Output:
# 1
# 2
# 5
# 5
# 6
# 9
```
