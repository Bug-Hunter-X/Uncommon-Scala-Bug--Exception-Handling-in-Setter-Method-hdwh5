# Uncommon Scala Bug: Exception Handling in Setter Method

This repository demonstrates a subtle bug that can occur in Scala when using setter methods with exception handling.  The `MyClass` class defines a setter for the `age` property that throws an `IllegalArgumentException` if a negative age is provided. This is good practice for input validation.

However, the `Main` object shows how this exception, if not properly handled, can cause the program to crash.  The `try-catch` block demonstrates one way to handle this;  Robust error handling is crucial for production applications.

**How to Reproduce:**

1. Compile and run the `MyClass.scala` file. 
2. Observe the output, noting the exception handling.
3. Modify the `Main` object to remove the `try-catch` block. Run again and observe the program crash.

**Key Learning:**

Always handle exceptions appropriately in your Scala code, especially those thrown from setter or other critical methods, to ensure application stability and resilience.