# Python: Dictionaries and Sets

This section introduces two essential data structures in Python: dictionaries (key-value pairs) and sets (unique collections). Both are useful for managing large or structured datasets efficiently.

---

## Dictionaries

A **dictionary** is a collection of key-value pairs. It's similar to a HashMap in Java.

### Creating a Dictionary

```python
top_performers = {"HD": 10, "D": 13}
remaining = {"C": 23, "P": 40, "F": 9}
```

Empty dictionary:

```python
empty_dict = {}
```

---

### Accessing Values

```python
print(top_performers["HD"])  # Output: 10
```

Check if key exists:

```python
if "D" in top_performers:
    print("Found grade D")
```

---

### Modifying / Adding Entries

```python
top_performers["HD"] = 12       # Modify
top_performers["DN"] = 7        # Add new key
```

---

### Deleting Entries

```python
top_performers.pop("HD")
```

---

### Iterating Over Dictionaries

```python
for key in top_performers:
    print(f"{key}: {top_performers[key]}")

for value in top_performers.values():
    print(value)

for key, value in top_performers.items():
    print(f"{key} => {value}")
```

---

### Combining Dictionaries

```python
combined = {}
for k in top_performers:
    combined[k] = top_performers[k]
for k in remaining:
    combined[k] = remaining[k]
```

Correcting values:

```python
combined["D"] += 3
combined["HD"] -= 3
```

---

## Sets

A **set** is a collection of unordered, unique elements.

### Creating Sets

```python
my_set = {"apple", "banana", "apple"}  # duplicate removed
```

Convert a list to a set:

```python
nums = [1, 2, 2, 3]
unique_nums = set(nums)
```

---

### Adding and Removing

```python
my_set.add("grape")
my_set.discard("banana")
```

---

### Set Operations

| Operation      | Symbol | Description                          |
|----------------|--------|--------------------------------------|
| Intersection   | `&`    | Elements in both sets                |
| Union          | `|`    | All elements from both sets          |
| Difference     | `-`    | Elements in one but not the other    |

```python
a = {10, 20, 30, 40}
b = {20, 40}

print(a & b)  # {20, 40}
print(a | b)  # {10, 20, 30, 40}
print(a - b)  # {10, 30}
```

---

### Checking Membership

```python
"apple" in my_set    # True
"orange" not in my_set  # True
```

---

### Iterating Over Sets

```python
for item in my_set:
    print(item)
```

---

### Get Size

```python
print(len(my_set))
```

---

## Summary

- Dictionaries store data as key-value pairs with fast lookup.
- Sets store unique items and support efficient membership tests.
- Use `&`, `|`, and `-` for powerful set operations.
- Both are core Python data structures used in data analysis, web apps, and algorithms.


