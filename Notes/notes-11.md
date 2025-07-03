# Final Keyword in Java

## Final Variables

- A **final variable** is a constant. Once assigned, its value **cannot be changed.**

Example:
```java
final int MAX_LIMIT = 100;
```

### Key Points:
- Must be **initialized at the time of declaration** or in a constructor.
- Commonly used for constants.

---

## Final Methods

- A **final method cannot be overridden** by child classes.

Example:
```java
class Animal {
    final void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    // Cannot override sound() here
}
```

### Key Points:
- Use `final` to **prevent method modification in subclasses.**
- Often used when method behavior must remain unchanged.

---

## Final Classes

- A **final class cannot be extended (inherited).**

Example:
```java
final class Shape {
    // code
}

// class Circle extends Shape {}  // Not allowed
```

### To note:
- Use `final` to **protect the entire class from being subclassed.**
- Example: `String` class in Java is final.

---

## Quick Summary:
- **Final Variables:** Value cannot change.
- **Final Methods:** Cannot be overridden.
- **Final Classes:** Cannot be inherited.

Final keyword is a great way to **create stability and security** in your code.
