Q: What is Java's key promise that attracted programmers?
A: Write-once/run-anywhere portability

Q: What file extension is used for Java source code?
A: `.java`

Q: What file extension is used for compiled Java code?
A: `.class`

C: Java source code is compiled into [bytecode], which can run on any device with a [Java Virtual Machine].

Q: What are the four steps in "The Way Java Works"?
A: 1. Create source document using Java language
2. Run through compiler to check for errors
3. Compiler creates bytecode document
4. Virtual machines read and run the bytecode

C: A source code file holds one [class] definition. The class must go within a pair of [curly braces].

Q: What goes in a class?
A: One or more methods

Q: What goes in a method?
A: Statements (instructions for how the method should be performed)

C: When the JVM starts running, it looks for a method called [main] with the signature: public static void [main](String[] args)

Q: What is the structure of Java code hierarchy?
A:
  - Source file contains classes
  - Classes contain methods
  - Methods contain statements

C: Every Java application must have at least one [class] and at least one main [method] per application.

Q: What are the three things you can tell the JVM to do inside a method?
A:
  - Do something (statements)
  - Do something again and again (loops)
  - Do something under a condition (branching)

C: Each statement must end in a [semicolon].

Q: How do you write a single-line comment in Java?
A: Use two forward slashes: `//`

C: Variables are declared with a [name] and a [type].

Q: What are the three standard looping constructs in Java?
A:
  - `while`
  - `do`-`while`
  - `for`

C: A conditional test is an expression that results in a [boolean] value —- something that is either [true] or [false].

Q: What are three common comparison operators in Java?
A:
  - `<` (less than)
  - `>` (greater than)
  - `==` (equality)

C: The [assignment] operator uses one equals sign (`=`), while the [equals] operator uses two equals signs (`==`).

Q: What does a `while` loop do?
A: As long as the conditional test is true, it executes everything inside the loop block (bounded by curly braces)

C: In Java, an `if` test is the same as a boolean test in a [while] loop, except instead of repeating, you execute code once if the condition is [true].

Q: What is the difference between `System.out.print()` and `System.out.println()`?
A: `println` inserts a newline after printing, while `print` keeps everything on the same line

Q: What command is used to compile a Java program?
A: `javac` (followed by the filename, e.g., `javac MyProgram.java`)

Q: What command is used to run a compiled Java program?
A: `java` (followed by the class name, e.g., `java MyProgram`)

C: The compiler checks for [syntax] violations and won't let you compile until it's satisfied that everything will run correctly.

Q: What is the primary role of the Java compiler?
A: To translate source code into bytecode and catch errors before runtime, including type violations and access violations

Q: What is the primary role of the JVM?
A: To execute bytecode, translate it for the underlying platform, and provide runtime security checks

C: Java is a [strongly-typed] language, meaning variables cannot hold data of the wrong type.

Q: How do you declare and initialize an array of `Strings` in Java?
A: `String[] arrayName = {"value1", "value2", "value3"};`

C: Java arrays are [zero-based], meaning the first element is at position [0].

Q: How do you get the length of an array in Java?
A: Use the `.length` property (e.g., `arrayName.length`)

C: The `Math.random()` method returns a random number between [0] and [not-quite-1].

Q: What operator is used to concatenate (join) Strings in Java?
A: The + operator

Q: How do you access an element from an array?
A: Use square brackets with the index: `arrayName[index]`

Q: What does the modulo operator `%` do in Java?
A: Returns the remainder after division

Q: Can a boolean and an integer be directly compared in Java?
A: No, they are not compatible types. Boolean tests require a boolean result.

C: The [public] keyword means everyone can access the method or class.

C: The [void] keyword means the method has no return value.

Q: What are the main differences between Java 1.02 and Java 5.0?
A: Java 1.02 had 250 classes, was slow, and buggy. Java 5.0 has 3500+ classes, is much faster, easier to develop with, and includes major language improvements.

Q: What does "platform-independent" mean for Java bytecode?
A: The compiled bytecode can run on any device with a Java Virtual Machine, regardless of the underlying hardware or operating system

C: Classes and methods must be defined within a pair of [curly braces].

Q: If you have code that might not work, what Java construct should you use?
A: A `try`-`catch` block

Q: In the code
```java
int x = 4;
while (x > 3)
{
  x = x - 1;
}
```
Will the loop run?
A: Yes, it will run once because x (4) is greater than 3, then x becomes 3 and the loop stops

Q: What happens if you don't increment or change the variable in a while loop condition?
A: The loop will run forever (infinite loop)

C: In Java, most [white space] doesn't matter for compilation.

Q: What is the significance of the "args" parameter in `main(String[] args)`?
A: It holds an array of Strings that can be passed as command-line arguments when running the program

C: To convert a String to an integer, use [Integer.parseInt()] method.

Q: What is Jini technology mentioned in the "Java-Enabled House" example?
A: Technology that allows Java-enabled devices to communicate and work together

Q: Why was Java designed to use bytecode compilation rather than pure interpretation?
A: For performance —- purely interpreted languages run much slower than bytecode-compiled languages

C: The compiler prevents about [99%] of potential problems before the code ever runs.

Q: What types of things does the Java compiler check for?
A: Syntax errors, datatype violations, access violations, and other compile-time errors

Q: What types of things does the JVM check for at runtime?
A: Security violations, ClassCastExceptions, incorrect array types, and dynamic binding issues

C: Java supports [dynamic binding], which allows programs to include new objects that weren't known to the original programmer.

Q: What is the purpose of the cast `(int)` before `Math.random()`?
A: To convert the floating-point result to an integer by truncating the decimal portion
