C: A [constructor] has the code that runs when you instantiate an object. It runs when you say [new] on a class type.

C: Every class you create has a [constructor], even if you don't write it [yourself].

Q: What is the difference between a constructor and a method?
A: A constructor must have the same name as the class, and must not have a return type. Methods can have any name and must have a return type (or void).

C: If you don't put a constructor in your class, the [compiler] will put in a [default constructor].

C: The default constructor is always a [no-arg] constructor.

Q: What happens if you write a constructor with arguments but don't write a no-arg constructor?
A: The compiler will not build a default constructor for you. If you want a no-arg constructor and you've already put in a constructor with arguments, you'll have to build the no-arg constructor yourself.

C: Overloaded constructors means you have [more than one] constructor in your class.

C: Overloaded constructors must have [different argument lists].

Q: What is the Stack and what lives there?
A: The Stack is where method invocations and local variables live. When a method is called, it goes into a stack frame at the top of the Stack. When the method completes, its stack frame is popped off the Stack.

Q: What is the Heap and what lives there?
A: The Heap is where ALL objects live. No matter where an object reference is declared or created, the object itself always goes on the Heap.

C: [Instance variables] are declared inside a class but not inside a method.

C: [Local variables] are declared inside a method, including method parameters.

C: All local variables live on the [stack], in the frame corresponding to the method where the variables are declared.

Q: Where do instance variables live?
A: Instance variables live within the object they belong to, on the Heap. When you say new on a class type, Java makes space on the Heap for all of the object's instance variables.

C: Object reference variables work just like [primitive] variables—if the reference is declared as a local variable, it goes on the [stack].

C: All objects live in the [heap], regardless of whether the reference is a local or instance variable.

Q: What is the role of superclass constructors in an object's life?
A: All the constructors in an object's inheritance tree must run when you make a new object. The superclass constructors run to build out the superclass parts of the object. For an object to be fully-formed, all the superclass parts of itself must be fully-formed.

C: When a constructor runs, it immediately calls its [superclass constructor], all the way up the chain until you get to the [Object] constructor.

Q: How do you invoke a superclass constructor?
A: You call super(). The call to super() must be the first statement in each constructor.

C: The only way to call a super constructor is by calling [super()].

Q: Can you pass arguments to a superclass constructor?
A: Yes. If your superclass constructor has arguments, you can pass something in to the super() call. For example, super(name) would pass the name parameter to the superclass constructor.

C: Every constructor can have a call to [super()] or [this()], but never both!

Q: What does this() do in a constructor?
A: this() is used to call another overloaded constructor in the same class. It must be the first statement in the constructor. This allows you to avoid duplicate code by having one "real" constructor that does the work, and other constructors that call it.

C: The call to [super()] must be the first statement in each constructor.

Q: Can the child exist before the parents?
A: No. The superclass parts of an object have to be fully-formed (completely built) before the subclass parts can be constructed. The superclass constructor must finish before its subclass constructor.

C: A [local variable] lives only within the method that declared the variable.

C: An [instance variable] lives as long as the object does. If the object is still alive, so are its instance variables.

Q: What is the difference between life and scope for local variables?
A: A local variable is alive as long as its Stack frame is on the Stack (until the method completes). A local variable is in scope only within the method in which the variable was declared. While a local variable is alive, its state persists, but it can be used only while that local variable's method is actually running.

Q: How does variable life affect object life?
A: An object's life depends entirely on the life of references referring to it. If the reference is considered "alive", the object is still alive on the Heap. If the reference dies, the object will die.

C: An object becomes eligible for [garbage collection] when its last live reference disappears.

Q: What are three ways to get rid of an object's reference?
A: 1) The reference goes out of scope, permanently. 2) The reference is assigned another object. 3) The reference is explicitly set to null.

C: Once an object is eligible for [garbage collection], you don't have to worry about reclaiming the memory that object was using.

Q: What is a null reference?
A: When you set a reference to null, you're deprogramming the remote control. You've got a remote control, but no object at the other end. If you use the dot operator on a null reference, you'll get a NullPointerException at runtime.

C: An object's life has no value, no meaning, no point, unless somebody has a [reference] to it.

Q: When does the Garbage Collector run?
A: You cannot predict when the Garbage Collector will run. If your program gets low on memory, GC will destroy some or all of the eligible objects to keep you from running out of RAM.

C: Your job is to make sure that you [abandon] objects when you're done with them, so that the garbage collector has something to reclaim.

Q: What happens when a Stack frame is popped off the Stack?
A: When a method completes and its Stack frame is popped off the Stack, all local variables in that frame are gone. If a local variable was the only reference to an object, that object is now abandoned on the Heap and becomes eligible for garbage collection.

C: Instance variables are assigned a [default value], even when you don't explicitly assign one. The default values are [0/0.0/false] for primitives, and [null] for references.

Q: Why should you always provide a no-arg constructor if you can?
A: To make it easy for programmers to make a working object. You can supply default values in the no-arg constructor so that objects can be created even when the programmer doesn't know what values to use.

C: A constructor looks like a method, but it's [not] a method.

Q: What is constructor chaining?
A: Constructor chaining is the process where all the constructors in an object's inheritance tree run when you make a new object. Each constructor invokes its superclass constructor until the Object constructor is reached.

C: Even [abstract] classes have constructors. Although you can never say new on an abstract class, an abstract class is still a superclass, so its constructor runs when someone makes an instance of a concrete subclass.

Q: What happens if the instance variable is a reference to an object?
A: Java makes space within the object only for the reference variable (the remote control) but not the object it refers to. The actual object the reference points to must be created separately with new.

C: No matter WHERE the object reference variable is declared, the object always always always goes on the [heap].

Q: Are constructors inherited?
A: No. Constructors are not inherited. Each class must have its own constructor.

C: If you write a constructor that takes arguments, and you still want a [no-arg] constructor, you'll have to build the no-arg constructor yourself!

C: As soon as you provide a constructor, ANY kind of constructor, the compiler [backs off] and says you're in charge of constructors now.

Q: Can a constructor be private?
A: Yes. Constructors can be public, protected, private, or default (which means no access modifier at all). A private constructor can only be called from within the same class.

C: Overloaded constructors means you have more than one constructor in your class, and the constructors MUST have [different argument lists].

Q: What determines if two constructors are different?
A: The variable type and order of the arguments. You can have two constructors that have identical types, as long as the order is different. What you name the parameter variable doesn't count.

C: The compiler gets involved in constructor-making in two ways: 1) If you don't provide a constructor, the compiler puts one in. 2) If you do provide a constructor but you do not put in the call to [super()], the compiler will put a call to super() in each of your overloaded constructors.

Q: What does the compiler-inserted call to super() look like?
A: It always looks like super() with no arguments. The compiler-inserted call to super() is always a no-arg call. If the superclass has overloaded constructors, only the no-arg one is called.

C: The best place to put initialization code is in the [constructor].

Q: Why use a constructor to initialize the state of an object?
A: If an object shouldn't be used until one or more parts of its state have been initialized, don't let anyone get a reference to a new object until you're finished initializing. The constructor runs before the object can be assigned to a reference, so you get a chance to step in and do things to get the object ready for use.

C: Most people use constructors to initialize the [state] of an object.

Q: What is the purpose of having a constructor with arguments?
A: To let the programmer using your class set the initial state of the object when it's created. This is better than requiring a two-step process (create the object, then call a setter method) because it ensures the object is never in an incomplete state.