# Java: Loops and Arrays

This document explains the core Java loop structures (`for`, `while`, `for-each`) and how arrays are used to store and manipulate collections of data.

---

## Loop Concepts in Java

Loops are used to repeat a block of code multiple times. There are three primary types:

### 1. For Loop

Used when the number of iterations is known in advance.

**Syntax:**

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

- Initialization: `int i = 0`
- Condition: `i < 5`
- Update: `i++` after each iteration

### 2. While Loop

Used when the number of iterations is not known in advance.

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}
```

- Checks the condition before executing the loop body.

### 3. Do-While Loop

Executes the loop body **at least once** before checking the condition.

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

---

## Loop Control Statements

- `break`: exit the loop immediately
- `continue`: skip the rest of the loop and move to the next iteration

```java
for (int i = 0; i < 10; i++) {
    if (i == 5) continue;
    if (i == 8) break;
    System.out.println(i);
}
```

---

## Enhanced For Loop (For-Each)

Used to iterate over arrays or collections easily.

```java
int[] numbers = {1, 2, 3};
for (int num : numbers) {
    System.out.println(num);
}
```

---

## Java Arrays

Arrays are used to store multiple values of the same data type in a single variable.

### Declaring and Initializing

```java
int[] scores = {85, 90, 78};
String[] names = {"Ali", "Ben", "Cara"};
boolean[] flags = {true, false, false};
```

### Declaring with Size

```java
int[] numbers = new int[5]; // Creates an array of size 5
```

By default:
- `int` is initialized to 0
- `boolean` to `false`
- `String` to `null`

---

## Accessing Elements

```java
System.out.println(scores[0]); // First item
scores[1] = 95;                // Update value
```

Arrays are zero-indexed:  
- `scores[0]` refers to the first element  
- `scores.length` returns total number of elements

---

## Array Length and Iteration

```java
for (int i = 0; i < scores.length; i++) {
    System.out.println("Score: " + scores[i]);
}
```

### Combining and Computing

```java
int[] values = {2, 4, 6};
int result = values[0] + values[1] * 2;
System.out.println(result); // Output: 10
```

---

## Common Mistakes

- **ArrayIndexOutOfBoundsException**: occurs when accessing elements beyond the array size.
- Always ensure:
```java
if (i < array.length) {
    // safe access
}
```

---

## Summary Table

| Feature        | Syntax/Example                            |
|----------------|--------------------------------------------|
| Declare        | `int[] nums = new int[3];`                |
| Initialize     | `int[] nums = {1, 2, 3};`                 |
| Access         | `nums[0]`                                 |
| Update         | `nums[1] = 10;`                           |
| Length         | `nums.length`                             |
| Loop (for)     | `for (int i = 0; i < nums.length; i++)`   |
| Loop (for-each)| `for (int n : nums)`                      |


