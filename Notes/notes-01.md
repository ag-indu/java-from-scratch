# JVM and Java Environment

## How Java Works

- JVM is a platform. If you have JVM, you can run Java applications.
- JVM works in which environment? JVM is part of JRE.
- JVM's job is to execute Java code.
- We will not write code that directly works on JVM. It needs bytecode.
- We create a Java file and need to convert it into bytecode, so in between, we have the Java compiler (`javac`).

## Compilation Flow

```plaintext
.java file → javac → .class (bytecode) → JVM → Output
```

- The compiler creates bytecode which has the extension `.class` file.
- You also want an environment, right? That is JRE. JVM is part of JRE.
- JDK is used by developers. JDK has JRE. JRE has JVM.

---

## Summary

- To compile Java code, you need JDK (Java Development Kit).
- JVM is needed to run your code.
- We need some extra files to run the code that is present in JRE.
- As a developer, you need JDK.
