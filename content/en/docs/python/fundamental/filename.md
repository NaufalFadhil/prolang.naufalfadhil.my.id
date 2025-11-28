---
title: Filename in Python
linkTitle: Filename
description: Getting started with file name for running Python programs.
date: 2025-11-27
weight: 5
---
In Python, the filename is the name of the file where your Python code is stored. It typically has a `.py` extension. For example, if you create a file named `hello.py`, you can run it using the Python interpreter by executing the following command in your terminal or command prompt:

```bash
python hello.py
```
Make sure to replace `hello.py` with the actual name of your Python file. The filename should be descriptive of the code it contains to make it easier to identify its purpose.
For example, if your file contains code to calculate the area of a circle, you might name it `circle_area.py`.

Here are some best practices for naming Python files:
- Use lowercase letters and underscores to separate words (e.g., `my_script.py`).
- Avoid using special characters or spaces in the filename.
- Keep the filename concise yet descriptive of its content.
- Ensure the filename does not conflict with Python's built-in module names to avoid import issues.
By following these guidelines, you can effectively manage and organize your Python files.

## Example
Here is an example of a simple Python file named `greet.py`:
```python
def greet(name):
    print(f"Hello, {name}!")
greet("World")
```

You can run this file using the command:
```bash
python greet.py
```

This will output:
```
Hello, World!
```

## Summary
The filename in Python is crucial for organizing and running your code. By following naming conventions and best practices, you can ensure that your Python files are easy to manage and understand.
