C: [State affects behavior, behavior affects state].

Q: How does an object's behavior relate to its state?
A: Methods use instance variable values. An object has behavior that acts on its state. For example, a Dog's bark might be different based on its size instance variable.

C: Every instance of a particular class has the [same methods], but the methods can [behave differently] based on the value of the [instance variables].

Q: Can every object of a type have different method behavior?
A: Sort of. Every instance of a particular class has the same methods, but the methods can behave differently based on the value of the instance variables.

C: A method uses [parameters]. A caller passes [arguments].

Q: What is the difference between parameters and arguments?
A: Arguments are the things you pass into methods. A parameter is nothing more than a local variable with a type and name that can be used inside the body of the method. Arguments land in parameters.

C: If a method takes a parameter, you must pass it [something]. And that something must be a value of the [appropriate type].

Q: What happens when you pass an argument to a method?
A: The bits representing the value are delivered into the method and land in the parameter (a variable of that type).

C: Every method is declared with a [return type]. A [void] return type means the method doesn't return anything.

Q: If you declare a method to return a value, what must you do?
A: You must return a value of the declared type (or a value that is compatible with the declared type).

C: Methods can have [multiple parameters]. Separate them with [commas] when you declare them.

Q: How are multiple arguments matched to parameters?
A: The arguments you pass land in the same order you passed them. First argument lands in the first parameter, second argument in the second parameter, and so on.

C: Java is [pass-by-value]. That means [pass-by-copy].

Q: What does pass-by-value mean in Java?
A: When you pass a variable to a method, Java makes a copy of the bits in the variable and passes that copy. The method cannot change the bits that were in the calling variable.

C: When you pass a primitive variable to a method, the method gets a [copy] of the value, not the [original variable].

Q: What happens to the original variable when you pass it as an argument?
A: The original variable doesn't change. The method receives a copy of the bits, so changes to the parameter inside the method don't affect the original variable.

C: Getters and Setters are also called [Accessors] and [Mutators].

Q: What are Getters and Setters used for?
A: Getters and Setters let you get and set instance variable values. A Getter's purpose is to send back the value as a return value. A Setter takes an argument value and uses it to set the value of an instance variable.

C: Mark instance variables [private] and provide [public] getters and setters for access control.

Q: What is encapsulation?
A: Encapsulation means hiding your data by marking instance variables private and forcing other code to go through setter methods. This protects your data and allows you to validate values and change implementation later.

C: Encapsulation puts a [force-field] around instance variables so nobody can set them to something [inappropriate].

Q: Why should you use setter methods instead of public instance variables?
A: Setter methods let you validate the parameter and decide if it's acceptable. You can reject invalid values, throw exceptions, or round to acceptable values. You can also change your mind later without breaking anyone's code.

C: The point to setters and getters is that you can [change your mind later], without breaking anybody else's [code].

Q: What are the benefits of encapsulation?
A: You protect data from inappropriate values, you can validate input in setters, and you can change implementation later without breaking other code. You maintain control over your instance variables.

C: Instance variables always get a [default value]. Integers get [0], floating points get [0.0], booleans get [false], and references get [null].

Q: What happens if you don't initialize an instance variable?
A: Instance variables always get a default value: integers get 0, floating points get 0.0, booleans get false, and object reference variables get null.

C: Instance variables are declared [inside a class] but not [within a method].

Q: What is the difference between instance variables and local variables?
A: Instance variables are declared inside a class but not within a method. Local variables are declared within a method. Instance variables get default values, but local variables must be initialized before use.

C: Local variables [MUST] be initialized before use. The compiler will [complain] if you try to use an uninitialized local variable.

Q: What happens if you try to use a local variable before initializing it?
A: The compiler will give you an error. Local variables do NOT get a default value and must be initialized before use.

C: Method parameters are virtually the same as [local variables], but they will never be [uninitialized].

Q: Do method parameters need to be initialized?
A: No. Method parameters are always initialized because the compiler guarantees that methods are called with arguments that match the parameters, and the arguments are automatically assigned to the parameters.

C: Use [==] to compare two primitives or to see if two references refer to the [same object].

Q: What does the == operator do?
A: The == operator compares the bits in two variables. For primitives, it checks if the values are the same. For references, it checks if two reference variables refer to the same object on the heap.

C: Use the [equals()] method to see if two [different objects] are equal.

Q: How do you check if two different String objects have the same characters?
A: Use the equals() method. The == operator only tells you if two references point to the same object, not if two different objects are meaningfully equivalent.

C: The [==] operator cares only about the pattern of [bits] in the variable.

Q: What is object equality?
A: Object equality depends on the type of object. Two different String objects with the same characters are meaningfully equivalent. The idea of equality for objects depends on what makes sense for that object type.

C: Any place where a particular value can be used, a [method call that returns that type] can be used.

Q: Can you use a method call in place of a value?
A: Yes. Any place where a particular value can be used, a method call that returns that type can be used. For example: int x = 3 + one.getSize();

C: You can pass [variables] into a method, as long as the [variable type] matches the [parameter type].

Q: What types of things can you pass as arguments to a method?
A: You can pass a literal value (2, 'c', etc.) or a variable of the declared parameter type. The value can also be implicitly promoted to a larger type.

C: Values passed in and out of methods can be [implicitly promoted] to a larger type or [explicitly cast] to a smaller type.

Q: Can you pass a byte where an int is expected?
A: Yes. You can return anything that can be implicitly promoted to the declared type. A byte fits into an int, so the caller won't care. You must use an explicit cast when the declared type is smaller than what you're trying to return.

C: Java doesn't require you to [acknowledge] a return value. You can [ignore] it.

Q: Do you have to do something with a method's return value?
A: No. Java doesn't require you to acknowledge a return value. You might call a method for the work it does inside the method rather than for what it returns.

Q: Can a method declare multiple return values?
A: Sort of. A method can declare only one return value. But if you want to return multiple values, the declared return type can be an array. You can stuff values into the array and pass it back.

C: If a method has parameters, you [must] pass arguments of the [right type] and [order].

Q: What are the rules for passing arguments to methods?
A: If a method has parameters, you must pass arguments of the right type and order. The number and type of values you pass must match the order and type of the parameters declared by the method.

C: A method [must] declare a return type. If a method declares a non-void return type, it [must] return a value compatible with the declared return type.

Q: What are the main bullet points about methods and instance variables?
A: Classes define what an object knows and does. Instance variables are state, methods are behavior. Methods can use instance variables so objects of the same type can behave differently. Methods can have parameters and return types. Values are passed by copy.