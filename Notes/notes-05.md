# Java Object-Oriented Design Basics

## Key Concept

- Every object has two things:
  - Properties
  - Methods

---

## Method Calling

- We need a virtual object to call a method.

Example:
```java
Calculator calc;
calc.add();
```

- This will not work because we are just creating a reference. We haven't created an object yet.

### Correct Way
```java
Calculator calc = new Calculator();
```

- `new` is used to create space.
- The constructor is used to assign space.
