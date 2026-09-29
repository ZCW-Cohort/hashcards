Q: What is the difference between a fruitful function and a void function?
A: A fruitful function produces a return value, while a void function has an effect (like printing or moving a turtle) but returns None.

Q: What does the return statement do in a fruitful function?
A: It returns immediately from the function and uses the following expression as a return value.

Q: What is dead code?
A: Code that appears after a return statement, or any other place the flow of execution can never reach.

Q: What is the goal of incremental development?
A: To avoid long debugging sessions by adding and testing only a small amount of code at a time.

Q: What are the key aspects of incremental development?
A: 1. Start with a working program and make small incremental changes
2. Use variables to hold intermediate values so you can display and check them
3. Once the program is working, remove scaffolding or consolidate statements

Q: What is composition in the context of functions?
A: Calling one function from within another function.

Q: What do Boolean functions return?
A: Boolean values (True or False).

Q: Why is it common to give boolean functions names that sound like yes/no questions?
A: Because they return True or False to indicate whether something is true or false.

Q: What is a recursive definition?
A: A definition that contains a reference to the thing being defined.

Q: What are the two parts of the factorial function definition?
A: 1. The factorial of 0 is 1 (base case)
2. The factorial of any other value n is n multiplied by the factorial of n-1 (recursive case)

Q: What is the "leap of faith" in the context of recursive functions?
A: Instead of following the flow of execution, you assume that the recursive call works correctly and returns the right result.

Q: What is the fibonacci function definition?
A: fibonacci(0) = 0, fibonacci(1) = 1, fibonacci(n) = fibonacci(n-1) + fibonacci(n-2)

Q: What happens when you call factorial with a non-integer argument like 1.5?
A: It causes infinite recursion because the base case (n == 0) is never reached.

Q: What is isinstance used for?
A: To verify the type of an argument.

Q: What is a guardian in programming?
A: A programming pattern that uses a conditional statement to check for and handle circumstances that might cause an error.

Q: What are the three possibilities to consider when debugging a function that is not working?
A: 1. Something wrong with the arguments (precondition violated)
2. Something wrong with the function (postcondition violated)
3. Something wrong with the return value or how it is being used

C: Many Python functions, such as math functions, produce [return values].

C: A [fruitful function] the return statement includes an expression.

C: In a fruitful function, it is a good idea to ensure that every possible path through the program hits a [return statement].

C: [Temporary variables] like a can make debugging easier.

C: Code that appears after a return statement is called [dead code].

C: The first step in incremental development is to consider what the [inputs] (parameters) and [output] (return value) should be.

C: Code used during program development but not part of the final product is called [scaffolding].

C: When testing a function with incremental development, it is useful to know the [right answer].

C: [Composition] is when you call one function from within another.

C: The result of the == operator is a [boolean].

C: A [complete] programming language means that anything that can be computed can be expressed in this language.

C: The [Turing Thesis] states that a small subset of Python is a complete programming language.

C: When you get to a recursive call, you should assume the recursive call works and ask yourself if you can compute the result - this is called the [leap of faith].

C: The built-in function [isinstance] can verify the type of an argument.

C: [Guardians] act as guards, protecting the code that follows from values that might cause an error.

C: A variable used to store an intermediate value in a complex calculation is called a [temporary variable].

C: Part of a program that can never run, often because it appears after a return statement, is called [dead code].

C: A program development plan intended to avoid debugging by adding and testing only a small amount of code at a time is called [incremental development].

C: Code that is used during program development but is not part of the final version is called [scaffolding].

C: A programming pattern that uses a conditional statement to check for and handle circumstances that might cause an error is called a [guardian].