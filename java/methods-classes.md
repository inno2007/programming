# Java: Methods, Classes, and Object-Oriented Structure

This document explains how to define and use methods, create classes, instantiate objects, use constructors, and structure Java programs with encapsulation and access modifiers.

---

## Java Methods

A **method** is a reusable block of code that performs a specific action.

### Syntax:

```java
returnType methodName(parameters) {
    // method body
}
```

### Examples:

```java
public void greet() {
    System.out.println("Welcome to Java!");
}
```

```java
public int add(int x, int y) {
    return x + y;
}
```

---

## Parameters and Return Values

- Parameters are values passed into a method.
- The return type can be `void` (no return) or any valid Java type (e.g., `int`, `String`).

```java
public String sayHello(String name) {
    return "Hello, " + name;
}
```

---

## Calling Methods

```java
sayHello("Alice"); // Returns: "Hello, Alice"
```

---

## Creating a Class

```java
public class VideoGame {
    String name;
    double price;

    // Constructor
    public VideoGame(String name, double price) {
        this.name = name;
        this.price = price;
    }

    // Method
    public void startGame() {
        System.out.println("The game " + name + " has started.");
    }

    // Method with return
    public double applyDiscount(double discount) {
        price -= discount;
        return price;
    }

    // toString method
    public String toString() {
        return name + " costs $" + price;
    }
}
```

---

## Creating and Using Objects

```java
public class Main {
    public static void main(String[] args) {
        VideoGame minecraft = new VideoGame("Minecraft", 50.0);
        minecraft.startGame();
        System.out.println(minecraft.applyDiscount(10.0));
        System.out.println(minecraft.toString());
    }
}
```

---

## Constructors

- A constructor is a special method used to initialize objects.
- It must have the same name as the class.

```java
public class Person {
    String firstName;
    int age;

    public Person(String firstName, int age) {
        this.firstName = firstName;
        this.age = age;
    }
}
```

---

## Access Modifiers and Encapsulation

- `public`: accessible everywhere
- `private`: accessible only within the class

### Getters (Accessors)

```java
public String getName() {
    return name;
}
```

### Setters (Mutators)

```java
public void setName(String name) {
    this.name = name;
}
```

Encapsulation allows you to keep data safe and only accessible in controlled ways.

---

## Method Overloading

You can define multiple methods with the same name but different parameter lists.

```java
public int add(int x, int y) {
    return x + y;
}

public double add(double x, double y) {
    return x + y;
}
```

---

## Class Inheritance (Preview)

```java
public class Truck extends Vehicle {
    private int cargoCapacity;

    public Truck(String model, int capacity) {
        super(model); // Calls parent constructor
        this.cargoCapacity = capacity;
    }

    @Override
    public void displayDetails() {
        System.out.println("Truck Model: " + model + ", Capacity: " + cargoCapacity);
    }
}
```

---

