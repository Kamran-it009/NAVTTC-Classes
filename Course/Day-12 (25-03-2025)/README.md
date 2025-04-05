## Decorators, File Handling, and Generators

### **Decorators**

**Definition:**
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

**Example:**
```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def sum():
    print('I am a sum..')

sum()
```

**Output:**
```
Something is happening before the function is called.
I am a sum..
Something is happening after the function is called.
```

---

### **File Handling**

**Definition:**
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

**Example:**
```python
# Reading a file
file = open('data.txt', mode='r')
file_data = file.read()
print(file_data)
file.close()
```

#### **Writing Files**

**Syntax:**
```python
file = open('file_name', mode='w')  # 'w' mode for writing
file.write('Hello, world!')
file.close()
```

**Example:**
```python
# Writing to a file
file = open('output.txt', mode='w')
file.write('Hello, this is a new file.')
file.close()
```

#### **Appending Data in Files**

**Syntax:**
```python
file = open('file_name', mode='a')  # 'a' mode for appending
file.write('New line of text')
file.close()
```

**Example:**
```python
# Appending to a file
file = open('output.txt', mode='a')
file.write('This is an appended line.\n')
file.close()
```

---

### **Generators**

**Definition:**
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

