## Decorators, File Handling, and Generators

### **Decorators**

Decorators in Python are a way to modify or enhance the behavior of a function or method. They allow you to wrap another function in order to extend its behavior without permanently modifying it.

**Syntax:**
```python
def decorator_name(func):
    def wrapper():
        # Do something before the function is called
        func()
        # Do something after the function is called
    return wrapper

@decorator_name
def function_to_decorate():
    # Function logic here
```

**Parameters:**
- `func`: The function that will be passed to the decorator for modification.

---

### **File Handling**

File handling in Python refers to reading from, writing to, and appending data in files. Python provides built-in functions to handle file operations.

#### **Reading Files**

**Syntax:**
```python
file = open('file_name', mode='r')
content = file.read()  # Read the entire file
line = file.readline()  # Read a single line
lines = file.readlines()  # Read all lines into a list
file.close()  # Always close the file after use
```

**Parameters:**
- `mode`: Determines the mode in which the file is opened, e.g., `'r'` for reading, `'w'` for writing, `'a'` for appending.
- `content`: The data read from the file.

**File Modes Table:**

| Mode | Description | File Pointer Position | File Must Exist? | Creates New File If Not Exists? |
|------|-------------|------------------------|------------------|-------------------------------|
| 'r'  | Read mode – Opens a file for reading. | Beginning | Yes | No |
| 'w'  | Write mode – Opens a file for writing. Overwrites if file exists. | Beginning | No | Yes |
| 'a'  | Append mode – Opens a file for appending. Data is added to the end. | End | No | Yes |
| 'x'  | Exclusive creation – Creates a new file, fails if the file exists. | Beginning | No | Yes (only if it doesn't exist) |
| 'r+' | Read and write mode – Opens a file for both reading and writing. | Beginning | Yes | No |
| 'w+' | Write and read mode – Opens a file for both writing and reading. Overwrites file. | Beginning | No | Yes |
| 'a+' | Append and read mode – Opens a file for both appending and reading. | End | No | Yes |
| 'x+' | Exclusive creation for read and write – Creates a file and opens it. | Beginning | No | Yes (only if it doesn't exist) |

**Notes:**
- You can add `'b'` (binary) or `'t'` (text, default) to any mode, e.g. `'rb'`, `'wb'`, etc.
- Always close the file after use, or use a `with open(...) as f:` block to auto-close.

---

### **Generators**

Generators in Python are a type of iterable, like lists or tuples, but instead of holding all values in memory, they generate values on the fly using the `yield` keyword. This makes them memory efficient.

**Syntax:**
```python
def generator_function():
    yield value
```

**Parameters:**
- `value`: The value that is generated at each iteration.

**Example:**
```python
fruits = ['apple', 'banana', 'cherry', 'mango']
gen = iter(fruits)  # Creating an iterator object
print(next(gen))  # 'apple'
print(next(gen))  # 'banana'
```

**Output:**
```
apple
banana
```

---
