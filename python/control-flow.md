# Python: Control Flow, Conditionals, and Boolean Logic

This section covers Python's decision-making tools using `if`, `elif`, and `else`. These allow programs to make decisions based on conditions. We also include how logical operators work in Python.

---

## Boolean Expressions

Python uses:
- `True` and `False` for boolean values
- `==`, `!=`, `<`, `<=`, `>`, `>=` for comparisons

### Example:

```python
x = 10
y = 20
print(x == y)     # False
print(x < y)      # True
print(x >= 10)    # True
```

---

## If Statement

```python
score = 85
if score > 80:
    print("Well done!")
```

Executes the block only if the condition is `True`.

---

## If–Else Statement

```python
score = 65
if score >= 50:
    print("Pass")
else:
    print("Fail")
```

Runs either the `if` block or the `else` block depending on the condition.

---

## If–Elif–Else Chains

```python
mark = 90

if mark < 50:
    print("Fail")
elif mark >= 85:
    print("Distinction")
else:
    print("Pass")
```

- You can have multiple `elif` branches
- Only the first true condition runs

---

## Logical Operators

| Operator | Python     | Example              |
|----------|------------|----------------------|
| AND      | `and`      | `a > 0 and a < 10`   |
| OR       | `or`       | `x == 5 or x == 10`  |
| NOT      | `not`      | `not is_logged_in`   |

### Example with Multiple Conditions

```python
age = 22
is_student = True

if age < 25 and is_student:
    print("Eligible for student discount")
```

---

## Odd or Even Check

```python
number = int(input("Enter a number: "))
if number % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

## Python Indentation Rules

Python uses indentation instead of braces `{}` to define blocks.

```python
if x > 0:
    print("Positive")
    print("Still inside the block")
```

- Consistency is key: 4 spaces is the standard.
- Improper indentation will raise `IndentationError`.

---

## Summary

- Python uses `if`, `elif`, and `else` for decision-making.
- Logical operators `and`, `or`, and `not` combine or invert conditions.
- Code blocks depend on correct **indentation**, not `{}`.
- Control flow enables dynamic program behavior.

