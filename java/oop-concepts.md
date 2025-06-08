# Java: Object-Oriented Programming (OOP) – Inheritance, Polymorphism, Interfaces, and Abstraction

This document explains Java’s object-oriented programming principles: inheritance, polymorphism, encapsulation, abstract classes, and interfaces. These concepts allow flexible, reusable, and modular design.

---

## Inheritance

Inheritance allows one class to inherit fields and methods from another.

- **Superclass (Parent Class)**: The class being inherited from
- **Subclass (Child Class)**: The class that inherits

**Syntax:**
```java
public class Truck extends Vehicle {
    // additional attributes and methods
}
```

### Example:
```java
class Vehicle {
    String model;
    public void start() {
        System.out.println("Vehicle started");
    }
}

class Truck extends Vehicle {
    int capacity;
    public void loadCargo() {
        System.out.println("Loading " + capacity + "kg of cargo.");
    }
}
```

**Key Keyword:**
- `extends`: Indicates inheritance
- `super()`: Calls parent constructor

---

## Method Overriding

Used when a child class provides a specific implementation of a method from the parent class.

```java
@Override
public void start() {
    System.out.println("Truck engine started");
}
```

---

## Encapsulation

Encapsulation hides data using private fields and provides access through getters/setters.

```java
public class Cyclist {
    private String name;
    private double speed;

    public String getName() {
        return name;
    }

    public void setSpeed(double speed) {
        this.speed = speed;
    }
}
```

### Benefits:
- Data protection
- Prevents direct modification
- Cleaner code and modular design

---

## Abstract Classes

An abstract class is a base class that cannot be instantiated. It may include abstract methods that subclasses must implement.

**Syntax:**
```java
abstract class Animal {
    abstract void makeSound();
}
```

**Child Class Example:**
```java
class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Bark");
    }
}
```

### Key Points:
- Use `abstract` keyword
- Enforces method implementation in child classes
- Allows common fields/methods across subclasses

---

## Interfaces

Interfaces define a set of methods that must be implemented by any class that "implements" the interface.

**Syntax:**
```java
interface HasArea {
    double getArea();
}
```

**Implementing Class:**
```java
class Square implements HasArea {
    double side;

    public double getArea() {
        return side * side;
    }
}
```

### Interface Characteristics:
- No method body in interface (until Java 8 default methods)
- A class can implement **multiple interfaces**

---

## Polymorphism

Polymorphism means "many forms". It allows objects to be treated as instances of their parent class or interface.

### Example:
```java
Animal a1 = new Dog(); // Reference is Animal, actual object is Dog
a1.makeSound(); // Calls Dog’s makeSound()
```

**Real-World Example:**
```java
ArrayList<HasArea> shapes = new ArrayList<>();
shapes.add(new Circle(5));
shapes.add(new Square(3));

for (HasArea s : shapes) {
    System.out.println(s.getArea());
}
```

---

## Key Differences: Inheritance vs Interfaces

| Feature            | Inheritance                 | Interface                           |
|--------------------|-----------------------------|-------------------------------------|
| Keyword            | `extends`                   | `implements`                        |
| Inherit From       | One class only              | Multiple interfaces allowed         |
| Purpose            | Share common implementation | Enforce method implementation rules |
| Abstract Methods   | Optional                    | Mandatory                           |

---

## Summary

OOP in Java supports modular design and reusable code by combining:
- **Inheritance** (shared structure),
- **Encapsulation** (controlled access),
- **Abstraction** (common templates),
- **Polymorphism** (flexibility with object types).


