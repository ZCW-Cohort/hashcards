C: [Inheritance] allows you to put common code in a [superclass] and let [subclasses] inherit that code.

Q: What is the main benefit of inheritance?
A: Inheritance lets you avoid duplicate code. You can put common code in one place (the superclass), and when you need to change that behavior, you have to modify it in only one place. All subclasses automatically see the change.

C: A [subclass] extends a [superclass]. In Java, we say the subclass [extends] the superclass.

Q: What does it mean when we say a subclass extends a superclass?
A: When one class inherits from another, the subclass inherits from the superclass. The subclass inherits the members of the superclass, which means the instance variables and methods.

C: [Overriding] means that a subclass redefines one of its inherited methods when it needs to [change or extend] the behavior of that method.

Q: What is method overriding?
A: Overriding means that a subclass redefines one of its inherited methods when it needs to change or extend the behavior of that method. At runtime, the JVM knows exactly which version of the method to run based on the actual object type.

C: [Public] members are inherited, [private] members are not inherited.

Q: What access levels determine inheritance?
A: Public members are inherited. Private members are not inherited. When a subclass inherits a member, it is as if the subclass defined the member itself.

C: [Instance variables] are not overridden because they don't need to be. They don't define any special [behavior].

Q: Can you override instance variables?
A: No. Instance variables are not overridden because they don't need to be. They don't define any special behavior, so a subclass can give an inherited instance variable any value it chooses.

C: Use the [IS-A] test to verify that your inheritance hierarchy is valid. If X extends Y, then [X IS-A Y] must make sense.

Q: How do you know if you've designed your inheritance correctly?
A: Use the IS-A test. If "X IS-A Y" makes sense, both classes should probably live in the same inheritance hierarchy. The IS-A relationship works in only one direction. Triangle IS-A Shape makes sense, but Shape IS-A Triangle does not.

C: The IS-A relationship works [anywhere] in the inheritance tree. If class C extends class B, and B extends A, then C IS-A B and C IS-A [A].

Q: Does the IS-A test work only for direct superclass relationships?
A: No. The IS-A test works anywhere in the inheritance tree. If your inheritance tree is well-designed, the IS-A test should make sense when you ask any subclass if it IS-A any of its supertypes, not just its immediate superclass.

C: When you call a method on an object reference, you're calling the [most specific] version of the method for that object type. The [lowest one wins].

Q: Which version of an overridden method gets called?
A: The lowest one wins. When you call a method on an object reference, you're calling the most specific version of the method for that object type. The JVM starts looking first in the actual object's class, then walks back up the inheritance hierarchy until it finds a match.

C: [Polymorphism] means that the reference type can be a [superclass] of the actual object type.

Q: What is polymorphism in Java?
A: With polymorphism, the reference type can be a superclass of the actual object type. You can declare a reference variable of a supertype and assign a subclass object to it. This lets you write flexible code that doesn't have to change when you introduce new subclass types.

C: When you declare a reference variable, any object that passes the [IS-A test] for the declared type can be assigned to that reference.

Q: What types of objects can be assigned to a reference variable?
A: When you declare a reference variable, any object that passes the IS-A test for the declared type of the reference variable can be assigned to that reference. Anything that extends the declared reference variable type can be assigned to the reference variable.

C: With polymorphism, you can write code that doesn't have to [change] when you introduce new [subclass] types into the program.

Q: Why is polymorphism valuable for flexible code?
A: With polymorphism, you can write code that doesn't have to change when you introduce new subclass types. If you write methods using arguments declared as the superclass type, your code can handle any subclass. Others can add new subclass types and your methods will still work.

C: Arguments must be the [same], and return types must be [compatible] when overriding a method.

Q: What are the rules for overriding method arguments and return types?
A: The arguments must be the same, and return types must be compatible. Whatever the superclass takes as an argument, the overriding method must use that same argument. The return type must be either the same type, or a subclass type.

C: An overriding method cannot be [less accessible] than the method it overrides.

Q: Can you make an overriding method more restrictive?
A: No. The method can't be less accessible. The access level must be the same, or friendlier. You can't override a public method and make it private.

C: [Overloading] means having two methods with the same name but different [argument lists]. There's no [polymorphism] involved.

Q: What is method overloading?
A: Method overloading is having two methods with the same name but different argument lists. Period. There's no polymorphism involved with overloaded methods. It's just a convenience for callers.

C: To overload a method, you MUST change the [argument list], although you can change the [return type] to anything.

Q: What must you change to create a valid overload?
A: You MUST change the argument list. You can't change ONLY the return type. If only the return type is different, it's not a valid overload. To overload a method, you must change the argument list, although you can also change the return type to anything.

C: When designing with inheritance, use it when one class is a more [specific type] of a superclass, or when you have [behavior] that should be shared.

Q: When should you use inheritance?
A: Use inheritance when one class is a more specific type of a superclass. Consider inheritance when you have behavior (implemented code) that should be shared among multiple classes of the same general type. This makes for easier maintenance and extensibility.

C: DO NOT use inheritance just to [reuse code] if the relationship violates the [IS-A] test.

Q: When should you NOT use inheritance?
A: Do not use inheritance just to reuse code from another class if the subclass and superclass do not pass the IS-A test. Do not use inheritance if the relationship doesn't make sense. The relationship should be that the subclass is a more specific type of the superclass.

C: Inheritance lets you guarantee that all classes grouped under a certain supertype have all the [methods] that the supertype has.

Q: How does inheritance establish a contract?
A: Inheritance lets you guarantee that all classes grouped under a certain supertype have all the methods that the supertype has. You define a common protocol for a set of classes related through inheritance. Any subclass of that supertype can be substituted where the supertype is expected.

C: You can have polymorphic [arguments] and [return types].

Q: Can polymorphism work with method parameters and return values?
A: Yes. You can have polymorphic arguments and return types. If you declare a method parameter as a supertype, you can pass in any subclass object. The method will work on whatever subclass is passed in at runtime.

C: A [final] class cannot be extended. A [final] method cannot be overridden.

Q: What does the final keyword do for classes and methods?
A: A final class means it's the end of the inheritance line - nobody can extend it. A final method cannot be overridden. Use final when you need security - the security of knowing that methods will always work the way you wrote them because they can't be overridden.

C: The keyword [super] lets you invoke the superclass version of a method from within the overriding method.

Q: How can you call the superclass version of an overridden method?
A: Use the keyword super. In your subclass overriding method, you can call the superclass version using super. For example: super.roam() calls the inherited version of roam(), then you come back and finish with your own subclass-specific code.

C: When you override a method, you're agreeing to fulfill the [contract] defined by the superclass method signature.

Q: What contract must an overriding method fulfill?
A: When you override a method from a superclass, you're agreeing to fulfill the contract. The arguments and return types of your overriding method must look to the outside world exactly like the overridden method in the superclass. The methods are the contract.

C: A [HAS-A] relationship means that one class has a reference to another as an [instance variable].

Q: What is a HAS-A relationship?
A: A HAS-A relationship means that one class has a reference to another as an instance variable. For example, Bathroom HAS-A Tub means Bathroom has a Tub instance variable. Tub and Bathroom are related, but not through inheritance.

C: The compiler looks at the [reference type] to decide whether you can call a method. At runtime, the JVM looks at the [actual object] on the heap.

Q: How does the compiler and JVM handle polymorphic method calls?
A: The compiler looks at the reference type to decide whether you can call a particular method on that reference. But at runtime, the JVM looks not at the reference type but at the actual object on the heap. The overriding method in the actual object type is the one that runs.

C: Polymorphic [arrays] let you put any subclass of the declared array type into the array.

Q: How do polymorphic arrays work?
A: When you declare an array of a supertype, you can put any subclass of that supertype into the array. Then you can loop through the array and call methods, and the JVM will run the correct overridden version based on the actual object type at each array position.

C: The five steps to better class design are: look for common [attributes and behaviors], design a class that represents the common [state and behavior], decide if subclasses need [specific behaviors], look for more opportunities to use [abstraction], and finish the class [hierarchy].

Q: What are the five steps to designing an inheritance hierarchy?
A: 1) Look for objects that have common attributes and behaviors. 2) Design a class that represents the common state and behavior. 3) Decide if a subclass needs behaviors that are specific to that particular subclass type. 4) Look for more opportunities to use abstraction by finding subclasses that might need common behavior. 5) Finish the class hierarchy.
