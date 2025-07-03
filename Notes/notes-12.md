
# Object Class in Java

## What is the Object Class?

The **Object class** is the parent of all classes in Java. Every class either directly or indirectly inherits from the `Object` class.

### Key Points:
- It is the **topmost class** in Java.
- All classes in Java automatically extend `Object`.
- It defines **methods that are available to all objects.**

---

## Common Methods in the Object Class

### 1. `toString()`
- Converts an object to a String representation.
- By default, it shows the memory address, but you can override it to display meaningful info.

Example:
```java
public String toString() {
    return "Object Info";
}
```

### 2. `equals(Object obj)`
- Compares two objects for equality.
- By default, checks reference equality (same memory location).
- Can be overridden to compare object contents.

### 3. `hashCode()`
- Returns the hash code of an object.
- Important when using hash-based collections like `HashMap` or `HashSet`.

### 4. `getClass()`
- Returns the runtime class of the object.

### 5. `clone()`
- Used to create a **copy** of an object.
- Requires implementing the `Cloneable` interface.

### 6. `finalize()`
- Called by the Garbage Collector before destroying the object.
- Rarely used in modern Java.

---

## Why Object Class Matters?
- Provides a **common foundation** for all classes.
- Supports core Java features like Collections, Reflection, and more.
- Helps in **polymorphic behavior** (parent class reference pointing to child objects).

---

# Upcasting and Downcasting in Java

## Upcasting

### What is Upcasting?
- **Upcasting** is casting a child class object to a parent class reference.

Example:
```java
Dog d = new Dog();
Animal a = d; // Upcasting
```

### Key Points:
- Happens **automatically** (implicit casting).
- You can only access the methods of the parent class unless they are overridden.
- Provides flexibility and is used in runtime polymorphism.

### Why Use Upcasting?
- Allows writing more generic and flexible code.
- Supports polymorphic behavior.

---

## Downcasting

### What is Downcasting?
- **Downcasting** is casting a parent class reference back to a child class reference.

Example:
```java
Animal a = new Dog();
Dog d = (Dog) a; // Downcasting
```

### Key Points:
- Must be done **explicitly.**
- Risky: Can cause `ClassCastException` if not used carefully.
- You should always ensure the reference is actually pointing to the child class object.

### Safe Downcasting:
```java
if (a instanceof Dog) {
    Dog d = (Dog) a;
    d.sound();
}
```

### Why Use Downcasting?
- To access specific methods or properties of the child class that are not available in the parent class.
