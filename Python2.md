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
### Break


# Basic Library Usage
## Keyword library

# Print formatting
## Placeholder passing

## Multiline Assignment
## Line-breaking
