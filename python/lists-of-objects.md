# Python: Lists of Objects

In Python, lists can store any type of data — including **class objects**. This makes it easy to manage groups of structured items like users, games, or employees.

---

## Creating a Class (Review)

We begin with a sample class:

```python
class VideoGame:
    def __init__(self, name, price):
        self.name = name
        self.price = price

    def __str__(self):
        return f"{self.name} – ${self.price}"
```

---

## Creating a List of Objects

You can store multiple `VideoGame` objects in a list:

```python
game1 = VideoGame("Candy Crush", 0)
game2 = VideoGame("Minecraft", 20)
game3 = VideoGame("FIFA", 40)

game_list = [game1, game2, game3]
```

---

## Iterating Over the List

Loop through and print:

```python
for game in game_list:
    print(game)  # Calls __str__()
```

Or access individual attributes:

```python
for game in game_list:
    print(game.name)
```

---

## Modifying Attributes in a List

You can update objects inside the list like this:

```python
game_list[1].price = 18  # Change price of Minecraft
```

---

## Adding New Objects to List

```python
new_game = VideoGame("Valorant", 0)
game_list.append(new_game)
```

---

## Sample Task – Filtering by Price

```python
for game in game_list:
    if game.price == 0:
        print(f"{game.name} is free!")
```

---

## Summary

- Python lists can store objects from any class.
- You can iterate, modify, and filter like with any other list.
- Great for menu programs, catalog systems, or inventory tracking.

