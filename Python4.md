# Object Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **classes** and **objects**.  

It helps organize code into reusable and modular structures.

---

## Class

A **class** is a blueprint for creating objects.

It defines attributes (data) and methods (functions) that describe the behavior of the objects.

---

### Basic Class Definition

```python
class Person:
    def __init__(self, name, age):
        self.name = name   # Instance attribute
        self.age = age

    def introduce(self):
        print(f"My name is {self.name} and I am {self.age} years old.")

```
---

### Class Attibutes

Class attributes are shared across all objects of the class.

```python
class Student:
    school_name = "ABC College"   # Class attribute

    def __init__(self, name):
        self.name = name          # Instance attribute

s1 = Student("Athira")
s2 = Student("Anu")

print(s1.school_name)  # Output: ABC College
print(s2.school_name)  # Output: ABC College

```

---

### Class Functions

Methods are functions defined inside a class.

- Instance Methods → act on individual objects (`self`)

- Class Methods → act on the class (`cls`)

- Static Methods → independent utility functions

```python

class MathOps:
    def square(self, x):        # Instance method
        return x * x

    @classmethod
    def greet(cls):             # Class method
        return "Hello from class method"

    @staticmethod
    def add(a, b):              # Static method
        return a + b

obj = MathOps()
print(obj.square(4))        # 16
print(MathOps.greet())      # Hello from class method
print(MathOps.add(5, 3))    # 8

```
---

## Object

An object is an instance of a class.

It represents a real-world entity with its own attributes and methods.

---

### Creating objects of a particular class

```python
p1 = Person("Athira", 24)
p1.introduce()  
# Output: My name is Athira and I am 24 years old.

```
---
### Inheritance

Inheritance allows a class (child) to acquire properties and methods of another class (parent).

```python
class Animal:
    def sound(self):
        print("Animals make different sounds")

class Dog(Animal):   # Dog inherits from Animal
    def sound(self):
        print("Bark! Bark!")

d = Dog()
d.sound()  # Output: Bark! Bark!

```
---

- Class = Blueprint

- Object = Instance of class

- Supports Encapsulation, Inheritance, Polymorphism, Abstraction

- Makes code more modular, reusable, and organized

---
