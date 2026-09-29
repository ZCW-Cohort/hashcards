C: Variables come in two flavors: [primitive] and [reference].

Q: What are the four places where variables are used?
A: As object state (instance variables), as local variables (variables declared within a method), as arguments (values sent to a method by the calling code), and as return types (values sent back to the caller of the method).

C: Variables must have a [type] and a [name].

Q: Why does Java care about type?
A: Java won't let you do something dangerous like stuff a Giraffe reference into a Rabbit variable. It also won't let you put a floating point number into an integer variable unless you acknowledge to the compiler that you know you might lose precision.

C: A primitive variable value is the [bits representing the value], while a reference variable value is the [bits representing a way to get to an object on the heap].

Q: What are the eight primitive types in Java?
A: boolean, char, byte, short, int, long, float, and double.

C: The mnemonic for remembering primitive types is: [Be Careful, Bears Shouldn't Ingest Large Furry Dogs].

Q: What are the bit depths of the primitive types?
A: boolean is JVM-specific, char is 16 bits, byte is 8 bits, short is 16 bits, int is 32 bits, long is 64 bits, float is 32 bits, and double is 64 bits.

C: When declaring a float literal, you must use the ['f'] suffix because Java thinks anything with a floating point is a [double] by default.

Q: What happens when you try to put a value that's too large into a variable?
A: You get spillage. The compiler tries to prevent this if it can tell from your code that something's not going to fit in the container (variable) you're using.

C: You can't put an [int]-full of stuff into a [byte]-sized container without the compiler complaining.

Q: What are the three ways to assign a value to a variable?
A: Type a literal value after the equals sign, assign the value of one variable to another, or use an expression combining the two.

C: Variable names must start with a [letter], [underscore], or [dollar sign]. You can't start a name with a [number].

Q: What are reserved words?
A: Reserved words are keywords and other things that the compiler recognizes. You cannot use them as variable names, class names, or method names.

C: Java's primitive types are reserved words: [boolean] [char] [byte] [short] [int] [long] [float] [double].

Q: What is an object variable?
A: There is actually no such thing as an object variable. There's only an object reference variable.

C: An object reference variable holds bits that represent a [way to access an object], not the [object itself].

Q: What does the dot operator (.) do?
A: The dot operator gives you access to an object's state and behavior (instance variables and methods). You use it on a reference variable to access the thing after the dot.

C: Think of an object reference variable as a [remote control] for an object.

Q: What does it mean when a reference variable has a value of null?
A: It means the reference is not programmed to control anything. It's like a remote control that isn't programmed to any TV. The reference variable exists but doesn't refer to any object.

C: Objects live in one place and one place only—the [garbage collectible heap].

Q: How do you declare a reference variable?
A: You declare it with a type and name, just like primitives. For example: Dog myDog; This tells the JVM to allocate space for a reference variable of type Dog.

C: The three steps of object declaration, creation and assignment are: [declare a reference variable], [create an object], and [link the object and the reference].

Q: What is the syntax for creating a new object?
A: Use the new keyword followed by the class name and parentheses. For example: new Dog();

C: To assign an object to a reference variable, use: Dog myDog = [new Dog()];

Q: What happens if a reference variable is the only reference to an object and then it's set to null?
A: Nobody can get to that object anymore, which means it's eligible for garbage collection.

C: Arrays are always [objects], even if the array is declared to hold [primitives].

Q: How do you declare an array variable?
A: Use the type followed by square brackets and the variable name. For example: int[] nums; or Dog[] pets;

C: To create a new array with a specific length, use: new int[[7]];

Q: What do array elements contain when the array is first created?
A: For primitive arrays, elements get default values (0 for numeric types, false for boolean). For object arrays, elements are null references until you assign objects to them.

C: When you create an array of objects, you have an array of [references], but no actual [objects] yet.

Q: How do you access elements in an array?
A: Use array notation with the index in square brackets. For example: myDogs[0] or nums[2].

C: Arrays have a variable called [length] that gives you the number of elements in the array.

Q: Can you put a Cat into a Dog array?
A: No. Once you've declared an array, you can't put anything in it except things that are of the declared array type. The compiler won't let you put the wrong thing in an array.

C: Java cares about [type]. It won't let you put the wrong thing in an array based on the array's declared [type].

Q: How do you access a Dog's instance variable when the Dog is in an array?
A: Use array notation and the dot operator together. For example: myDogs[0].name or myDogs[0].bark();

C: A [byte] will always fit into an [int]-sized cup. This is known as an [implicit widening].

Q: What is a reference variable like?
A: A reference variable is like a remote control. Using the dot operator on a reference variable is like pressing a button on the remote control to access a method or instance variable.

C: With primitive variables, the value of the variable is the [value]. With reference variables, the value of the variable is bits representing a [way to get to a specific object].

Q: How big is a reference variable?
A: You don't know unless you're on the JVM's development team. All references for a given JVM will be the same size regardless of the objects they reference, but each JVM might represent references differently.

C: You [cannot] do arithmetic on a reference variable or increment it.

Q: What happens when you assign one reference variable to another?
A: The bits inside the first variable are copied, and that copy is stuffed into the second variable. Both variables then refer to the same object.

C: When two reference variables refer to the same object, you have [two remotes programmed to one TV].

Q: What happens to an object when there are no more references to it?
A: It becomes unreachable and eligible for garbage collection. The Garbage Collector can reclaim that memory space.

C: An [abandoned] object is one that has no more references and is [eligible for garbage collection].

Q: What is the difference between active references and reachable objects?
A: Active references are reference variables that currently hold a reference to an object. Reachable objects are objects that have at least one active reference pointing to them.

C: As long as an object has an [active reference], it is not eligible for [garbage collection].

Q: Can you have multiple reference variables referring to the same object?
A: Yes. You can have as many reference variables as you want all referring to the same object, like multiple remote controls programmed to the same TV.

C: Arrays give you fast [random access] by letting you use an [index position] to get to any element in the array.

Q: What is the first index position in a Java array?
A: 0 (zero). Arrays start with element 0.

C: In a Dog array (Dog[]), each element can hold a [remote control to a Dog], not the [Dog itself].

Q: What are the key points about arrays?
A: Arrays are always objects. Each element in an array is just a variable. You can have an array of primitives or an array of object references. The array itself is always an object, even if it holds primitives.

C: When you declare a variable as [final], once it is assigned a value, it can never be [reprogrammed] to anything else.

Q: What is null?
A: null is a value. It means the reference variable is like a remote control that isn't programmed to control anything. It's still a reference variable, but it doesn't refer to any object.

C: If you are the only reference to a particular object and then you're set to [null], that object is now eligible for [garbage collection].
