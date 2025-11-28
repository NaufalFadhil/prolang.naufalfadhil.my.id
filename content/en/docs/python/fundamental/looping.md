---
title: Looping in Python
linkTitle: Looping
date: 2025-11-27
weight: 31
---

In Python, loops are used to execute a block of code repeatedly until a certain condition is met. Python provides two main types of loops: `for` loops and `while` loops.

## `for` Loop
The `for` loop is used to iterate over a sequence (such as a list, tuple, or string) or other iterable objects. It allows you to execute a block of code for each item in the sequence.

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

You can also use the `range()` function to generate a sequence of numbers for iteration:

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

## `while` Loop
The `while` loop is used to execute a block of code as long as a specified condition is `True`. It continues to loop until the condition becomes `False`.

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

## Loop Control Statements
Python provides several control statements to manage the flow of loops:
- `break`: Terminates the loop prematurely.
- `continue`: Skips the current iteration and moves to the next iteration.
- `else`: Executes a block of code once when the loop condition is no longer true.

### Example of `break` and `continue`

```python
# Using break
for i in range(10):
    if i == 5:
        break
    print(i)

# Output:
# 0
# 1
# 2
# 3
# 4

# Using continue
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)

# Output:
# 1
# 3
# 5
# 7
# 9
```

### Example of `else` with loops

```python
# Using else with for loop
for i in range(5):
    print(i)
else:
    print("Loop completed successfully.")
# Output:
# 0
# 1
# 2
# 3
# 4

# Using else with while loop
count = 0
while count < 5:
    print(count)
    count += 1
else:
    print("While loop completed successfully.")

# Output:
# 0
# 1
# 2
# 3
# 4
```

If the `while` loop's condition is never `True` from the start, the `else` block will still execute:

```python
count = 10
while count < 5:
    print(count)
    count += 1
else:
    print("While loop completed successfully.")

# Output:
# While loop completed successfully.
```

## Summary
Loops are essential for performing repetitive tasks in Python. By using `for` and `while` loops, along with control statements like `break`, `continue`, and `else`, you can effectively manage the flow of your programs and handle various iteration scenarios.
