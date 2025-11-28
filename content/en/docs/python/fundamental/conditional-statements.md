---
title: Conditional Statements in Python
linkTitle: Conditional Statements
date: 2025-11-27
weight: 30
---

Conditional statements in Python allow you to execute specific blocks of code based on certain conditions. The primary conditional statements in Python are `if`, `elif`, and `else`.

## `if` Statement
The `if` statement is used to test a condition. If the condition evaluates to `True
`, the block of code inside the `if` statement is executed.

```python
age = 18
if age >= 18:
    print("You are an adult.")

# Output: You are an adult.
```

## `elif` Statement
The `elif` (short for "else if") statement allows you to check multiple conditions.
```python
age = 16
if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
# Output: You are a teenager.
```

## `else` Statement
The `else` statement is used to execute a block of code when none of the previous conditions
are met.
```python
age = 10
if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
# Output: You are a child.
```

## Nested Conditional Statements
You can also nest conditional statements within each other to create more complex decision-making structures.
```python
age = 20
if age >= 18:
    if age >= 65:
        print("You are a senior adult.")
    else:
        print("You are an adult.")
else:
    print("You are a minor.")
# Output: You are an adult.
```

## Switching with `match-case` (Python 3.10+)
Starting from Python 3.10, you can use the `match-case` statement as a more readable alternative to multiple `if-elif-else` statements for certain scenarios.
```python
day = "Monday"
match day:
    case "Monday":
        print("Start of the work week.")
    case "Wednesday":
        print("Midweek day.")
    case "Friday":
        print("End of the work week.") 
    case _:
        print("It's just another day.")
# Output: Start of the work week.
```

## Ternary Conditional Operator
Python also supports a shorthand way of writing conditional statements using the ternary conditional operator.

```python
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)  # Output: Adult
```

## Summary
Conditional statements in Python are essential for controlling the flow of your program based on different conditions. By using `if`, `elif`, and `else`, you can create complex decision-making structures to handle various scenarios in your code.
