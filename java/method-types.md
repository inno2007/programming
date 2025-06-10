# Java: Method Types – Constructor, Behavior, and Function Methods

In Java, methods can be categorized into three main types based on their role in object-oriented programming. This structure helps organize and clarify a class’s responsibilities.

---

## 1. Constructor Methods

Constructor methods are used to **create and initialize new objects**.

- Always have the same name as the class.
- No return type (not even `void`).
- Can be **overloaded** (multiple versions with different parameters).

### Example:

```java
public class Book {
    String title;
    double price;

    // Constructor Method
    public Book(String title, double price) {
        this.title = title;
        this.price = price;
    }
}
```

---

## 2. Behavior Methods

Behavior methods represent what the **object can do** — its actions or behaviors.  
They may change internal state or simply show behavior (like `start()`, `display()`, etc.).

- Often return `void`, but not always.
- Can access and modify instance variables.

### Example:

```java
public class Book {
    String title;

    public void read() {
        System.out.println("Reading " + title);
    }

    public void updateTitle(String newTitle) {
        title = newTitle;
    }
}
```

---

## 3. Function Methods

Function methods perform a **calculation or operation** and usually **return a value**.

- Used for computation, logic checks, or formatting.
- Should not change the object’s state (pure functions when possible).

### Example:

```java
public class Book {
    double price;

    public double applyDiscount(double percent) {
        return price - (price * percent / 100);
    }

    public String getTitle() {
        return title;
    }
}
```

---

## Summary Table

| Method Type        | Purpose                        | Return Type | Example           |
|--------------------|--------------------------------|-------------|-------------------|
| Constructor Method | Creates/initializes object     | None        | `Book(String, double)` |
| Behavior Method    | Defines object’s behavior      | Usually `void` | `read()`, `start()` |
| Function Method    | Returns a computed result      | Yes         | `getPrice()`, `applyDiscount()` |

