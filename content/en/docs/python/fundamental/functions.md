---
title: Functions in Python
linkTitle: Functions
date: 2025-11-27
weight: 32
---

Functions are reusable blocks of code that perform a specific task. In Python, functions are defined using the `def` keyword, followed by the function name and parentheses `()`.

## Defining a Function
You can define a function using the following syntax:
```python
def function_name(parameters):
    """Docstring describing the function."""
    # Function body
    return value
```

##### Example of a Simple Function

```python
def greet(name):
    """Function to greet a person by name."""
    return f"Hello, {name}!"
# Calling the function
print(greet("Alice"))  # Output: Hello, Alice!
```

## Function Parameters
Functions can take parameters (also known as arguments) that allow you to pass data into the function. Parameters can be of any data type, and you can define multiple parameters separated by commas.

##### Example with Multiple Parameters

```python
def add(a, b):
    """Function to add two numbers."""
    return a + b

# Calling the function
print(add(5, 3))  # Output: 8
```

### Default Parameters
You can also define default values for parameters. If a parameter is not provided when the function is called, the default value will be used.

##### Example Function with Default Parameters

```python
def power(base, exponent=2):
    """Function to calculate the power of a number."""
    return base ** exponent


# Calling the function with and without the exponent parameter
print(power(3))      # Output: 9 (3^2)
print(power(2, 3))   # Output: 8 (2^3)
```


### Default Data Types
You can specify the expected data types for function parameters using type hints. This helps improve code readability and allows for better static analysis.

#### Pattern Define Data Types
```python
def function_name(param1: type1, param2: type2) -> return_type:
    """Docstring describing the function."""
    # Function body
    return value
```

#### Example with Type Hints
```python
def multiply(a: int, b: int) -> int:
    """Function to multiply two integers."""
    return a * b
# Calling the function
print(multiply(4, 5))  # Output: 20
```

### Variable-Length Arguments
Python allows you to define functions that can accept a variable number of arguments using `*args` for positional arguments and `**kwargs` for keyword arguments.

##### Example with Variable-Length Arguments

```python
def summarize(*args, **kwargs):
    """Function to summarize positional and keyword arguments."""
    print("Positional arguments:", args)
    print("Keyword arguments:", kwargs)


# Calling the function
summarize(1, 2, 3, name="Alice", age=30)

# Output:
# Positional arguments: (1, 2, 3)
# Keyword arguments: {'name': 'Alice', 'age': 30}
```

{{% alert title="Python Star Operators (* and **) — Explaination" color="warning" %}}
Python uses star operators to control how arguments are collected and unpacked. They are not pointers (unlike in C). Instead, they determine how arguments are grouped when calling or defining a function.
##### `*` — Positional Argument Collector
When used in function definitions:
```python
def func(*args):
    ...
```
- `*args` collects any number of positional arguments.
- Stored as a tuple.
- Example:
```python
def func(*args):
    print(args)

func(1, 2, 3)
# args = (1, 2, 3)
```

##### `**` — Keyword Argument Collector
When used in function definitions:
```python
def func(**kwargs):
    ...
```
- `**kwargs` collects any number of keyword arguments.
- Stored as a dictionary where:
    - key → argument name
    - value → argument value
{{% /alert %}}

## Lambda Functions
Lambda functions are small anonymous functions defined using the `lambda` keyword. They can take any number of arguments but can only have a single expression.

##### Example of a Lambda Function
```python
# Lambda function to square a number
square = lambda x: x ** 2
print(square(5))  # Output: 25
```

##### Real-World Example of Lambda Function
```python
users = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 19},
    {"name": "Charlie", "age": 30},
]

sorted_users = sorted(users, key=lambda u: u["age"])
print(sorted_users)
# Output: [{'name': 'Bob', 'age': 19}, {'name': 'Alice', 'age': 25}, {'name': 'Charlie', 'age': 30}]
```

##### Using Lambda Functions with Built-in Functions
```python
# Using lambda with the map() function to square a list of numbers
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x ** 2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]
```

```python
# Using lambda with the filter() function to get even numbers from a list
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6]
```

```python
# Using lambda with the sorted() function to sort a list of tuples by the second element
tuples = [(1, 'b'), (2, 'a'), (3, 'c')]
sorted_tuples = sorted(tuples, key=lambda x: x[1])
print(sorted_tuples)  # Output: [(2, 'a'), (1, 'b'), (3, 'c')]
```

```python
# Using lambda with reduce() to calculate the product of a list of numbers
from functools import reduce
numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 24
```

```python
# Using lambda with list comprehension to create a list of squares
numbers = [1, 2, 3, 4, 5]
squared_numbers = [ (lambda x: x ** 2)(x) for x in numbers ]
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]
```

```python
# Using lambda with the min() function to find the tuple with the smallest second element
tuples = [(1, 3), (2, 1), (3, 2)]
min_tuple = min(tuples, key=lambda x: x[1])
print(min_tuple)  # Output: (2, 1)
```

<!-- ## Data Types as Function Parameters
You can pass different data types as parameters to functions, including lists, dictionaries, tuples, and sets.
### Example with Different Data Types
```python
def process_data(data):
    """Function to process different data types."""
    if isinstance(data, list):
        return [item * 2 for item in data]
    elif isinstance(data, dict):
        return {key: value * 2 for key, value in data.items()}
    elif isinstance(data, tuple):
        return tuple(item * 2 for item in data)
    elif isinstance(data, set):
        return {item * 2 for item in data}
# Calling the function with different data types
print(process_data([1, 2, 3]))          # Output: [2, 4, 6]
print(process_data({'a': 1, 'b': 2}))   # Output: {'a': 2, 'b': 4}
print(process_data((1, 2, 3)))          # Output: (2, 4, 6)
print(process_data({1, 2, 3}))          # Output: {2, 4, 6}
``` 

### Pattern Matching in Functions
Python 3.10 introduced structural pattern matching, which allows you to match data structures against specific patterns. You can use the `match` statement within functions to handle different cases based on the input data.
### Example of Pattern Matching in a Function
```python
def describe_value(value):
    """Function to describe the type of value using pattern matching."""
    match value:
        case int():
            return "This is an integer."
        case str():
            return "This is a string."
        case list() if len(value) == 0:
            return "This is an empty list."
        case list():
            return f"This is a list with {len(value)} elements."
        case _:
            return "Unknown type."
# Calling the function with different types of values
print(describe_value(10))            # Output: This is an integer.
print(describe_value("Hello"))       # Output: This is a string.
print(describe_value([]))            # Output: This is an empty list.
print(describe_value([1, 2, 3]))     # Output: This is a list with 3 elements.
print(describe_value(3.14))          # Output: Unknown type.
``` -->

## Best Practices for Defining Functions
- Use descriptive names for functions and parameters to improve code readability.
- Include docstrings to document the purpose and usage of the function.
- Keep functions focused on a single task to enhance maintainability.

## Summary
Functions in Python are powerful tools for organizing and reusing code. They can take parameters, have default values, accept variable-length arguments, and can even be defined as anonymous functions using lambda syntax.
By mastering functions, you can write cleaner, more efficient, and more maintainable code.
