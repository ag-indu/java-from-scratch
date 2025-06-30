# Strings in Java

## Why Do We Use Strings?
When you need to store a bunch of related characters together, we use **strings.**

### Syntax Example:
```java
String name = "Indulekha";
```

In Java:
- **Primitive types** always start with lowercase letters (like `int`, `float`).
- **String** is actually a **class**, that’s why it starts with a capital letter.

---

## Behind the Scenes: Memory Management
Even though we wrote:
```java
String name = "Indulekha";
```
we didn’t use the `new` keyword here.

But this is what’s happening under the hood:
- In **JVM stack memory**, a **reference variable** (`name`) is created.
- The **actual String object** is created in **heap memory.**
- The stack holds the address (reference) of that string in the heap.

You can also explicitly create a string like this:
```java
String name = new String("Indulekha");
```

---

## String Properties and Methods
- `string.hashCode()` → Returns the hash code (basically the memory reference identity).
- String concatenation:
  - Can be done with `+` operator.
  - Can also use `String.concat("text")`

Example:
```java
String a = "Hello";
a = a + " World"; // This does not modify the original string.
```

### Important:
When you do string concatenation, **Java doesn’t actually modify the existing string.**
- A **new string is created** with the combined value.
- The old string becomes eligible for **garbage collection.**

### Accessing Characters:
```java
String name = "Indulekha";
char ch = name.charAt(2); // Returns character at index 2
```

---

## String Memory Optimization: String Constant Pool
```java
String name1 = "hello";
String name2 = "hello";
```
We might think that two objects are created, but actually **only one string object exists.**

In the heap, there’s a **special area called the String Constant Pool.**
- If the same string already exists, Java reuses the object.
- This helps **save memory** because strings are used a LOT in Java.

---

## Mutable vs Immutable Strings
- **By default, Strings are immutable** (you can’t change them directly).
- If you want **mutable strings**, you can use:
  - `StringBuffer`
  - `StringBuilder`

### StringBuffer Example:
```java
StringBuffer sb = new StringBuffer();
sb.append("Hello");
sb.insert(0, "Say ");
System.out.println(sb.toString());
System.out.println(sb.length());
```

### Key Differences:
- `StringBuffer` is **thread-safe** (good for multi-threaded programs)
- `StringBuilder` is **not thread-safe** but faster

---

## Recap:
- Strings are objects, not primitives.
- Strings are stored in heap memory but optimized in the String Constant Pool.
- Strings are **immutable** by default.
- Mutable strings can be created using `StringBuffer` or `StringBuilder`.
- String operations like concatenation always create **new strings** unless you use a mutable class.

---


