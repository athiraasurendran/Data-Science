# Functions in Python

Functions are reusable blocks of code that perform a specific task.

They help in improving **code reusability, readability, and modularity**.

---

## Built-in Functins

Python provides many ready-to-use functions such as:

- `print()` → displays output  
- `len()` → returns the length of a sequence  
- `sum()` → returns the sum of elements  
- `type()` → returns the type of an object  
- `range()` → generates a sequence of numbers

---

## Custom Functions

You can define your own functions using the `def` keyword.

```python
def greet():
    print("Hello, welcome to Python!")
```
---

### Function arguments

Functions can accept inputs (parameters).

```python
def add(a, b):
    return a + b

print(add(5, 3))   # Output: 8

```
---
### Default arguments

You can assign default values to parameters.

```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()          # Output: Hello, Guest!
greet("Athira")  # Output: Hello, Athira!

```
---

### kwargs

### Function return values
