Q: What is object-oriented programming?
A: A programming approach that uses programmer-defined types to organize both code and data.

C: A [programmer-defined type] is also called a [class].

Q: What are three ways to represent points in Python?
A: 1. Store coordinates separately in two variables (x and y)
2. Store coordinates as elements in a list or tuple
3. Create a new type to represent points as objects

C: Defining a class named Point creates a [class object].

Q: What is the process of creating a new object called?
A: Instantiation, and the object is an instance of the class.

C: You can assign values to an instance using [dot notation].

Q: What are the named elements of an object called?
A: Attributes.

Q: How is "attribute" pronounced as a noun?
A: "AT-trib-ute" with emphasis on the first syllable.

C: A state diagram that shows an object and its attributes is called an [object diagram].

Q: What does the expression blank.x mean?
A: Go to the object blank refers to and get the value of x.

Q: What happens when a function parameter is an alias for an object passed as an argument?
A: If the function modifies the parameter, the original object changes.

C: An object that is an attribute of another object is [embedded].

Q: What can functions return in addition to basic types?
A: Functions can return instances (objects).

C: You can change the state of an object by making an assignment to one of its [attributes].

Q: Why can aliasing make a program difficult to read?
A: Because changes in one place might have unexpected effects in another place, and it's hard to keep track of all variables that might refer to a given object.

C: The [copy] module contains a function called [copy] that can duplicate any object.

Q: What is the default behavior of the == operator for instances?
A: It is the same as the is operator; it checks object identity, not object equivalence.

C: A [shallow copy] copies the object and any references it contains, but not the embedded objects.

Q: What does the deepcopy function do?
A: It copies not only the object but also the objects it refers to, and the objects they refer to, and so on.

Q: What exception do you get if you try to access an attribute that doesn't exist?
A: AttributeError.

Q: How can you check what type an object is?
A: Use the type() function.

C: You can use [isinstance] to check whether an object is an instance of a class.

Q: How can you check if an object has a particular attribute?
A: Use the built-in function hasattr().

Q: What are the two arguments to the hasattr() function?
A: The first argument is any object; the second argument is a string that contains the name of the attribute.

Q: What is another way to check if an object has needed attributes?
A: Use a try statement to attempt to access the attributes and catch AttributeError if they don't exist.

Q: What is a class?
A: A programmer-defined type. A class definition creates a new class object.

Q: What is a class object?
A: An object that contains information about a programmer-defined type. The class object can be used to create instances of the type.

Q: What is an instance?
A: An object that belongs to a class.

Q: What does instantiate mean?
A: To create a new object.

Q: What is an attribute?
A: One of the named values associated with an object.

Q: What is an embedded object?
A: An object that is stored as an attribute of another object.

Q: What is a shallow copy?
A: To copy the contents of an object, including any references to embedded objects; implemented by the copy function in the copy module.

Q: What is a deep copy?
A: To copy the contents of an object as well as any embedded objects, and any objects embedded in them, and so on; implemented by the deepcopy function in the copy module.

Q: What is an object diagram?
A: A diagram that shows objects, their attributes, and the values of the attributes.
