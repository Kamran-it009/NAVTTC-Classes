# ✅ Python Programming Topics

## 1. 2D List

A 2D list is a list of lists. It's essentially a matrix with rows and columns, and each element can be accessed using two indices (row and column).

### Definition:
A 2D list is like a table or grid. It’s a list where each item is also a list.  
You can think of it as rows and columns (like in Excel), and you use two indexes to access values.

### Syntax:
```python
list_name = [[element1, element2], [element3, element4]]
```

### Example:
```python
matrix = [[1, 2], [3, 4]]
print(matrix[0][1])  # Output: 2
```

---

## 2. 3D List

A 3D list is an extension of the 2D list. It’s a list of lists of lists. Each element can be accessed with three indices.

### Definition:
A 3D list is like a cube of data. It’s a list that contains lists of lists.  
You can access the values using three indexes, like layers, rows, and columns.

### Syntax:
```python
list_name = [[[element1, element2], [element3, element4]], [[element5, element6], [element7, element8]]]
```

### Example:
```python
cube = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]
print(cube[1][0][1])  # Output: 6
```

---

## 3. Conditional Statements

### if statement

#### Definition:
The `if` statement checks if something is true, and if it is, it runs the block of code.

#### Syntax:
```python
if condition:
    # code to execute
```

#### Example:
```python
x = 10
if x > 5:
    print("x is greater than 5")
```

---

### if-else statement

#### Definition:
The `if-else` statement runs one block of code if the condition is true, and another block if the condition is false.

#### Syntax:
```python
if condition:
    # code to execute if true
else:
    # code to execute if false
```

#### Example:
```python
x = 4
if x > 5:
    print("x is greater than 5")
else:
    print("x is less than or equal to 5")
```

---

### if-else-if (elif) statement

#### Definition:
The `elif` statement allows checking multiple conditions. It’s a way to handle different cases.

#### Syntax:
```python
if condition1:
    # code to execute if condition1 is true
elif condition2:
    # code to execute if condition2 is true
else:
    # code to execute if none of the conditions are true
```

#### Example:
```python
x = 15
if x < 5:
    print("x is less than 5")
elif x < 10:
    print("x is less than 10")
else:
    print("x is 10 or greater")
```

---

## 4. Dictionary

A dictionary is a collection of key-value pairs. It allows you to store data in a way that each item is associated with a unique key.

### Definition:
A dictionary is a mutable, unordered collection of data values in Python.

### Syntax:
```python
dict_name = {key1: value1, key2: value2, ...}
```

### Example:
```python
student = {"name": "Alice", "age": 20, "course": "Computer Science"}
print(student["name"])  # Output: Alice
```

---

## 5. Sets

A set is an unordered collection of unique elements. Sets do not allow duplicate values.

### Definition:
A set is a collection of unordered, unindexed, and unique elements.

### Syntax:
```python
set_name = {element1, element2, ...}
```

### Example:
```python
fruits = {"apple", "banana", "cherry"}
fruits.add("orange")
print(fruits)  # Output: {'banana', 'apple', 'orange', 'cherry'}
```

---

## 6. Tuple

A tuple is an ordered, immutable collection of elements. Unlike lists, tuples cannot be changed once they are created.

### Definition:
A tuple is an immutable collection of ordered elements.

### Syntax:
```python
tuple_name = (element1, element2, ...)
```

### Example:
```python
coordinates = (10, 20)
print(coordinates[0])  # Output: 10
```

---
