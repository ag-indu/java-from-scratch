# Arrays

## Why Do We Need Arrays?

When you create a **single variable**, you can store only **one value.**

Example:
```java
int i = 5;
int j = 6;
int k = 7;
```
But what if you want to store all these values together in **one variable?**

**That’s where arrays come in.**  
Arrays make it easy to store and manage **multiple values under a single variable.**

---

##  Syntax of an Array
```java
int num[] = {5, 6, 7}; // Direct initialization
```
OR  
```java
int num[] = new int[4]; // Declaring an array with fixed size
```

---

##  Looping Through an Array
We can use the **for-each loop** to print or access elements:
```java
for(int n : num) {
    System.out.println(n);
}
```
 The **for-each loop** works with arrays and array-type data structures.

---

##  Jagged Arrays (Arrays with Variable Columns)

In **multi-dimensional arrays**, the size of inner arrays (columns) doesn’t have to be fixed.

Example:
```java
int nums[][] = new int[3][];
```
 This is called a **jagged array.**

### Managing Jagged Arrays:
You need to assign each row individually:
```java
nums[0] = new int[3]; // Row 0 has 3 columns
nums[1] = new int[2]; // Row 1 has 2 columns
nums[2] = new int[4]; // Row 2 has 4 columns
```

---

##  Array Properties
- `.length` → Property that shows the size of the array.
- Arrays in Java are **objects** and are stored in **heap memory.**
- Memory allocated to arrays is **continuous.**  
   This is why the size of the array is **fixed** and cannot be changed later.
- By default, **integer arrays are filled with 0.**  
  (For objects, it would be `null` by default.)

---

##  Array of Objects
When you create an **array of objects**, Java:
- ✅ Creates space to store **references only.**
- ❌ Does NOT automatically create the actual objects.

### Example:
```java
// This creates space for references only (all are null by default)
Student[] students = new Student[3];

// You need to create objects for each reference like this:
for (int i = 0; i < students.length; i++) {
    students[i] = new Student(); // Now, actual objects are created
}
```
 You can only access object properties **after** the object is created.

---

##  For-Each Loop Syntax (Quick Recap)
```java
for (type variable : array_name) {
    // Access each element here
}
```

---

###  Key Takeaways:
- Arrays store multiple values under one variable.
- Arrays in Java are objects stored in heap memory.
- Arrays of objects **need manual object creation.**
- The size of the array is fixed.
- Jagged arrays can have variable-length rows.
