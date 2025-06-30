# Constructors and Inheritance in Java

## Constructors: The Basics

When you want to **assign values to instance variables automatically when an object is created**, you use a **constructor.**

### Constructor Syntax:
```java
public ClassName() {
    // Initialization code
}
```

### Key Points:
- A constructor **must have the same name as the class.**
- A constructor **never returns anything.**
- Every time you create an object, the **constructor is automatically called.**

### Rule of Thumb:
Whenever you want to perform operations like **assignment or calculations inside a class, always do it in a method, not in the constructor.**

---

## Types of Constructors

### Default Constructor:
- Java provides this **automatically** if you don't create any constructor.
- It has no parameters.

### Parameterized Constructor:
- You create this when you want to **pass values directly** while creating an object.

Example:
```java
public Student(String name) {
    this.name = name;
}
```

---

## this and super Keywords

- `this()` → Calls **another constructor of the same class.**
- `super()` → Calls **the constructor of the parent class.**

### Important:
- When you create an object of a class, **the constructor of the parent class is always called first.**
- Even if you don't write `super()`, **Java adds it automatically.**

### What is super()?
- Calls the **default constructor of the parent class** (if no parameters).

### Reminder:
- Every class in Java **implicitly extends the `Object` class.**

---

## Naming Conventions

- **Class and Interface Names:** Start with Capital letters (CamelCase)
- **Variable and Method Names:** Start with lowercase letters
- **Constants:** Use ALL CAPS (UPPERCASE)

---

## Object Creation Explained

Example:
```java
A obj = new A();
```

There are **two steps happening here:**
1. **Reference Creation:** `A obj;`
2. **Object Creation:** `new A();`

- `new A();` → Creates an **anonymous object** (if you don’t assign it, you can’t reuse it).

---

# Inheritance in Java

### Inheritance = Acquiring properties and methods of another class.

- **Super / Parent / Base Class:** Class that is inherited from.
- **Child / Sub / Derived Class:** Class that inherits.

### Types of Inheritance in Java:
- **Single Inheritance:** One parent, one child.
- **Multilevel Inheritance:** Inheritance chain (Grandparent → Parent → Child)

### Java Does Not Support Multiple Inheritance (with classes)
- **Why?** To avoid ambiguity (Diamond Problem)

---

## Method Overriding

- When a **child class provides its own version** of a method that is already defined in the parent class.

### Key Rules:
- Method name and parameters must match exactly.
- Used to **achieve runtime polymorphism.**

Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}
```

---

## Recap:
- Constructors initialize objects when they are created.
- `this()` calls constructor of the same class.
- `super()` calls constructor of the parent class.
- Naming conventions keep code clean and readable.
- Inheritance allows one class to inherit from another.
- Method overriding lets child classes change parent behavior.



