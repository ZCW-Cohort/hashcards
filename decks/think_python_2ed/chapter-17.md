Q: What are the three defining characteristics of object-oriented programming?
A:
- Programs include class and method definitions
- Most of the computation is expressed in terms of operations on objects
- Objects often represent things in the real world, and methods often correspond to the ways things in the real world interact

C: A [method] is a function that is associated with a particular class.

Q: What are the two syntactic differences between methods and functions?
A:
- Methods are defined inside a class definition in order to make the relationship between the class and the method explicit
- The syntax for invoking a method is different from the syntax for calling a function

C: In method invocation, the object a method is invoked on is called the [subject].

Q: What is the conventional name for the first parameter of a method and why?
A: The first parameter is called self, by convention. This reflects the perspective that in object-oriented programming, the objects are the active agents, so a method invocation like start.print_time() says "Hey start! Please print yourself."

C: Inside a method, the [subject] is assigned to the first parameter.

Q: When using function syntax to call a method, how do you invoke it?
A: Use the class name, dot notation, and pass the object as a parameter. For example: Time.print_time(start)

Q: When using method syntax to call a method, how do you invoke it?
A: Use the object, dot notation, and the method name with parentheses. For example: start.print_time()

C: A [positional argument] is an argument that doesn't have a parameter name; that is, it is not a keyword argument.

Q: What is the init method and when is it invoked?
A: The init method (short for "initialization") is a special method that gets invoked when an object is instantiated. Its full name is __init__.

C: The [__str__] method is a special method that is supposed to return a string representation of an object.

Q: When does Python invoke the __str__ method?
A: When you print an object, Python invokes the __str__ method.

C: By defining a method named [__add__] for a class, you can use the + operator on objects of that class.

Q: What is operator overloading?
A: Changing the behavior of an operator so that it works with programmer-defined types.

C: The built-in function [isinstance] takes a value and a class object, and returns True if the value is an instance of the class.

Q: What is type-based dispatch?
A: An operation that checks the type of an operand and invokes different functions for different types. It dispatches the computation to different methods based on the type of the arguments.

C: The special method [__radd__] stands for "right-side add" and is invoked when an object appears on the right side of the + operator.

Q: Why is __radd__ necessary for making addition commutative?
A: When an integer is the first operand and a Time object is the second, Python asks the integer to add a Time object, which it doesn't know how to do. The __radd__ method allows the Time object to handle addition when it appears on the right side of the + operator.

C: Functions that work with several types are called [polymorphic].

Q: What makes a function polymorphic?
A: If all of the operations inside a function work with a given type, the function works with that type. Polymorphic functions can work with multiple types.

Q: What is the best kind of polymorphism?
A: The unintentional kind, where you discover that a function you already wrote can be applied to a type you never planned for.

C: The built-in function [vars] takes an object and returns a dictionary that maps from attribute names (as strings) to their values.

C: The built-in function [getattr] takes an object and an attribute name (as a string) and returns the attribute's value.

Q: What is the design principle for keeping interfaces separate from implementations?
A: The methods a class provides should not depend on how the attributes are represented. This allows you to change the implementation without changing the interface.

Q: Why is it important to keep interfaces separate from implementations?
A: It makes software more maintainable. If you design the interface carefully, you can change the implementation without changing the interface, which means that other parts of the program don't have to change.

Q: What is a good practice for initializing object attributes?
A: It is considered a good idea to initialize all of an object's attributes in the init method. This prevents mistakes that can occur when objects of the same type don't have the same attributes.

C: When writing a new class, it's recommended to start by writing [__init__] and [__str__] methods.

Q: object-oriented language
A: A language that provides features, such as programmer-defined types and methods, that facilitate object-oriented programming.

Q: object-oriented programming
A: A style of programming in which data and the operations that manipulate it are organized into classes and methods.

Q: method
A: A function that is defined inside a class definition and is invoked on instances of that class.

Q: subject
A: The object a method is invoked on.

Q: positional argument
A: An argument that does not include a parameter name, so it is not a keyword argument.

Q: operator overloading
A: Changing the behavior of an operator like + so it works with a programmer-defined type.

Q: type-based dispatch
A: A programming pattern that checks the type of an operand and invokes different functions for different types.

Q: polymorphic
A: Pertaining to a function that can work with more than one type.
