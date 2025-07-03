# Polymorphism in Java

## What is Polymorphism?
Polymorphism means **"many forms."** It allows one interface to be used for different data types or classes.

### Types of Polymorphism:
- **Compile-Time Polymorphism (Static Binding)**
- **Run-Time Polymorphism (Dynamic Binding)**

---

## Compile-Time Polymorphism

### Achieved by: Method Overloading

#### Method Overloading:
- Same method name with different parameters within the same class.

Example:
```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```

### Key Points:
- Happens at compile time.
- Improves readability.

---

## Run-Time Polymorphism

### Achieved by: Method Overriding

- The method that gets executed is decided at **runtime.**
- Enables Java to support **dynamic method dispatch.**

Example:
```java
Animal a = new Dog();
a.sound(); // Will call Dog's sound() method
```

### Key Points:
- Parent class reference can point to child class object.
- Helps in achieving flexibility and scalability in code.

---

## Why Polymorphism Matters?
- Makes code **more flexible**
- Improves **reusability**
- Supports **clean architecture**
