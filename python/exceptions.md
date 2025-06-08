# Python: Exception Handling and Custom Exceptions

This document covers how to manage runtime errors using Python's built-in `try`, `except`, and `raise`. It also shows how to define your own exception classes.

---

## What is an Exception?

An exception is an error that interrupts program execution. Without handling, the program crashes.

### Common Exceptions

| Exception     | Trigger Example                  |
|---------------|----------------------------------|
| `ValueError`  | `int("abc")` – can't convert     |
| `IndexError`  | `my_list[5]` when list too short |
| `KeyError`    | Accessing missing key in dict    |

---

## Basic Exception Handling

Use `try` to wrap code that may error, and `except` to catch and handle it.

```python
try:
    age = int(input("Enter your age: "))
    print(f"You are {age} years old.")
except ValueError:
    print("Please enter a valid number.")
```

If the user enters non-numeric input, `ValueError` is caught and handled gracefully.

---

## Handling Multiple Exceptions

Each error type can have its own `except` block.

```python
try:
    num = int(input("Enter index: "))
    print([1, 2, 3][num])
except ValueError:
    print("Not a valid integer")
except IndexError:
    print("Index out of range")
```

---

## Raising Exceptions

Use `raise` to manually trigger an exception.

```python
def withdraw(balance, amount):
    if amount <= 0:
        raise ValueError("Amount must be positive.")
    if amount > balance:
        raise ValueError("Insufficient funds.")
    return balance - amount
```

```python
try:
    balance = withdraw(100, -10)
except ValueError as e:
    print("Error:", e)
```

---

## Creating Custom Exceptions

You can define your own exception types using classes.

```python
class InsufficientFundsError(Exception):
    pass

def withdraw(balance, amount):
    if amount > balance:
        raise InsufficientFundsError("You don't have enough funds.")

try:
    withdraw(100, 200)
except InsufficientFundsError as e:
    print("Bank error:", e)
```

---

## Final Structure

General structure of robust exception handling:

```python
try:
    # risky operation
except SpecificError:
    # handle it
except AnotherError:
    # different handling
else:
    # runs if no error
finally:
    # runs no matter what
```

---

## Summary

- Use `try` and `except` to prevent crashing.
- Handle multiple types of errors with different blocks.
- Use `raise` to enforce rules.
- Create custom error types by extending `Exception`.


