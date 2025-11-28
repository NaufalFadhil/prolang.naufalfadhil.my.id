---
title: While Looping in Python for Competitive Programming
linkTitle: While Looping
date: 2025-11-27
weight: 31
---

## `while` Loop

### Iterating with a condition
```python
# Example of a while loop
count = 0
while count < 5:
    print(count)
    count += 1

# Output:
# 0
# 1
# 2
# 3
# 4
```

### Iterating over a `list` using a `while` loop

```python
# Example of a while loop iterating over a list
fruits = ["apple", "banana", "cherry"]
index = 0
while index < len(fruits):
    print(fruits[index])
    index += 1

# Output:
# apple
# banana
# cherry
```

### Iterating until a specific condition is met

```python
# Example of a while loop until a specific condition is met
number = 0
while True:
    print(number)
    number += 1
    if number >= 5:
        break
        
# Output:
# 0
# 1
# 2
# 3
# 4
```

### Iterating with a sentinel value

```python
# Example of a while loop with a sentinel value
data = [10, 20, 30, -1, 40, 50]
index = 0
while index < len(data):
    if data[index] == -1:
        break
    print(data[index])
    index += 1

# Output:
# 10
# 20
# 30
```