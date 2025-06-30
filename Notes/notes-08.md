# Static Keyword and Encapsulation in Java

## Static Keyword Basics

- **Static variables** are shared by **all objects** of the class.
- Static variables should ideally be accessed using the **class name** instead of the object name (it’s cleaner and correct practice).
- You **can use static variables inside non-static methods.** No issues.
- Static variables are **class-level variables, not instance-level.**

### Instance Variables:
- To initialize instance variables (unique to each object), we use **constructors.**

---

## Static Block

- A **static block** runs **only once** when the class is loaded.
- It is usually used to initialize static variables if complex logic is needed.

### JVM Class Loading Order:
1. Class is loaded.
2. Static block (if any) executes.
3. Objects are instantiated (if created).

### Where is the class loaded?
- In JVM, class loading happens in a special area called the **Class Loader.**

### Important:
- If you **don’t create an object, the class won’t load** automatically.
- The static block **runs only when the class is loaded.**

#### Force Class Loading:
If you want to load a class without creating an object:
```java
Class.forName("ClassName"); // Forces the class to load
```
(We normally don’t use this in regular projects, but it’s good to know.)

---

## Static Methods

- Static methods can be called directly using the **class name.**

### Rules:
- You can **use static variables inside non-static methods.**
- You **cannot directly use non-static variables inside static methods.**
- If you need to use a non-static variable inside a static method, **pass an object as a parameter.**

---

## Why is `main` Method Static?

- If `main` was **non-static**, you would need to create an object to call it.
- But `main` is the **starting point of execution.**
- If the program hasn’t started, how would you create the object?

So, `main` **must be static** to allow the program to run without needing an object first.

---

# Encapsulation in Java

- **Encapsulation** is an OOP principle where **not all data should be accessible directly.**
- We achieve this using the **`private` keyword** to restrict variable access.
- Private variables can be accessed using **getter and setter methods.**

### Example:
```java
class Student {
    private String name;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
```

---

## `this` Keyword

- `this` refers to the **current object** calling the method.
- It helps differentiate between class variables and method parameters if they have the same name.

### Example:
```java
public void setName(String name) {
    this.name = name; // Refers to the instance variable
}
```

---

## Summary:
- Static variables and methods belong to the class, not objects.
- Static blocks run only once when the class loads.
- The `main` method is static because the program must start without creating an object.
- Encapsulation hides data using `private` variables and provides access through getters and setters.
- `this` refers to the current object and helps avoid variable naming conflicts.

---


