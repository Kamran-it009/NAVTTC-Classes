# Async Functions & OOP

### **Synchronous Programming**

Synchronous programming refers to the execution model where tasks are performed one after another. Each operation waits for the previous one to complete before starting. This can lead to inefficiencies, especially in I/O-bound tasks.

**Syntax:**
```python
def function_name():
    task_1()
    task_2()
```

**Example:**
```python
def sync_function():
    print("Task 1")
    print("Task 2")

sync_function()
```

**Output:**
```
Task 1
Task 2
```

In synchronous programming, the function `sync_function` will execute `task_1` and then `task_2`, blocking any other task until these two tasks complete.

---

### **Asynchronous Programming**

Asynchronous programming allows tasks to run concurrently, enabling other tasks to continue executing without waiting for others to complete. This is particularly useful for I/O-bound operations like file reading, network requests, or database queries.

**Syntax:**
```python
import asyncio

async def function_name():
    await task_1()
    await task_2()
```

**Parameters:**
- `async`: Defines an asynchronous function.
- `await`: Waits for the asynchronous operation to complete.

**Example:**
```python
import asyncio

async def async_function():
    print("Start Task 1")
    await asyncio.sleep(2)
    print("Finish Task 1")

async def main():
    await asyncio.gather(async_function(), async_function())

asyncio.run(main())
```

**Output:**
```
Start Task 1
Start Task 1
Finish Task 1
Finish Task 1
```

In asynchronous programming, multiple tasks run concurrently, and the program doesn't wait for each task to finish before starting the next one.

---

## **Object-Oriented Programming (OOP)**

### **Class**

A class is a blueprint for creating objects (instances). It encapsulates data for the object and methods to manipulate that data. In Python, a class is defined using the `class` keyword.

**Syntax:**
```python
class ClassName:
    def __init__(self, parameters):
        # Initialization code here

    def method(self):
        # Method logic here
```

**Parameters:**
- `__init__(self)`: The constructor method to initialize instance variables.

**Example:**
```python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"{self.name} is barking!")

# Creating an object (instance)
dog1 = Dog("Buddy", "Golden Retriever")
dog1.bark()
```

**Output:**
```
Buddy is barking!
```

A **class** defines a blueprint, and an object is created from that blueprint.

---

### **Object Creation**

An object is an instance of a class. It is created by calling the class as if it were a function, and it can have its own unique properties (instance variables) and behaviors (methods).

**Syntax:**
```python
object_name = ClassName(parameters)
```

**Example:**
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def start(self):
        print(f"The {self.make} {self.model} is starting!")

# Creating an object (instance)
car1 = Car("Tesla", "Model S")
car1.start()
```

**Output:**
```
The Tesla Model S is starting!
```

An **object** is instantiated from a class, and methods can be called on that object to perform operations.

---

