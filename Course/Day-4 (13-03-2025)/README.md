# 🐍 Python Programming

Python is a powerful and versatile programming language that is easy to learn and use. It is widely used for web development (server-side), software development, data analysis, artificial intelligence, system scripting, and more.

---

## 🖨️ `print()` Function in Python
The `print()` function in Python is used to display output on the console. It is one of the most commonly used built-in functions.

### 📌 Syntax
```python
print(value1, value2, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
```

### 🔹 Parameters
- **`value1, value2, ...`**: One or more values to be printed, separated by commas.
- **`sep`** *(optional)*: A string inserted between values, default is a single space `' '`.
- **`end`** *(optional)*: A string added at the end of the print statement, default is a newline `\n`.
- **file** (optional): An object with a write(string) method. Defaults to sys.stdout.
- **flush** (optional): A boolean. If True, the stream is forcibly flushed. Default is False.

### ✅ Examples
```python
# Printing a number (integer)
print(100)  

# Printing a decimal number (float)
print(3.14)  

# Printing multiple values together
print("Age:", 25)  

# Printing different types together
print("Price:", 99.99, "Available:", True)  

# Using a custom separator
print(1, 2, 3, 4, 5, sep=",")  

# Using a custom end
print("Python is", end=" ")
print("Awesome!")  
m end
```
**Output:**
```
Hello
100
3.14
Age: 25
Price: 99.99 Available: True
1,2,3,4,5
Python is Awesome!

```

---

## 💬 Comments in Python
Comments are used to make code more readable and to explain what different parts of the code do. Python ignores comments during execution.

### 📌 Why Use Comments?
- To make the code easier to understand later.
- To turn off some code without deleting it (for testing).
- To help others understand your code when working together.

### 🟢 Single-line Comments
Single-line comments start with `#`. Python ignores everything after `#` on that line.
```python
# This is a single-line comment
print("Python is fun!")
```

### 🟡 Multi-line Comments
Multi-line comments are enclosed within triple quotes (`'''` or `"""`). Everything inside these quotes is ignored by Python.
```python
"""
This is a multi-line comment.
It spans multiple lines.
Python will ignore everything written inside these triple quotes.
"""
```

---

## 📦 Variables and Data Types
A variable is a container for storing data values. Python automatically assigns the type based on the value assigned to the variable.

### 🔹 What Are Variables?
- Variables store data that can be used later in the program.
- We don’t need to specify the type; Python decides it automatically.
- Variable names must start with a letter or `_` (underscore) and cannot contain spaces.

### 🔹 Common Data Types
1. **Integer (`int`)**: Whole numbers without decimals.
   ```python
   x = 10  # Integer
   print(x, type(x))  # Output: 10 <class 'int'>
   ```

2. **Float (`float`)**: Numbers with decimal points.
   ```python
   y = 10.5  # Float
   print(y, type(y))  # Output: 10.5 <class 'float'>
   ```

3. **Boolean (`bool`)**: A data type that can only have two values: `True` or `False`. It is used to represent logical decisions, like `Yes` or `No`.
   ```python
   is_python_easy = True  # Boolean
   print(is_python_easy, type(is_python_easy))  # Output: True <class 'bool'>
   ```

4. **String (`str`)**: A sequence of letters, numbers, or symbols enclosed in quotes. Strings are used to store text.
   ```python
   name = "Python"  # String
   print(name, type(name))  # Output: Python <class 'str'>
   ```

5. **Complex (`complex`)**: A special type of number that has two parts: a real part and an imaginary part (written with j). It is used in advanced mathematics and engineering.
   ```python
   z = 3 + 4j  # Complex number
   print(z, type(z))  # Output: (3+4j) <class 'complex'>
   ```

---

