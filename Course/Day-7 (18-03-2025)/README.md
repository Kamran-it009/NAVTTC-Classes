# 📘 Lists and Strings in Python  
## 🔤 Strings

### 📌 What is a String?
A **string** is a sequence of characters (letters, numbers, or symbols) enclosed in quotes. Strings are **immutable**, meaning you cannot change their characters directly after creation.

> A string is just text – like your name, a sentence, or any word.

---

### 🧱 Syntax
```python
string_name = 'Your text here'
```
You can use single `'` or double `"` quotes.

---

### ✅ Example
```python
name = 'Muhammad Kamran Khan'
print(name)
```
**Output:**
```
Muhammad Kamran Khan
```

---

### 🔢 Indexing (Accessing Characters)

#### 📘 Definition:
**Indexing** means accessing individual characters of a string using their position (index).  
In Python, indexing starts at **0** (zero-based indexing).

#### 🔹 Example:
```python
text = 'Python'
print(text[0])   # First character
print(text[2])   # Third character
```
**Output:**
```
P  
t
```

---

### 🔁 Negative Indexing

#### 📘 Definition:
**Negative indexing** allows you to access characters from the **end of the string**.  
- `-1` refers to the **last character**
- `-2` is second to last, and so on.

#### 🔹 Example:
```python
text = 'Python'
print(text[-1])  # Last character
print(text[-3])  # Third from the end
```
**Output:**
```
n  
h
```

---

### ✂️ Slicing Strings

#### 📘 Definition:
**Slicing** is used to get a part (or "slice") of the string using a range of indexes.

#### 🔹 Syntax:
```python
string[start:end]
```

- `start`: index where the slice begins (included)
- `end`: index where the slice ends (excluded)
- If `start` is omitted, slicing starts from 0.
- If `end` is omitted, slicing goes till the end.

#### 🔹 Example:
```python
text = 'Python Programming'
print(text[0:6])   # Characters from index 0 to 5
print(text[:6])    # Same as above
print(text[7:])    # From index 7 to the end
```
**Output:**
```
Python  
Python  
Programming
```

---

### 🧰 String Methods (with Examples)

| Method       | Description                              | Example                             | Output                        |
|--------------|------------------------------------------|-------------------------------------|-------------------------------|
| `upper()`    | Converts all characters to uppercase     | `text.upper()`                      | `'PYTHON PROGRAMMING'`       |
| `lower()`    | Converts all characters to lowercase     | `text.lower()`                      | `'python programming'`       |
| `replace()`  | Replaces part of the string              | `text.replace('Python', 'Java')`    | `'Java Programming'`         |
| `find()`     | Finds position of a substring            | `text.find('Pro')`                  | `7`                          |
| `split()`    | Splits the string into a list            | `text.split()`                      | `['Python', 'Programming']`  |

---

#### ✅ Short Example
```python
text = 'Python Programming'
print(text.upper())
print(text.replace('Python', 'Java'))
print(text.split())
```

**Output:**
```
PYTHON PROGRAMMING  
Java Programming  
['Python', 'Programming']
```

---

## 🔢 Lists

### 📌 What is a List?
A **list** is a collection that stores multiple items in one variable. Lists are **ordered**, **changeable (mutable)**, and can hold **different types** of values like numbers, strings, or even other lists.

> Think of a list as a grocery basket where you can add, remove, or replace any item.

---

### 🧱 Syntax
```python
list_name = [item1, item2, item3, ...]
```

- `list_name`: any variable name  
- Items are separated by commas  
- Square brackets `[]` define the list

---

### ✅ Example
```python
fruits = ['apple', 'banana', 'cherry', 'mango']
print(fruits)
print(type(fruits))
```
**Output:**
```
['apple', 'banana', 'cherry', 'mango']  
<class 'list'>
```

---

### ✏️ Updating a List
You can change an item by accessing it through its index.

```python
fruits[1] = 'blueberry'
print(fruits)
```
**Output:**
```
['apple', 'blueberry', 'cherry', 'mango']
```

---

### 🧰 Common List Methods (with Examples)

| Method       | Description                            | Example                             | Output                          |
|--------------|----------------------------------------|-------------------------------------|---------------------------------|
| `append()`   | Adds item at the end                   | `fruits.append('grape')`            | `['apple', ..., 'grape']`       |
| `insert()`   | Adds item at specific index            | `fruits.insert(1, 'kiwi')`          | `'kiwi'` is added at index 1    |
| `remove()`   | Removes first matching item            | `fruits.remove('apple')`            | `'apple'` is removed            |
| `pop()`      | Removes item at given index (default last) | `fruits.pop()`                   | removes last item               |
| `sort()`     | Sorts the list in ascending order      | `fruits.sort()`                     | sorted list                     |
| `reverse()`  | Reverses the list                      | `fruits.reverse()`                  | reversed list                   |

#### 🔹 Example
```python
numbers = [5, 2, 9, 1]
numbers.sort()
print(numbers)
```
**Output:**
```
[1, 2, 5, 9]
```
