# Java Data Types and Variables

## Why Do We Build Software

- We build to solve problems: real-world problems with virtual world solutions.
- We deal with data and processing data.
- We store data in a database (persistent storage).
- You will receive data from the user and store it in a variable.
- Java is a strongly typed language.

---

## Data Types

Primitive - In-built data types. These are simple and fall into four categories:

- Integer: byte (1), short (2), int (4), long (8)
- Float: point integer values. double (8, default), float (4)
- Character: 2 bytes, UNICODE.
- Boolean: true, false

### Notes:
- Long needs 'l' (Example: `55434l`)
- Float needs 'f' (Example: `5.8f`)

---

## Literals

- For binary, you need to place 'b' (Example: `0b101`)
- For hexadecimal, you need to place 'x'

---

## Type Conversion and Casting

- You cannot change the type of a variable directly.
- You can assign values if type conversion is allowed.

Example:
```java
byte b = 127;
int a = 256;
b = a; // Will not work

a = b; // Will work
```

### Casting (Explicit)
```java
a = (int) b;
```

### Conversion (Implicit)
```java
a = b;
```

Example:
```java
int x = (int) f;
