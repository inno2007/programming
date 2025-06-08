# Python: Variables, Data Types, Input/Output, and Lists

This section covers the basics of Python programming, focusing on how to work with variables, input/output, strings, and lists. These are the foundational elements for writing any Python script or project.

---

## Python Variables

Python does not require explicit type declarations. Variables are dynamically typed.

```python
university_name = "UTS College"  # String
age = 19                         # Integer
gpa = 3.75                       # Float
```

- Use `snake_case` for variable and function names.
- Class names use `UpperCamelCase`.

---

## Data Types

| Type       | Example           |
|------------|-------------------|
| String     | `"Hello"`         |
| Integer    | `10`, `-4`        |
| Float      | `2.45`, `0.01`    |
| Boolean    | `True`, `False`   |

Python automatically determines the type based on assignment.

---

## Input and Output

### Print Statement

```python
print("Hello, world")
```

### String Input

```python
name = input("What is your name? ")
print(f"Hi {name}!")
```

### Integer and Float Input

```python
age = int(input("Enter your age: "))
weight = float(input("Enter your weight in kg: "))
```

---

## String Operations

### Concatenation

```python
first = "Hello"
second = "World"
message = first + " " + second  # Hello World
```

### F-Strings

```python
name = "Sachio"
print(f"Welcome, {name}!")
```

- Useful for combining text and variables

---

## Python Lists

Lists are dynamic and can hold any data type.

### Creating Lists

```python
fruits = ["apple", "banana", "cherry"]
scores = [85, 90, 78]
```

### Accessing Elements

```python
print(fruits[0])  # Output: apple
```

- Index starts from `0`
- Negative indices can be used to access from the end: `fruits[-1]`

### Modifying Elements

```python
fruits[1] = "orange"
```

### List Length

```python
print(len(fruits))  # Output: 3
```

### Adding and Removing

```python
fruits.append("grape")
fruits.remove("banana")
```

---

## Understanding List Behavior

Lists can store other lists (nested):

```python
matrix = [[1, 2], [3, 4]]
```

`append()` adds to the end, and `remove()` deletes the first occurrence.

---

## List Iteration

```python
for fruit in fruits:
    print(fruit)
```

### Example with Index

```python
for i in range(len(fruits)):
    print(f"Item {i}: {fruits[i]}")
```

---

## Summary

- Python variables are simple and dynamically typed
- Strings can be combined using `+` or formatted with `f""`
- Lists are powerful, built-in data structures used like Java's ArrayList
- `len()`, `append()`, `remove()` and iteration are key operations


