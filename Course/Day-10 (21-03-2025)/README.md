# 🧠 Exception Handling & Functions in Python 
## ⚠️ Exception Handling in Python

### 📘 What is Exception Handling?

**Definition (Simple):**  
Exception handling is a way to **stop your program from crashing** when something goes wrong.  
It lets you **catch errors** and handle them **nicely**, so the program can keep going.

> For example: If someone tries to divide a number by 0 — normally that would crash the program. But with exception handling, you can show a message like “You can’t divide by zero!”

---

## 1️⃣ Try-Except Block

### 🔤 Syntax:
```python
try:
    # Code that might cause an error
except ErrorType:
    # Code to run if there's an error
```

### ✅ Example:
```python
try:
    x = 5 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")
```

**Output:**
```
You can't divide by zero!
```

---

### 🧱 Multiple Except Blocks

You can check for more than one type of error:

```python
try:
    value = int(input("Enter a number: "))
    result = 10 / value
except ZeroDivisionError:
    print("Cannot divide by zero.")
except ValueError:
    print("Invalid input! Please enter a number.")
```

---

## 2️⃣ Finally Block

### 📘 Definition:
The finally block is a part of exception handling in Python that always runs, no matter what.
It runs whether there is an error or not.
It’s usually used to clean up—like closing files or ending connections—even if an error happens.

> Use it when you want to make sure something gets done at the end.

### ✅ Example:
```python
try:
    file = open("data.txt", "r")
finally:
    file.close()
    print("File closed.")
```

**Output:**
```
File closed.
```

---

## 3️⃣ Raising Exceptions

### 📘 Definition:
Raising an exception means you manually stop the program and show an error if something isn’t right.
You use the raise keyword to do this.

> Use it when you want to create your own error messages if certain conditions aren't met.

### ✅ Example:
```python
x = -5
if x < 0:
    raise ValueError("Negative value not allowed!")
```

**Output:**
```
ValueError: Negative value not allowed!
```

# 🧩 Functions in Python


### 📘 What is a Function?

**Definition (Simple):**  
A function is a block of code that does a specific job.
You define it once using the def keyword, and then you can call it whenever needed.
Functions help you reuse code, make your programs organized, and avoid repetition.

> Think of a function like a recipe: give it ingredients (input), follow the steps (code), and get a dish (output).

---

### 🔤 Syntax:
```python
def function_name():
    # code block
```

---

### ✅ Example 1: Function without Parameters
```python
def greet():
    print("Hello, student!")

greet()
```

**Output:**
```
Hello, student!
```

---

### ✅ Example 2: Function with Parameters
```python
def greet(name):
    print(f"Hello, {name}!")

greet("Ali")
```

**Output:**
```
Hello, Ali!
```

---

### ✅ Example 3: Function that Returns a Value
```python
def add(x, y):
    return x + y

result = add(5, 3)
print("Sum:", result)
```

**Output:**
```
Sum: 8
```
