Q: What is the main difference between procedural programming and object-oriented programming?
A: In procedural programming, code is organized around procedures and functions. In OO programming, code is organized around objects that combine data (state) and behavior (methods), allowing for better extensibility and maintainability without touching previously tested code.

C: A [class] is a blueprint for an object, while an [object] is an instance created from that class.

Q: What are instance variables?
A: Instance variables are things an object knows about itself. They represent an object's state and can have unique values for each object of that type.

Q: What are methods?
A: Methods are things an object can do. They represent an object's behavior and operate on the object's data.

C: When you design a class, think about the [objects] that will be created from that class type.

Q: What is inheritance in Java?
A: Inheritance is a relationship where a subclass inherits instance variables and methods from a superclass. The superclass contains common features, while subclasses can have more specific implementations.

C: The `Shape` class is called the [superclass], and `Square`, `Circle`, `Triangle`, and `Amoeba` are its [subclasses].

Q: What is method overriding?
A: Overriding means that a subclass redefines one of its inherited methods when it needs to change or extend the behavior of that method from the superclass.

C: At runtime, the [JVM] knows exactly which method to run when someone tells an object to perform an action.

Q: What are the two main uses of the `main()` method?
A: To test your real class, and to launch/start your Java application.

C: In a true OO application, you need [objects] talking to other [objects], as opposed to a static `main()` method creating and testing objects.

Q: What is the dot operator (.) used for?
A: The dot operator gives you access to an object's state and behavior - its instance variables and methods.

C: To create an object, you use the [new] keyword followed by the class name and parentheses.

Q: What is the Garbage-Collectible Heap?
A: The heap is an area of memory where all objects live in Java. When the JVM can see that an object can never be used again, it becomes eligible for garbage collection, and the Garbage Collector can reclaim that memory space.

C: Each object made from a class can have its own values for the [instance variables] of that class.

Q: What happens when a class inherits from a superclass?
A: If the superclass has functionality, then the subclasses automatically get that same functionality. Subclasses inherit the methods and instance variables of the superclass.

C: [Object-oriented] programming lets you extend a program without having to touch previously-tested, working [code].

Q: How do you make a class?
A: You write a class definition that includes instance variables (state) and methods (behavior), then compile it from a `.java` file.

Q: What is a Java program?
A: A Java program is a pile of classes (or at least one class). In a Java application, one of the classes must have a main method used to start up the program.

C: You can bundle all of your application files into a [Java Archive] -- a .jar file -- based on the pkzip format.

Q: What makes procedural code harder to maintain when requirements change?
A: In procedural code, when specifications change, you often have to modify and retest existing procedures. This can break previously working code and requires extensive retesting.

Q: What is the relationship between superclasses and subclasses in terms of abstraction?
A: Superclasses are more abstract and contain common features, while subclasses are more specific and can override or extend the behavior of the superclass.

C: Instance variables and methods are designed as part of the [class], but objects have instance variables and methods.

Q: How does object-oriented design help with flexibility and extensibility?
A: OO design allows you to add new object types (classes) without modifying existing code. New classes can inherit from existing classes and override methods as needed for specific behavior.

C: At runtime, a Java program is nothing more than [objects] 'talking' to other [objects].

Q: What does it mean that a class is like a template?
A: A class defines the structure and behavior that all objects of that type will have, just like a template or blueprint defines what will be created from it.

C: The [Math] class contains public static methods like `random()` that can be accessed from anywhere in the program.

C: Methods that are marked as [public] and [static] behave much like global functions and can be called from any code in any class.

Q: What is the analogy between objects and Rolodex cards?
A: Each Rolodex card has the same blank fields (instance variables), and when you fill out a card you create an instance (object) with its own unique data. The methods are the things you do to a card like getName() or changeName().

C: In Java, everything goes in a [class], even constants and static methods.

Q: How do you access an object's methods and variables?
A: You use the dot operator (.) on a reference to the object, followed by the method name or variable name.

C: Instance variables represent an object's [state], while methods represent an object's [behavior].

C: To mark a variable as a globally-available constant, declare it as [public], [static], and [final].

Q: Why is it better to have objects talk to other objects instead of doing everything in `main()`?
A: Having objects interact with each other is true object-oriented design. It provides better encapsulation, reusability, and maintainability compared to putting all logic in a static `main()` method.
