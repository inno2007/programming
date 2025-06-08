# Python: Classes, Objects, Constructors, and Inheritance

This section explores Python’s object-oriented programming (OOP) features including classes, constructors (`__init__`), instance attributes, methods, and inheritance. These concepts allow you to model real-world entities in code.

---

## Defining a Class

Use the `class` keyword to define a new type or object.

```python
class VideoGame:
    def __init__(self, name, price):
        self.name = name
        self.price = price

    def start(self):
        print(f"The game {self.name} has started.")

    def stop(self):
        print(f"The game {self.name} has stopped.")

    def play(self):
        print(f"Playing the game {self.name}.")
```

- `__init__` is the constructor, used to initialize objects.
- `self` refers to the current instance, like `this` in Java.

---

## Creating Objects

```python
first_game = VideoGame("Candy Crush", 0)
second_game = VideoGame("Minecraft", 20)

first_game.start()
first_game.play()
first_game.stop()
```

---

## Instance Attributes

Access or update attributes with dot notation:

```python
print(first_game.name)   # Candy Crush
first_game.price = 5     # Update price
```

---

## Special Method: `__str__()`

Defines how an object is represented as a string (like Java's `toString()`):

```python
def __str__(self):
    return f"Game: {self.name}, Price: ${self.price}"
```

Now, printing an object will call this:

```python
print(first_game)
```

---

## Methods with Parameters

```python
def discount(self, percentage):
    self.price -= self.price * (percentage / 100)
```

---

## Passing Objects as Parameters

You can pass objects to other methods or functions:

```python
def is_cheaper_than(self, other_game):
    return self.price < other_game.price
```

---

## Inheritance

Create a subclass that inherits from a parent class:

```python
class MobileGame(VideoGame):
    def __init__(self, name, price, platform):
        super().__init__(name, price)
        self.platform = platform

    def __str__(self):
        return f"{self.name} on {self.platform} - ${self.price}"
```

- `super()` calls the parent’s constructor.
- Add new attributes (like `platform`) in the child class.

---

## Object-Oriented Concepts Summary

| Concept        | Description                                           |
|----------------|-------------------------------------------------------|
| Class          | Template/blueprint for creating objects              |
| Object         | An instance of a class                               |
| Attribute      | Variables inside a class (state)                     |
| Method         | Functions inside a class (behavior)                  |
| Constructor    | `__init__` – initializes object attributes           |
| Inheritance    | A child class inherits attributes/methods from parent|

---

## Best Practices

- Use `self.attribute` to refer to attributes inside class methods.
- Use `__str__()` to define readable object output.
- Favor inheritance for code reuse and organization.


