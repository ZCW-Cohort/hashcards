C: The keyword [static] lets a method run without any instance of the class.

C: A [static] method means behavior not dependent on an instance variable, so no instance/object is required. Just the [class].

Q: How do you call a static method?
A: Use the class name rather than an object reference variable. For example, Math.min(88,86) rather than creating an instance of Math.

Q: Why can't you make an instance of the Math class?
A: The Math constructor is marked private. You can NEVER say 'new' on the Math class to make a new Math object.

C: Static methods run [without] any instance of the class.

Q: Can a static method access instance variables?
A: No. A static method can't refer to any instance variables of the class. The static method doesn't know which instance's variable value to use.

C: Static methods can't use [non-static] (instance) variables.

C: Static methods can't use [non-static] methods, either.

Q: What is a static variable?
A: A static variable is a variable shared by all members of a given class. There is only one copy of a static variable in a class, rather than one copy per each individual instance for instance variables.

C: Static variable: value is the [same] for ALL instances of the class.

C: Instance variables: [1] per instance. Static variables: [1] per class.

Q: When are static variables initialized?
A: Static variables are initialized when a class is loaded. A class is loaded because the JVM decides it's time to load it, typically when somebody's trying to make a new instance of the class for the first time, or use a static method or variable of the class.

C: All static variables in a class are initialized [before] any object of that class can be created.

C: Static variables in a class are initialized [before] any static method of the class runs.

Q: What are the default values for static and instance variables?
A: Primitive integers (long, short, etc.): 0, primitive floating points (float, double): 0.0, boolean: false, object references: null.

C: A variable marked [final] means that once initialized it can never change.

C: A [static final] variable is a constant.

Q: How do you initialize a final static variable?
A: Either at the time you declare it (public static final int FOO_X = 25;) or in a static initializer block.

C: Constant variable names should be in [all caps].

Q: What is a static initializer?
A: A static initializer is a block of code that runs when a class is loaded, before any other code can use the class. It's a great place to initialize a static final variable.

C: A [final] variable means you can't change its value.

C: A [final] method means you can't override the method.

C: A [final] class means you can't extend the class (i.e. you can't make a subclass).

Q: Why would you make a class final?
A: For security. You can't make a subclass of String, for example. If you need to count on a particular implementation of the methods in a class, make the class final.

Q: Can a non-static method access a static variable?
A: Yes. A non-static method in a class can always call a static method in the class or access a static variable of the class.

C: A static method should be called using the [class] name rather than an object reference variable.

C: A static method can be invoked [without] any instances of the method's class on the heap.

Q: When should you use a static method?
A: A static method is good for a utility method that does not (and will never) depend on a particular instance variable value.

C: A static method is [not] associated with a particular instance—only the class—so it cannot access any instance variable values of its class.

C: A static method cannot access a [non-static] method, since non-static methods are usually associated with instance variable state.

Q: How can you prevent a class from being instantiated?
A: Mark the constructor private. If you have a class with only static methods, and you do not want the class to be instantiated, you can mark the constructor private.

C: A [static variable] is a variable shared by all members of a given class. There is only one copy of a static variable in a class.

Q: What are wrapper classes?
A: There's a wrapper class for every primitive type. The wrapper classes let you treat a primitive like an object. For example, Integer is the wrapper for int, Boolean for boolean, Character for char.

C: When you need to treat a primitive like an object, [wrap] it.

Q: How do you wrap a primitive value?
A: Give the primitive to the wrapper constructor. For example: int i = 288; Integer iWrap = new Integer(i);

Q: How do you unwrap a value?
A: Call the appropriate method on the wrapper object. For example: int unWrapped = iWrap.intValue(); All wrappers work similarly (booleanValue(), charValue(), etc.).

C: Before Java 5.0, you cannot put a [primitive] directly into a collection like ArrayList or HashMap.

C: [Autoboxing] does the conversion from primitive to wrapper object automatically.

Q: What is autoboxing?
A: The autoboxing feature added to Java 5.0 automatically converts primitives to wrapper objects and vice versa. You can add an int directly to an ArrayList<Integer> and the compiler handles the wrapping.

C: Autoboxing works with method [arguments], [return] values, [boolean] expressions, [operations] on numbers, and [assignments].

Q: How do you convert a String to a primitive value?
A: Use the wrapper class parse methods. For example: int x = Integer.parseInt(s); double d = Double.parseDouble("420.24"); boolean b = Boolean.parseBoolean("True");

Q: What happens if you try to parse a String that can't be converted to a number?
A: You'll get a NumberFormatException at runtime. Every method or constructor that parses a String can throw a NumberFormatException.

Q: How do you turn a primitive number into a String?
A: The easiest way is to concatenate the number to an existing String: String doubleString = "" + d; You can also use a static method: String doubleString = Double.toString(d);

C: Formatting numbers and dates is handled through a [Formatter] class in java.util.

Q: How do you format a number with commas?
A: Use String.format() with formatting instructions. For example: String s = String.format("%,d", 1000000000); produces "1,000,000,000".

C: The percent (%) sign in a format String represents [the argument to be formatted].

Q: What are the two main parts of formatting?
A: 1) Formatting instructions - special format specifiers that describe how the argument should be formatted. 2) The argument to be formatted.

C: A format specifier can have up to [five] different parts: %[argument number][flags][width][.precision]type.

C: The only required format specifier is for [TYPE].

Q: What are the most common type specifiers for numbers?
A: %d for decimal integer and %f for floating point. You typically combine %f with a precision indicator like %.2f for two decimal places.

C: [%d] formats as decimal, [%f] as floating point, [%x] as hexadecimal, [%c] as character.

Q: How do you format a date?
A: Date formats use a two-character type that starts with "t". For example: String.format("%tc", new Date()) for complete date and time, or %tr for just the time.

C: The angle-bracket [<] in a format specifier tells the formatter to use the [previous argument] again.

Q: Should you use Date or Calendar for date manipulation?
A: For a time-stamp of "now", use Date. But for everything else, use Calendar.

C: The Date class is great for getting a [time stamp], but most of Date's methods have been [deprecated].

Q: How do you get a Calendar instance?
A: You can't instantiate Calendar directly (it's abstract). Instead use: Calendar cal = Calendar.getInstance();

C: Calendar is an [abstract] class, so you always work with a concrete subclass like [GregorianCalendar].

Q: What are the key concepts for working with Calendar objects?
A: 1) Fields hold state (year, month, etc.). 2) Dates and times can be incremented using add() and roll(). 3) Dates and times can be represented in milliseconds for precise calculations.

C: The [add()] method adds or subtracts time from a calendar's field and can change larger fields. The [roll()] method adds or subtracts time without changing larger fields.

Q: What's the difference between add() and roll() in Calendar?
A: add() will change larger fields if needed (adding 35 days to Jan 7 gives you Feb 11). roll() will not change larger fields (rolling 35 days keeps you in the same month).

C: Full moons happen every [29.52] days or so.

Q: What are static imports?
A: Static imports let you import static classes, static variables, or enums so you can use them without the class name prefix. For example: import static java.lang.System.out; lets you use out.println() instead of System.out.println().

C: Static imports exist only to save you some [typing].

Q: What's the downside of static imports?
A: If you're not careful, using them can make your code a lot harder to read. Naming conflicts can occur if you have two different classes with methods of the same name.

C: Use static imports [carefully]: they can make your code confusing to read.

Q: When is it appropriate to use static imports?
A: If you're only using a static member a few times, avoid static imports for readability. If you're using a static member a lot (like doing lots of Math calculations), it's probably OK to use the static import.

C: Static variables are more [efficient]: one per class instead of one per instance.

C: The [out] in System.out is a static variable of the System class.

Q: What's one major criticism of static variables and methods?
A: They're considered un-object-oriented. Static variables are like global variables, and abuse of statics is often the mark of an immature OO programmer who is thinking procedurally instead of about object state.