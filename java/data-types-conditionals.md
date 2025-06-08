# Java: Data Types, Variables, Conditionals, and Input Handling

This document outlines the foundational Java concepts covered in early programming labs at UTS, including primitive data types, input/output, and conditional branching using `if`, `else`, and comparison operators.

---

## Data Types

### 1. Primitive Data Types

| Type     | Description                         | Example              |
|----------|-------------------------------------|----------------------|
| `int`    | Integer numbers                     | `int age = 20;`      |
| `double` | Floating-point numbers              | `double pi = 3.14;`  |
| `boolean`| True or False values                | `boolean valid = true;` |
| `char`   | Single characters                   | `char letter = 'A';` |

### 2. Reference Types

- Examples: `String`, arrays, classes
- Stored as memory references instead of direct values
- Example:
```java
String name = "Sachio";
```

---

## Declaring Variables

```java
int score = 85;
double balance = 99.95;
boolean isStudent = true;
String university = "UTS";
```

---

## Input & Output (Using `In` class)

The `In` class is used for receiving input from the user.

### Input Methods:

| Input Type | Example Code |
|------------|--------------|
| String     | `String name = In.nextLine();` |
| Integer    | `int age = In.nextInt();` |
| Double     | `double price = In.nextDouble();` |

### Output:

```java
System.out.println("Hi " + name + "!");
System.out.println("Next year, you'll be " + (age + 1));
```

---

## Boolean Expressions

```java
boolean isRich = balance >= 10000.0;
boolean isEqual = 5 == 5;
boolean isDifferent = 3 != 5;
boolean combined = isRich && isStudent;
```

| Operator | Description          |
|----------|----------------------|
| `==`     | Equals               |
| `!=`     | Not equal            |
| `>`      | Greater than         |
| `<`      | Less than            |
| `>=`     | Greater or equal     |
| `<=`     | Less or equal        |
| `&&`     | AND                  |
| `||`     | OR                   |
| `!`      | NOT                  |

---

## Conditional Branching

### Simple If Statement

```java
if (score > 90) {
    System.out.println("Excellent!");
}
```

### If-Else Statement

```java
if (score >= 50) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

### Else If Chain

```java
int mark = 90;

if (mark < 50) {
    System.out.println("Fail");
} else if (mark > 85) {
    System.out.println("Distinction");
} else {
    System.out.println("Pass");
}
```

---

## Example Program: Planet Selector

```java
public class SelectPlanet {
    public static void main(String[] args) {
        System.out.println("Select a planet:");
        System.out.println("1. Mercury");
        System.out.println("2. Venus");
        System.out.println("3. Earth");
        System.out.println("4. Mars");

        int choice = In.nextInt();

        if (choice == 1) {
            System.out.println("You picked Mercury");
        } else if (choice == 2) {
            System.out.println("You picked Venus");
        } else {
            System.out.println("Unknown selection");
        }
    }
}
```

---

## Even or Odd Check

```java
int number = In.nextInt();
if (number % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```

---
