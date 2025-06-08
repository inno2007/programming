# Python: File Handling (Read, Write, Append, and Close)

Python supports working with external `.txt` files. This allows programs to save data or load existing information.

---

## Opening Files

Use the `open()` function.

```python
file = open("data.txt", "r")  # Read mode
file = open("data.txt", "w")  # Write mode (overwrites)
file = open("data.txt", "a")  # Append mode (adds to end)
```

---

## Reading a File

Read the entire content:

```python
file = open("data.txt", "r")
content = file.read()
print(content)
file.close()
```

Read line by line:

```python
file = open("data.txt", "r")
for line in file:
    print(line.strip())
file.close()
```

Read into a list:

```python
lines = file.readlines()
```

---

## Writing to a File

```python
file = open("output.txt", "w")
file.write("This will be the first line\n")
file.write("This is the second line")
file.close()
```

- `"w"` overwrites the file.
- If file does not exist, it creates one.

---

## Appending to a File

```python
file = open("output.txt", "a")
file.write("\nThis line is added to the end.")
file.close()
```

---

## Best Practice: Using `with` Statement

Automatically closes the file, even if an error occurs.

```python
with open("data.txt", "r") as file:
    print(file.read())
```

```python
with open("log.txt", "a") as file:
    file.write("User logged in\n")
```

---

## Example: Save Usernames to File

```python
with open("users.txt", "a") as file:
    while True:
        name = input("Enter name (or leave empty to quit): ")
        if not name:
            break
        file.write(name + "\n")
```

---

## Reading into List and Removing Newlines

```python
with open("users.txt", "r") as file:
    usernames = [line.strip() for line in file]

print(usernames)
```

---

## Checking File Content First

```python
try:
    with open("users.txt", "r") as file:
        print(file.read())
except FileNotFoundError:
    print("File not found. Creating a new one.")
```

---

## Summary

- Use `open(filename, mode)` to handle files.
- `"r"` = read, `"w"` = write, `"a"` = append.
- Use `with` to manage file context safely.
- Always close files if not using `with`.

