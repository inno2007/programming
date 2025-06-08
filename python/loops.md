# Python: Loops – for, while, range, break, and continue

This document explores Python loops, including `for` and `while`, and how to control flow using `break`, `continue`, and `range()`. These tools allow repetitive execution of code.

---

## For Loop

Used to iterate over a sequence such as a list, string, or range.

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

You can also use `for` with `range()`:

```python
for i in range(5):  # 0 to 4
    print(i)
```

### `range(start, stop, step)`

- `start`: where the count begins (default = 0)
- `stop`: the loop runs up to but not including this number
- `step`: how much to increment (default = 1)

```python
for i in range(1, 10, 2):
    print(i)  # prints odd numbers from 1 to 9
```

---

## While Loop

Executes a block of code as long as the condition is `True`.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

### Infinite Loop (Avoid unless intentional)

```python
while True:
    print("Running forever")
```

---

## Loop Control Statements

### `break`

Stops the loop immediately.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### `continue`

Skips the current iteration and continues with the next.

```python
for i in range(6):
    if i == 3:
        continue
    print(i)
```

---

## Nested Loops

You can place loops inside other loops:

```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

---

## Real Example – Print Odd Numbers

```python
for i in range(1, 20):
    if i % 2 != 0:
        print(i)
```

---

## Task Example – Multiples of 3

```python
for i in range(17, -1, -1):
    if i % 3 == 0:
        print(i)
```

---

## Do-While Equivalent in Python

Python doesn't have a built-in `do-while`, but it can be mimicked:

```python
while True:
    print("Runs once")
    if not condition:
        break
```

---

## Summary

- `for` is best for iterating over known sequences.
- `while` is best for unknown-length loops.
- `break` exits the loop.
- `continue` skips to the next iteration.
- Use `range()` to generate numeric sequences.


