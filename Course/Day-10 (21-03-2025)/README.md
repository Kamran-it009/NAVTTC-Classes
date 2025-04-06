# 🧠 Exception Handling & Functions in Python 
## ⚠️ Exception Handling in Python

### 📘 What is Exception Handling?
 
Exception handling is a way to **stop your program from crashing** when something goes wrong.  
It lets you **catch errors** and handle them **nicely**, so the program can keep going.

> For example: If someone tries to divide a number by 0 — normally that would crash the program. But with exception handling, you can show a message like “You can’t divide by zero!”

---

## 1⃣ Try-Except Block

### 🔤 Syntax:
```python
try:
    # Code that might cause an error
except ErrorType:
    # Code to run if there's an error
```

---

### 🧱 try, except, else, finally Block

Python allows combining different parts in one exception handling structure:

```python
try:
    # Code that might cause an error
except ErrorType:
    # Runs if there is a matching error
else:
    # Runs if no error occurs in try block
finally:
    # Always runs, no matter what
```

**Components:**
- **`try:`** The main code you think might crash
- **`except:`** Runs only if an error happens
- **`else:`** Runs if everything inside try worked fine
- **`finally:`** Runs no matter what – great for cleanup

---

## 2⃣ Finally Block

### 📘 Definition:
The finally block is a part of exception handling in Python that always runs, no matter what.
It runs whether there is an error or not.
It’s usually used to clean up—like closing files or ending connections—even if an error happens.

> Use it when you want to make sure something gets done at the end.

---

## 3⃣ Raising Exceptions

### 📘 Definition:
Raising an exception means you manually stop the program and show an error if something isn’t right.
You use the `raise` keyword to do this.

> Use it when you want to create your own error messages if certain conditions aren't met.

---

# 🧹 Functions in Python

### 📘 What is a Function?

A function is a block of code that does a specific job.
You define it once using the `def` keyword, and then you can call it whenever needed.
Functions help you reuse code, make your programs organized, and avoid repetition.

> Think of a function like a recipe: give it ingredients (input), follow the steps (code), and get a dish (output).

---

### 🔤 Syntax:
```python
def function_name():
    # code block
```

---

