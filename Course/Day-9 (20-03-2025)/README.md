# ✅ Loops and Nested Conditions in Python 
## 🔁 What is a Loop?

A **loop** is used to run a block of code **again and again** until a certain condition is met.Think of it like repeating something until you're told to stop.

---

## 1️⃣ While Loop

A while loop keeps doing something as long as a condition is true. It checks the condition before each run, and if it’s false, the loop stops.

### 🔤 Syntax:
```python
while condition:
    # do something
```

- `condition`: A true/false check. If true → loop runs. If false → loop stops.

### ✅ Example:
```python
count = 0
while count < 3:
    print("Count:", count)
    count += 1
```
**Output:**
```
Count: 0  
Count: 1  
Count: 2
```

---

## 2️⃣ For Loop

A for loop is used to go through each item in a group (like a list or string) one by one, and do something with each item.

### 🔤 Syntax:
```python
for item in iterable:
    # do something
```

- `item`: Each value in the sequence
- `iterable`: The collection you're looping through

### ✅ Example:
```python
for fruit in ['apple', 'banana', 'cherry']:
    print(fruit)
```
**Output:**
```
apple  
banana  
cherry
```

---

## 3️⃣ Nested Loop

A nested loop means a loop inside another loop. The inner loop runs completely every time the outer loop runs once.

### ✅ Example:
```python
for x in range(1, 3):
    for y in range(1, 4):
        print(f"x = {x}, y = {y}")
```
**Output:**
```
x = 1, y = 1  
x = 1, y = 2  
x = 1, y = 3  
x = 2, y = 1  
x = 2, y = 2  
x = 2, y = 3
```

---

## 4️⃣ List Comprehension

List comprehension is a short and smart way to create a new list by looping through something and changing or filtering the items.

### 🔤 Syntax:
```python
[expression for item in iterable if condition]
```

### ✅ Example:
```python
squares = [x**2 for x in range(5)]
print(squares)
```
**Output:**
```
[0, 1, 4, 9, 16]
```

---

## 5️⃣ Iterables

An **iterable** is anything you can loop through, like a list, string, or dictionary.

### ✅ Example:
```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
```
**Output:**
```
apple  
banana  
cherry
```

---

## 🌐 Nested Conditions in Python

### 📘 What is a Condition?
A **condition** checks whether something is true or false. We use `if`, `else`, and `elif` to make decisions in our code.

---

## 1️⃣ Nested Conditions

A **nested condition** is when one `if` statement is **inside another**. Useful when one condition depends on another.

### ✅ Example:
```python
english = 'pass'
math = 'fail'

if english == 'pass':
    print("You passed English")
    if math == 'pass':
        print("Promoted!")
    else:
        print("Try again in Math")
else:
    print("You are not eligible")
```
**Output:**
```
You passed English  
Try again in Math
```

---

## 2️⃣ Shortcut of if-else (Ternary Operator)

A shortcut of if-else lets you write a quick decision in one line. It’s useful when you just want to check something and give one of two answers.

```python
value_if_true if condition else value_if_false
```

### ✅ Example:
```python
num = 5
print("Positive") if num >= 0 else print("Negative")
```
**Output:**
```
Positive
```
