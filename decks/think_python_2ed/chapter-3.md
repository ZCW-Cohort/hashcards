Q: What is a function in the context of programming?
A: A named sequence of statements that performs a computation.

Q: What is the expression in parentheses called when you call a function?
A: The argument of the function.

C: A function [takes] an argument and [returns] a result.

C: The result of a function is also called the [return value].

Q: How does the int function convert floating-point values to integers?
A: It chops off the fraction part (it doesn't round off).

C: A [module] is a file that contains a collection of related functions.

Q: What statement is used to import a module?
A: An import statement.

C: To access a function in a module, you specify the [module name] and the [function name], separated by a [dot]. This format is called [dot notation].

Q: What value does math.pi provide?
A: A floating-point approximation of π, accurate to about 15 digits.

Q: How do trigonometric functions like sin, cos, and tan take their arguments?
A: In radians.

Q: How do you convert from degrees to radians?
A: Divide by 180 and multiply by π.

C: One of the most useful features of programming languages is their ability to take small building blocks and [compose] them.

Q: What is the one exception to where you can put an arbitrary expression?
A: The left side of an assignment statement has to be a variable name.

C: The keyword [def] indicates that this is a function definition.

Q: What are the rules for function names?
A: Letters, numbers and underscore are legal, but the first character can't be a number. You can't use a keyword as the name of a function.

C: The first line of a function definition is called the [header]; the rest is called the [body].

Q: What must the header of a function end with?
A: A colon.

Q: What is the convention for indentation in Python function bodies?
A: Four spaces.

Q: What type of quotation marks must be used in Python?
A: Straight quotes (not curly quotes).

C: Defining a function creates a [function object], which has type [function].

Q: What happens when you define a function?
A: Function definitions get executed just like other statements, but the effect is to create function objects. The statements inside the function do not run until the function is called.

C: The order statements run in is called the [flow of execution].

Q: Where does execution always begin in a program?
A: At the first statement of the program.

Q: Do function definitions alter the flow of execution?
A: No, but the statements inside the function don't run until the function is called.

C: A function call is like a [detour] in the flow of execution.

C: Inside a function, arguments are assigned to variables called [parameters].

Q: What does the argument get evaluated in relation to the function call?
A: The argument is evaluated before the function is called.

C: When you create a variable inside a function, it is [local], which means that it only exists inside the [function].

Q: What happens to local variables when a function terminates?
A: The variable is destroyed.

C: A [frame] is a box in a stack diagram that represents a function call.

Q: What is the special name for the topmost frame in a stack diagram?
A: __main__

C: A [traceback] is a list of the functions that are executing, printed when an exception occurs.

Q: What is the order of functions in a traceback?
A: The same as the order of the frames in the stack diagram. The function that is currently running is at the bottom.

C: Functions that return results are called [fruitful functions].

C: Functions that perform an action but don't return a value are called [void functions].

Q: What value do you get if you assign the result of a void function to a variable?
A: None.

Q: Is None the same as the string 'None'?
A: No, None is a special value that has its own type (NoneType).

Q: What are four reasons why it is worth dividing a program into functions?
A: 1) Creating a new function gives you an opportunity to name a group of statements, making your program easier to read and debug
2) Functions can make a program smaller by eliminating repetitive code
3) Dividing a long program into functions allows you to debug the parts one at a time
4) Well-designed functions are often useful for many programs and can be reused

Q: How is debugging like detective work?
A: You are confronted with clues and you have to infer the processes and events that led to the results you see.

Q: How is debugging like an experimental science?
A: Once you have an idea about what is going wrong, you modify your program and try again. If your hypothesis was correct, you can predict the result.

C: A [function] is a named sequence of statements that performs some useful operation. Functions may or may not take arguments and may or may not produce a result.

C: A [function definition] is a statement that creates a new function, specifying its name, parameters, and the statements it contains.

C: A [function object] is a value created by a function definition. The name of the function is a variable that refers to a function object.

C: The [header] is the first line of a function definition.

C: The [body] is the sequence of statements inside a function definition.

C: A [parameter] is a name used inside a function to refer to the value passed as an argument.

C: A [function call] is a statement that runs a function. It consists of the function name followed by an argument list in parentheses.

C: An [argument] is a value provided to a function when the function is called. This value is assigned to the corresponding parameter in the function.

C: A [local variable] is a variable defined inside a function. A local variable can only be used inside its function.

C: The [return value] is the result of a function. If a function call is used as an expression, the return value is the value of the expression.

C: A [fruitful function] is a function that returns a value.

C: A [void function] is a function that always returns None.

C: [None] is a special value returned by void functions.

C: A [module] is a file that contains a collection of related functions and other definitions.

C: An [import statement] is a statement that reads a module file and creates a module object.

C: A [module object] is a value created by an import statement that provides access to the values defined in a module.

C: [Dot notation] is the syntax for calling a function in another module by specifying the module name followed by a dot (period) and the function name.

C: [Composition] is using an expression as part of a larger expression, or a statement as part of a larger statement.

C: [Flow of execution] is the order statements run in.

C: A [stack diagram] is a graphical representation of a stack of functions, their variables, and the values they refer to.

C: A [frame] is a box in a stack diagram that represents a function call. It contains the local variables and parameters of the function.

C: A [traceback] is a list of the functions that are executing, printed when an exception occurs.
