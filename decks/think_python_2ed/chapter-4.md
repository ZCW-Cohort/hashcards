Q: What is the turtle module used for in Python?
A: Creating images using turtle graphics.

C: The [turtle] module (with a lowercase 't') provides a function called [Turtle] (with an uppercase 'T') that creates a Turtle object.

Q: What does the mainloop() function do in the turtle module?
A: It tells the window to wait for the user to do something.

C: A [method] is similar to a function, but it uses slightly different syntax and is associated with an object, called using dot notation.

Q: What are the basic movement methods available for a Turtle object?
A:
- fd (forward) - moves the turtle forward by a distance in pixels
- bk (backward) - moves the turtle backward
- lt (left turn) - turns the turtle left by an angle in degrees
- rt (right turn) - turns the turtle right by an angle in degrees

C: The argument for [lt] and [rt] is an angle in [degrees].

Q: What do the pu and pd methods do?
A: They control the pen: "pen up" (pu) lifts the pen so the turtle doesn't leave a trail, and "pen down" (pd) puts the pen down so the turtle leaves a trail when it moves.

C: A [for] statement is also called a [loop] because the flow of execution runs through the body and then loops back to the top.

Q: What is the syntax structure of a for statement?
A: It has a header that ends with a colon and an indented body. The body can contain any number of statements.

Q: What is encapsulation in the context of function design?
A: Wrapping a piece of code up in a function, which attaches a name to the code and serves as documentation.

C: One of the benefits of [encapsulation] is that it attaches a name to the code, which serves as a kind of [documentation].

Q: What is generalization when applied to functions?
A: Adding a parameter to a function to make it more general, so it can work with different values instead of being limited to specific constants.

C: Adding a [parameter] to a function is called [generalization] because it makes the function more general.

Q: What are keyword arguments?
A: Arguments that include the parameter names as "keywords" when calling a function, making the program more readable (e.g., polygon(bob, n=7, length=70)).

Q: What is the interface of a function?
A: A summary of how a function is used: what are the parameters, what does the function do, and what is the return value.

C: An interface is ["clean"] if it allows the caller to do what they want without dealing with [unnecessary details].

Q: What is refactoring?
A: The process of rearranging a program to improve interfaces and facilitate code re-use.

Q: What are the steps of the "encapsulation and generalization" development plan?
A:
1. Start by writing a small program with no function definitions
2. Once the program works, identify a coherent piece, encapsulate it in a function and give it a name
3. Generalize the function by adding appropriate parameters
4. Repeat steps 1-3 until you have a set of working functions
5. Look for opportunities to improve the program by refactoring

C: A [docstring] is a string at the beginning of a function that explains the [interface].

Q: What convention is used for writing docstrings?
A: All docstrings are triple-quoted strings (also known as multiline strings) because the triple quotes allow the string to span more than one line.

Q: What should a good docstring contain?
A: It should explain concisely what the function does (without getting into details of how), what effect each parameter has on the behavior of the function, and what type each parameter should be (if not obvious).

C: [Preconditions] are requirements that are supposed to be true before the function starts executing, while [postconditions] are conditions at the end of the function.

Q: Who is responsible for preconditions?
A: The caller. If the caller violates a properly documented precondition and the function doesn't work correctly, the bug is in the caller, not the function.

Q: If preconditions are satisfied but postconditions are not, where is the bug?
A: The bug is in the function.

Q: What formula is used to calculate the exterior angles of an n-sided regular polygon?
A: 360/n degrees

Q: How can you approximate a circle using the polygon function?
A: By drawing a many-sided polygon, making sure that length * n = circumference, where circumference = 2 * pi * r.

C: In Python 2, integer division might cause issues with angle calculations, which can be solved by using [floating-point] numbers (e.g., 360.0 / n instead of 360 / n).

Q: What is a method?
A: A function that is associated with an object and called using dot notation.

Q: What is a loop?
A: A part of a program that can run repeatedly.

Q: What is encapsulation?
A: The process of transforming a sequence of statements into a function definition.

Q: What is generalization?
A: The process of replacing something unnecessarily specific (like a number) with something appropriately general (like a variable or parameter).

Q: What is a keyword argument?
A: An argument that includes the name of the parameter as a "keyword".

Q: What is an interface?
A: A description of how to use a function, including the name and descriptions of the arguments and return value.

Q: What is refactoring?
A: The process of modifying a working program to improve function interfaces and other qualities of the code.

Q: What is a development plan?
A: A process for writing programs.

Q: What is a docstring?
A: A string that appears at the top of a function definition to document the function's interface.

Q: What is a precondition?
A: A requirement that should be satisfied by the caller before a function starts.

Q: What is a postcondition?
A: A requirement that should be satisfied by the function before it ends.
