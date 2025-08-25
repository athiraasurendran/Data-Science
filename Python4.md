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


## Object
### Creating objects of a particular class

### Inheritance
