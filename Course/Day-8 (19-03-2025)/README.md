# ✅ Python Programming Topics

## 1. 2D List

### Definition:
A 2D list is a list where each item is another list, forming a table-like structure with rows and columns that can be accessed using two indexes (like in Excel).

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

### Definition:
A 3D list is a list that contains lists of lists, forming a cube-like structure where elements are accessed using three indexes (layers, rows, and columns).

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

### Definition:
A dictionary is a mutable, unordered collection in Python that stores data as key-value pairs, where each key is unique.

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

### Definition:
A set is an unordered and unindexed collection of unique elements that automatically removes duplicates.

### Uses of Sets:

✅ To remove duplicates from a list

✅ To perform mathematical operations like union, intersection, and difference

✅ To check membership quickly using in

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

### Definition:
A tuple is an ordered collection of elements that cannot be changed (immutable) once created.

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
