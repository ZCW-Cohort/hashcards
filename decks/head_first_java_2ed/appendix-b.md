Q: What is the Bitwise NOT operator (`~`) used for?
A: It flips all the bits of a primitive.

Q: What does the Bitwise AND operator (`&`) return?
A: A value whose bits are turned on only if both original bits are turned on.

Q: What does the Bitwise OR operator (`|`) return?
A: A value whose bits are turned on only if either of the original bits are turned on.

Q: What does the Bitwise XOR operator (`^`) return?
A: A value whose bits are turned on only if exactly one of the original bits are turned on.

Q: What does the Right Shift Operator (`>>`) do?
A: It shifts all of a number's bits right by a certain number, filling all of the bits on the left side with whatever the original leftmost bit was. The sign bit does not change.

Q: What does the Unsigned Right Shift Operator (`>>>`) do?
A: It shifts bits right and ALWAYS fills the leftmost bits with zeros. The sign bit might change.

Q: What does the Left Shift Operator (`<<`) do?
A: It shifts bits left and fills the rightmost bits with zeros. The sign bit might change.

C: Shifting bits [left] effectively [multiplies] a number by a power of two, and shifting bits [right] effectively [divides] a number by a power of two.

C: In Java, negative numbers are stored using [two's complement] formula.

Q: How do you change a number's sign using two's complement?
A: Flip all the bits, then add 1.

Q: Are Strings in Java mutable or immutable?
A: Immutable.

Q: Why are Strings stored in a special part of memory called the String Pool?
A: For security purposes and conserving memory. If there is already a String in the String Pool with the same value, the JVM doesn't create a duplicate, it simply refers your reference variable to the existing entry.

Q: Does the Garbage Collector clean up the String Pool?
A: No, the Garbage Collector doesn't go there.

Q: What class should you use if you have to do a lot of String manipulations?
A: StringBuilder.

Q: Can you change the value of a wrapper object once it's created?
A: No. There is no setter method for a wrapper object. Once you create a wrapper object, there's no way to change the value of that object.

C: Roses are red, violets are blue. [Strings] are [immutable], [wrappers] are too.

Q: What are assertions used for?
A: Debugging Java programs. They are like `System.out.println()` statements on steroids that can be enabled or disabled at runtime.

Q: How do you add an assertion to your code?
A: Use the assert keyword followed by a condition, for example:
```java
assert (height > 0);
```

Q: How do you compile code with assertions enabled?
A: As of Java 5.0, use
```bash
javac TestDriveGame.java
```
no command line options necessary.

Q: How do you run a program with assertions enabled?
A: Use
```bash
java -ea TestDriveGame
```

Q: What happens if an assertion is false?
A: It throws an `AssertionError`.

Q: What happens to assert statements when you run a program without enabling assertions?
A: They are completely ignored by the JVM, so there's no performance hit.

Q: What is a block variable?
A: A variable declared inside a block of code (bounded by curly braces), such as within loops or conditional expressions.

Q: How long does a block variable stay in scope?
A: Only as long as the block in which it's declared.

C: Your Java programs will be more debuggable and expandable if you use [local] variables instead of [instance] variables, and [block] variables instead of [local] variables, whenever possible.

Q: What are linked invocations?
A: A coding construct where multiple method calls are chained together in a single statement, with each method being called on the object returned by the previous method.

Q: How do you decipher linked invocations?
A: Work from left to right, finding the result of each method call and using that returned object to call the next method to the right.

Q: What is a static nested class?
A: A class enclosed within another class and marked with the static modifier.

Q: How do you instantiate a static nested class?
A: Use the outer class name, not an instance. For example:
```java
FooOuter.BarInner foo = new FooOuter.BarInner();
```

Q: What is the difference between nested and inner classes?
A: All inner classes are nested classes, but not all nested classes are inner classes. Non-static nested classes are referred to as inner classes.

Q: What is an anonymous inner class?
A: A class created and instantiated at the point where you need it, without giving it a name. You pass the entire class definition where you'd normally pass only an instance.

Q: What are the four access levels in Java?
A: In order from least to most restrictive
- public
- protected
- default
- private

Q: What does `public` access mean?
A: Any code anywhere can access the public thing.

Q: What does `protected` access mean?
A: Code in the same package has access, AND it allows subclasses outside the package to inherit the protected thing.

Q: What does `default` access mean?
A: Only code within the same package as the class with the default thing can access the default thing.

Q: What does `private` access mean?
A: Only code within the same class can access the private thing. It's private to the class, not to the object.

Q: When should you use `public` access?
A: For classes, constants (static final variables), methods you're exposing to other code (like getters and setters), and most constructors.

Q: When should you use `private` access?
A: For virtually all instance variables, and for methods that you don't want outside code to call.

C: Both [String] and [StringBuffer]/[StringBuilder] classes have: `charAt()`, `length()`, `substring()`, and `toString()` methods.

Q: How do you concatenate `Strings` in the `String` class?
A: Using the `concat(String)` method.

Q: How do you concatenate `Strings` in `StringBuffer` and `StringBuilder`?
A: Using the `append(String)` method.

Q: What is the difference between `StringBuffer` and `StringBuilder`?
A: As of Java 5.0 you should use StringBuilder instead of StringBuffer, unless your String manipulations need to be thread-safe, which is not common.

C: The [StringBuffer] and [StringBuilder] classes have delete(), insert(), replace(), reverse(), and setCharAt() methods.

Q: In Java, what is a two-dimensional array?
A: An array of arrays.

Q: How many arrays are created when you declare
```java
int[][] a2d = new int[4][2];
```
A: Five arrays: one array with 4 elements, and each of those four elements is a reference variable referring to an int array with 2 elements.

Q: How do you access the second element in the third array of a 2D array named a2d?
A:
```java
int x = a2d[2][1];
```

Q: What is an enumeration in Java?
A: A set of constant values that represent the only valid values for a variable.

Q: How do you declare an enum in Java 5.0?
A: Using the enum keyword, for example:
```java
public enum Members { JERRY, BOBBY, PHIL };
```

Q: What class does every enum implicitly extend?
A: `java.lang.Enum`.

Q: Can you compare `enum` instances using `==`?
A: Yes, and you can also use the `.equals()` method. Usually `==` is considered better style.

Q: Can you use enums in switch statements?
A: Yes.

Q: What built-in method does every enum come with for iteration?
A: The values() method, which is typically used in a for loop.

Q: Can you add constructors and methods to an enum?
A: Yes, you can add constructors, methods, variables, and constant-specific class bodies.

Q: What are constant-specific class bodies in enums?
A: They allow you to override basic enum methods for specific enum values, similar to overriding a method in a subclass.
