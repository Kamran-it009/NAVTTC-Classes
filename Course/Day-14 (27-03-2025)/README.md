# Python README: OOP (Object-Oriented Programming) in Python

## **Example of Class and Object**

A class is a blueprint for creating objects (instances). An object is an instance of a class, where the class defines the properties and methods that the object will have.

**Syntax:**
```python
class ClassName:
    def __init__(self, attributes):
        self.attribute = attribute

# Creating an object
object_name = ClassName(attribute_value)
```

**Example:**
```python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"{self.name} is barking!")

# Creating an object
dog1 = Dog("Buddy", "Golden Retriever")
dog1.bark()
```

**Output:**
```
Buddy is barking!
```

---

## **Attributes and Methods**

- **Attributes**: Variables that are associated with a class and its objects.
- **Methods**: Functions that belong to a class and can operate on the attributes of that class.

**Syntax:**
```python
class ClassName:
    def __init__(self, attribute):
        self.attribute = attribute  # Attribute

    def method(self):  # Method
        print(self.attribute)
```

**Example:**
```python
class Car:
    def __init__(self, model, year):
        self.model = model
        self.year = year

    def display_info(self):
        print(f"Car Model: {self.model}, Year: {self.year}")

car1 = Car("Toyota", 2020)
car1.display_info()
```

**Output:**
```
Car Model: Toyota, Year: 2020
```

---

## **Constructor Function**

The constructor `__init__()` in Python is used to initialize the object when it is created. It is called automatically when an object is instantiated.

**Syntax:**
```python
class ClassName:
    def __init__(self, parameters):
        # Initialization code
```

**Example:**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 30)
```

---

## **Destructor**

A destructor `__del__()` is called when an object is destroyed or goes out of scope. It is used to clean up resources.

**Syntax:**
```python
class ClassName:
    def __del__(self):
        print("Destructor called")
```

**Example:**
```python
class Car:
    def __del__(self):
        print("Car object is being destroyed")

car1 = Car()
del car1  # Destructor called
```

**Output:**
```
Car object is being destroyed
```

---

## **Inheritance**

Inheritance allows one class (child) to inherit the attributes and methods of another class (parent).

**Syntax:**
```python
class Parent:
    pass

class Child(Parent):
    pass
```

### **Multilevel Inheritance**

In multilevel inheritance, a class inherits from a derived class, forming a chain.

**Example:**
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

class Puppy(Dog):
    def wag_tail(self):
        print("Puppy wags tail")

puppy = Puppy()
puppy.speak()
puppy.bark()
puppy.wag_tail()
```

---

### **Hierarchical Inheritance**

In hierarchical inheritance, multiple classes inherit from a single parent class.

**Example:**
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

class Cat(Animal):
    def meow(self):
        print("Cat meows")

dog = Dog()
cat = Cat()
dog.speak()
cat.speak()
```

---

### **Multiple Inheritance**

Multiple inheritance occurs when a class inherits from more than one parent class.

**Example:**
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Playful:
    def play(self):
        print("Playing!")

class Dog(Animal, Playful):
    pass

dog = Dog()
dog.speak()
dog.play()
```

---

## **Method Overriding**

Method overriding allows a child class to provide a specific implementation for a method that is already defined in the parent class.

**Example:**
```python
class Animal:
    def sound(self):
        print("Some sound")

class Dog(Animal):
    def sound(self):
        print("Bark")

dog = Dog()
dog.sound()
```

**Output:**
```
Bark
```

---

## **Method Overloading**

Python does not support method overloading directly. However, you can achieve it by using default arguments or variable-length arguments.

**Example:**
```python
class Calculator:
    def add(self, *args):
        return sum(args)

calc = Calculator()
print(calc.add(1, 2))
print(calc.add(1, 2, 3, 4))
```

---

## **Encapsulation**

Encapsulation is the practice of restricting access to certain components of an object and bundling the data with methods that operate on that data.

**Example:**
```python
class Car:
    def __init__(self, model, year):
        self.__model = model  # Private attribute
        self.__year = year

    def get_model(self):
        return self.__model

    def set_model(self, model):
        self.__model = model

car1 = Car("Toyota", 2020)
car1.set_model("Honda")
print(car1.get_model())
```

---

## **Getter and Setter Methods**

Getter and Setter methods are used to access and modify private attributes of a class.

**Example:**
```python
class Person:
    def __init__(self, name):
        self.__name = name

    def get_name(self):
        return self.__name

    def set_name(self, name):
        self.__name = name

person = Person("John")
print(person.get_name())
person.set_name("Alice")
print(person.get_name())
```

---

## **Abstraction**

Abstraction is the concept of hiding the internal details of an object and exposing only the necessary features.

**Example:**
```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def sound(self):
        pass

class Dog(Animal):
    def sound(self):
        print("Bark")

dog = Dog()
dog.sound()
```

---

## **Polymorphism**

Polymorphism allows objects of different classes to be treated as instances of the same class through inheritance.

**Example:**
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Bark")

class Cat(Animal):
    def speak(self):
        print("Meow")

animals = [Dog(), Cat()]
for animal in animals:
    animal.speak()
```

---

## **Static Methods**

A static method does not require a class instance to be called. It behaves like a regular function, but it belongs to the class.

**Syntax:**
```python
class ClassName:
    @staticmethod
    def method_name():
        pass
```

**Example:**
```python
class Math:
    @staticmethod
    def add(x, y):
        return x + y

print(Math.add(5, 3))
```

---

## **Dunder Methods / Magic Methods**

Dunder methods (also known as magic methods) are special methods in Python that have double underscores before and after their names. These methods are used to implement behavior for basic operations such as addition, subtraction, etc.

**Example:**
```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Point(self.x + other.x, self.y + other.y)

point1 = Point(1, 2)
point2 = Point(3, 4)
point3 = point1 + point2  # Calls __add__
```

---

## **Class and Object Creation**

A class is a blueprint, and objects are instances of that class. To create an object, you call the class as if it were a function.

---

## **Another Example of Class and Object**

**Example:**
```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def get_book_info(self):
        print(f"Title: {self.title}, Author: {self.author}")

book1 = Book("Python 101", "John Doe")
book1.get_book_info()
```

**Output:**
```
Title: Python 101, Author: John Doe
```
---
