C: An [abstract class] means that nobody can ever make a new instance of that class. You can still use it as a [reference type] for polymorphism.

Q: What does it mean when a class is marked as abstract?
A: An abstract class cannot be instantiated. You cannot say "new" on that type. The compiler will stop any code from ever creating an instance of that type. However, you can still use that abstract class as a declared reference type for polymorphic purposes.

C: To make a class abstract, put the keyword [abstract] before the class declaration.

Q: How do you prevent a class from being instantiated?
A: Mark the class with the abstract keyword before the class declaration. For example: abstract class Canine extends Animal { }. This tells the compiler that nobody can make objects of that type.

C: An abstract class has virtually no use unless it is [extended].

Q: What is the purpose of an abstract class?
A: An abstract class has virtually no use, no value, no purpose in life unless it is extended. With an abstract class, the guys doing the work at runtime are instances of a subclass of your abstract class.

C: A class that's not abstract is called a [concrete] class.

Q: What is a concrete class?
A: A class that's not abstract is called a concrete class. Concrete classes are those that are specific enough to be instantiated. A concrete class just means that it's OK to make objects of that type.

C: [Abstract methods] have no body and end with a [semicolon].

Q: What is an abstract method?
A: An abstract method has no body - no curly braces, just a method declaration that ends with a semicolon. For example: public abstract void eat();. Abstract methods exist solely for polymorphism.

C: If you declare an abstract method, you MUST mark the [class] abstract as well.

Q: If a class has even one abstract method, what must you do?
A: You must mark the class abstract. You can't have an abstract method in a non-abstract class. But you can mix both abstract and non-abstract methods in the abstract class.

C: You MUST implement all [abstract methods] in the first [concrete] subclass.

Q: What must a concrete subclass do with abstract methods?
A: The first concrete class in the inheritance tree must implement all abstract methods. Abstract methods don't have a body, so the first concrete subclass must provide a body for all abstract methods inherited from abstract superclasses.

C: Implementing an abstract method is just like [overriding] a method.

Q: How do you implement an abstract method?
A: Implementing an abstract method is just like overriding a method. You must provide a body - create a non-abstract method in your class with the same method signature and a return type that is compatible with the declared return type of the abstract method.

C: Every class in Java extends class [Object].

Q: What is the superclass of all classes in Java?
A: Every class in Java extends class Object. Class Object is the mother of all classes; it's the superclass of everything. Even if you don't explicitly extend anything, the compiler makes your class extend Object.

C: Any class that doesn't explicitly extend another class, [implicitly] extends Object.

Q: If a class doesn't use the extends keyword, what does it extend?
A: Any class that doesn't explicitly extend another class, implicitly extends Object. The compiler automatically makes it extend Object. If your class already extends something, the compiler walks up the tree until it finds a class that extends Object.

C: Class Object has methods including [equals()], [getClass()], [hashCode()], and [toString()].

Q: What are some key methods in class Object?
A: Class Object has equals() to compare objects, getClass() to tell you the actual class type, hashCode() to get a hashcode for the object, and toString() to print out a String message for that object. Every class inherits these methods.

C: When you put an object into an ArrayList<Object>, it goes in as any type but comes out as type [Object].

Q: What type do objects have when retrieved from ArrayList<Object>?
A: Everything comes out of an ArrayList<Object> as a reference of type Object, regardless of what the actual object is or what the reference type was when you added the object to the list. Objects come out acting like generic instances of class Object.

C: The compiler decides whether you can call a method based on the [reference type], not the actual [object type].

Q: How does the compiler determine which methods you can call?
A: The compiler checks the class of the reference variable, not the class of the actual object at the other end of the reference. You can call a method on an object only if the class of the reference variable has that method.

C: To cast an object reference back to its real type, use parentheses: [(Dog) o].

Q: How do you cast an object reference back to its original type?
A: Use a cast with parentheses and the type name. For example: Dog d = (Dog) o; This copies the Object reference and forces that copy to go into a Dog reference variable. If you're not sure it's the right type, use instanceof to check first.

C: The [instanceof] operator checks if an object is of a particular type before you cast it.

Q: How can you check if an object is safe to cast?
A: Use the instanceof operator. For example: if (o instanceof Dog) { Dog d = (Dog) o; }. This checks if the object is really a Dog before attempting the cast, preventing a ClassCastException at runtime.

C: An object contains [everything] it inherits from each of its superclasses.

Q: What does an object contain in terms of inheritance?
A: An object contains everything it inherits from each of its superclasses. Every object is also an instance of class Object. When you say new Snowboard(), you get a single object on the heap that wraps itself around an inner core representing the Object portion of itself.

C: Polymorphism means [many forms]. You can treat a Snowboard as a Snowboard or as an [Object].

Q: What does polymorphism mean?
A: Polymorphism means "many forms." You can treat an object in multiple ways - a Snowboard can be treated as a Snowboard or as an Object. The reference type determines which methods you can call, acting like a remote control with different numbers of buttons.

C: A Java [interface] is like a 100% pure [abstract class]. All methods in an interface are [abstract].

Q: What is a Java interface?
A: A Java interface is like a 100% pure abstract class. All methods in an interface are abstract, so any class that IS-A that interface type must implement all the methods. An interface solves the multiple inheritance problem.

C: To define an interface, use the keyword [interface] instead of class.

Q: How do you define an interface in Java?
A: Use the keyword interface instead of the word class. For example: public interface Pet { void beFriendly(); void play(); }. All interface methods are implicitly public and abstract.

C: To implement an interface, use the keyword [implements].

Q: How does a class implement an interface?
A: Use the keyword implements followed by the interface name. For example: public class Dog extends Canine implements Pet { }. You still get to extend a class when you implement an interface.

C: A class can extend only [one] class, but can implement [multiple] interfaces.

Q: How many classes can you extend and how many interfaces can you implement?
A: A class can extend only one class (single inheritance), but can implement multiple interfaces. For example: public class Dog extends Animal implements Pet, Saveable, Paintable { }. This is Java's solution to multiple inheritance.

C: Classes from [different] inheritance trees can implement the [same] interface.

Q: Can classes from different inheritance trees implement the same interface?
A: Yes! Classes from different inheritance trees can implement the same interface. The only requirement is that the objects are from a class that implements the interface. This is crucial - a RoboDog from the Robot tree and a Dog from the Animal tree can both implement Pet.

C: Interface methods are implicitly [public] and [abstract], so typing those keywords is optional.

Q: Do you need to type public and abstract for interface methods?
A: No, it's optional. Interface methods are implicitly public and abstract, so you don't need to type those keywords. However, some programmers include them for clarity.

C: Java doesn't allow [multiple inheritance] because of the [Deadly Diamond of Death] problem.

Q: Why doesn't Java allow multiple inheritance?
A: Because of the Deadly Diamond of Death. If a class could inherit from two classes that both have the same method or instance variable, there would be ambiguity about which version to use. Interfaces solve this by making all methods abstract.

C: Use the [super] keyword to invoke the superclass version of an overridden method.

Q: How do you call the superclass version of an overridden method?
A: Use the super keyword. For example: super.runReport(); The super keyword is a reference to the superclass portion of an object. This lets you extend the functionality rather than completely replace it.

C: Make a [class] when it doesn't pass the IS-A test for any other type.

Q: When should you make a new standalone class?
A: Make a class that doesn't extend anything (other than Object) when your new class doesn't pass the IS-A test for any other type. It's a completely new type that doesn't specialize anything else.

C: Make a [subclass] only when you need to make a more [specific] version of a class.

Q: When should you make a subclass?
A: Make a subclass (extend a class) only when you need to make a more specific version of a class and need to override or add new behaviors. The subclass should pass the IS-A test for the superclass.

C: Use an [abstract class] when you want to define a [template] for a group of subclasses.

Q: When should you use an abstract class?
A: Use an abstract class when you want to define a template for a group of subclasses, and you have at least some implementation code that all subclasses could use. Make the class abstract when you want to guarantee that nobody can make objects of that type.

C: Use an [interface] when you want to define a [role] that other classes can play.

Q: When should you use an interface?
A: Use an interface when you want to define a role that other classes can play, regardless of where those classes are in the inheritance tree. Interfaces allow unrelated classes to implement the same contract.

C: The inheritance IS-A relationship works in only [one] direction.

Q: Does the IS-A relationship work both ways?
A: No, the inheritance IS-A relationship works in only one direction. Triangle IS-A Shape makes sense, so Triangle can extend Shape. But Shape IS-A Triangle does not make sense, so Shape should not extend Triangle.

C: [Public] members are inherited, [private] members are not inherited.

Q: Which members are inherited by a subclass?
A: Public members are inherited. Private members are not inherited. A subclass inherits the public instance variables and methods of the superclass, but does not inherit private members.

C: When you design with inheritance, put common code in [one place] and let subclasses [inherit] it.

Q: What is a key benefit of inheritance for code reuse?
A: You avoid duplicate code by putting common code in one place (the superclass) and letting subclasses inherit it. When you need to change that behavior, you modify it in only one place, and all subclasses automatically see the change.

C: DO NOT use inheritance just to [reuse code] if the relationship violates the [IS-A] test.

Q: When should you NOT use inheritance?
A: Do not use inheritance just so you can reuse code from another class if the relationship between the superclass and subclass violates the IS-A test. If the classes don't have a true IS-A relationship, use composition (HAS-A) instead.

C: A [HAS-A] relationship means one class has a reference to another as an [instance variable].

Q: What is a HAS-A relationship?
A: A HAS-A relationship means that one class has a reference to another class as an instance variable. For example, Bathroom HAS-A Tub means Bathroom has a Tub instance variable. This is composition, not inheritance.

C: The [super] keyword is a reference to the [superclass] portion of an object.

Q: What does the super keyword represent?
A: The super keyword is a reference to the superclass portion of an object. When subclass code uses super, as in super.runReport(), the superclass version of the method will run. This allows you to extend rather than replace behavior.
