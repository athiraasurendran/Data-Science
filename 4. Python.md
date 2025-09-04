# Control Flow
## IF
This checks a condition, and if it's true, the indented code block under it will be executed.
```python
if True:
    print("Inside if block")
```

## IF-ELSE
```python
if True:
    print("Inside if block")
else:
    print("Inside Else block")
```

```python
a=10
b=20
if a>b:
    print("a is greater than b")
else:
    print("a is not greater than b")
```
## IF-ELIF
```python
x = 10
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is exactly 10")
elif x < 10:
    print("x is less than 10")
```

## IF-ELIF-ELSE
```python
x = 10
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is exactly 10")
else:
    print("x is less than 10")
```
A more general format would be
```python
if condition:
    pass
elif condition:
    pass
else:
    pass
```
## Nested IFs
You can also nest conditional statements for more complex checks
```python
x = 15
if x > 10:
    print("x is greater than 10")
    if x > 20:
        print("x is also greater than 20")
    else:
        print("x is not greater than 20")
```

# Loops

## For Loop
For loops can be applied on any sequential object (list, string, tuple, range, etc.)
```python
for char in "Hello":
    print(char)
```

```python
for i in range(10):
    print(i)
```

## While Loop
```python
i = 1
while i<=10:
  print(i)
  i = i+1
```
### Continue
Skips the current iteration and goes to the next one.
```python
for i in range(5):
    if i == 2:
        continue
    print(i)
# Output: 0, 1, 3, 4  (2 is skipped)
```
### Break
Stops the loop completely.
```python
for i in range(5):
    if i == 3:
        break
    print(i)
# Output: 0, 1, 2  (loop ends when i = 3)
```

# Basic Library Usage
## Keyword library
Python has a built-in library called keyword that shows reserved words in Python.
```python
import keyword

print(keyword.kwlist)  # Shows all Python keywords
```

# Print formatting
## Placeholder passing
Use {} inside strings and .format() or f-strings to insert values.
```python
name = "Athira"
age = 24

print("My name is {} and I am {} years old.".format(name, age))
print(f"My name is {name} and I am {age} years old.")  # f-string (newer, easier)
```

## Multiline Assignment
Assign multiple variables in one line.
```python
x, y, z = 10, 20, 30
print(x, y, z)  # 10 20 30
```
Assign same value to multiple variables.
```python
a = b = c = 5
print(a, b, c)  # 5 5 5
```
## Line-breaking
Use \ to break a long line into multiple lines.
```python
total = 10 + 20 + 30 + \
        40 + 50
print(total)  # 150
```
In parentheses, brackets, or braces you don’t need \.
```python
numbers = [
    1, 2, 3,
    4, 5, 6
]
print(numbers)
```
