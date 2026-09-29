C: The Java Standard Edition ships with [hundreds] of pre-built classes in the [Java API].

Q: What is the Java API and why is it important?
A: The Java API (Application Programming Interface) is the core Java library - a giant pile of classes waiting for you to use like building blocks. You don't have to reinvent the wheel; you can write only the parts that are truly custom for your application.

C: [ArrayList] is a class in the [java.util] package that can grow and shrink dynamically.

Q: What problem does ArrayList solve that arrays cannot?
A: Arrays can't change their size - once created, they're stuck at that size. ArrayList resizes dynamically to whatever size is needed. It grows when objects are added and shrinks when objects are removed.

C: To add something to an ArrayList, use [add()]. To remove something, use [remove()].

Q: What are the key ArrayList methods for basic operations?
A: add() adds an object to the list, remove() removes an object (by index or by object), contains() checks if an object is in the list, isEmpty() checks if the list is empty, indexOf() finds the position of an object (returns -1 if not found), size() returns the number of elements, and get() retrieves an object at a specific index.

C: ArrayList uses [angle bracket] syntax to declare the type of objects it can hold, like ArrayList<[String]>.

Q: How do you declare an ArrayList that holds only String objects?
A: ArrayList<String> myList = new ArrayList<String>(). The <String> in angle brackets is a "type parameter" that tells the compiler this list will hold only String objects.

C: Classes in the Java API are grouped into [packages].

Q: What are packages in Java and why are they important?
A: Packages group related classes together. They help organize the library, provide name-scoping to prevent collisions if multiple programmers create classes with the same name, and provide a level of security by restricting access to classes in the same package.

C: The full name of a class includes both the [package name] and the [class name].

Q: What is the full name of the ArrayList class?
A: java.util.ArrayList. The package name is java.util and the class name is ArrayList.

C: To use a class from a package other than java.lang, you must either [import] it at the top of your file or type the [full name] everywhere you use it.

Q: What are the two ways to use a class from the Java API?
A: Either put an import statement at the top of your source code (like import java.util.ArrayList;) or type the full name every place you use the class (like java.util.ArrayList<Dog> list = new java.util.ArrayList<Dog>()).

C: The [java.lang] package is automatically imported - you never have to import String, System, or Math.

Q: Why don't you have to import the String class or System class?
A: Because they're in the java.lang package, which is automatically pre-imported for free. The classes in java.lang are so fundamental that you don't have to use the full name.

C: An [import] statement saves you from typing but does NOT make your class [bigger] or [slower].

Q: Does an import statement compile the imported class into your code?
A: No. An import is not like a C include. It simply saves you from typing the full name. Your code doesn't become bloated or slower from too many imports - an import is just the way you give Java the full name of a class.

C: ArrayList's indexOf() method returns [-1] if the object is not found in the list.

Q: What does ArrayList's indexOf() method return if the object is not in the list?
A: It returns -1. This allows you to use indexOf() both to check if an object is in the ArrayList AND to get its index at the same time if the object is there.

C: Arrays use special [bracket] syntax, but ArrayList is a plain old [object] that uses regular method calls.

Q: What's the difference between array syntax and ArrayList syntax?
A: Arrays use special bracket syntax (like myArray[1]) that you won't use anywhere else. ArrayList is a regular object, so you use normal method calls with the dot operator (like myList.get(1)).

C: Unlike arrays, you don't have to know the [size] of an ArrayList when you create it.

Q: Do you need to specify the size of an ArrayList when you create it?
A: No. You just make an object of type ArrayList. It never needs to know how big it should be because it grows and shrinks as objects are added or removed.

C: The [&& ] operator means "and" and the [||] operator means "or" in boolean expressions.

Q: What do the && and || operators do in Java?
A: && is the "and" operator - both sides must be true for the expression to be true. || is the "or" operator - if either side is true, the whole expression is true.

C: The && and || operators are [short circuit] operators - they stop evaluating as soon as the result is known.

Q: What does "short circuit" mean for the && and || operators?
A: With &&, if the left side is false, it stops immediately without checking the right side. With ||, if the left side is true, it declares the entire statement true without checking the right side. This can prevent errors like checking a null reference.

C: The [! ] operator means "not" and can be used to negate a boolean expression.

Q: How do you express "not equal" in Java?
A: For primitives, use != (like model != 2000). For objects, use ! with equals() (like !brand.equals("X")). The ! operator means "not".

C: Packages that begin with [javax] started life as [extensions] and then got promoted to the standard library.

Q: What does it mean when a package name starts with javax?
A: The "x" indicates it started as a standard extension (like javax.swing for Swing GUI). When extensions get promoted to the standard library, they normally would change from javax to java, but Swing kept javax to avoid breaking existing code.

C: When you have a bug, you can count a hit multiple times by not [removing] it or not [checking] if it was already hit.

Q: What was the bug in the SimpleDotCom game?
A: The bug allowed the user to guess the same cell multiple times and get credit for multiple hits. The game counted every guess as a hit without checking whether that cell location had already been hit.

C: The fixed DotCom code uses ArrayList's [indexOf()] to check if a guess is in the list and [remove()] to eliminate it if hit.

Q: How does the fixed DotCom code prevent counting the same hit twice?
A: It uses indexOf() to find if the user guess is in the ArrayList. If the index is >= 0, it removes that cell from the ArrayList with remove(). Once removed, that cell can't be hit again.

C: The enhanced for loop uses the syntax: for ([Type element] : [collection]).

Q: What is the syntax of an enhanced for loop in Java?
A: for (Type element : collection) { }. For example: for (String name : nameArray) { }. It reads as "for each element in the collection, assign the element to the variable and run the loop body."

C: To browse the Java API, use a [reference book] or the [HTML API documentation].

Q: What are two ways to learn what's in the Java API?
A: Browse a reference book to discover classes by flipping through pages, or use the HTML API documentation that comes with Java to get detailed information about classes and methods.

C: The HTML API docs show you the [package name], [class description], and detailed [method] information including what happens in edge cases.

Q: What important information do the HTML API docs provide that method signatures alone don't?
A: The API docs tell you what happens in edge cases. For example, they tell you that indexOf() returns -1 if the object isn't in the ArrayList. Looking at just the method signature wouldn't tell you that.

C: The DotComBust game has [three] main classes: [DotComBust] (the game), [DotCom] (the objects), and [GameHelper] (the helper).

Q: What are the three main classes in the DotComBust game and their roles?
A: DotComBust is the game class that makes DotComs, gets user input, and plays until all DotComs are dead. DotCom represents the actual DotCom objects that know their name, location, and how to check a user guess. GameHelper is the helper class that gets user command-line input and makes DotCom locations.

C: The DotComBust game uses a [7 x 7 grid] with [three] DotComs, each occupying [three] cells.

Q: What is the structure of the DotComBust game grid?
A: It's a 7 x 7 grid (like a battleship board) with three DotComs. Each DotCom occupies three consecutive cells, either vertically or horizontally. Cells are named with a letter (A-G) and number (0-6), like "A3" or "D5".

C: [Prepcode] describes what to do, not how to do it. [Test code] validates the implementation. [Real code] is the actual Java implementation.

Q: What are the three types of code you write when developing a class?
A: Prepcode (a form of pseudocode to plan the logic without worrying about syntax), test code (a class or methods to test and validate the real code), and real code (the actual Java implementation).

C: Write [test code] before you implement the methods, following Extreme Programming practices.

Q: When should you write test code according to XP (Extreme Programming)?
A: Write test code BEFORE you implement the methods. The act of thinking through and writing test code helps clarify what the method needs to do. As soon as implementation is done, you already have test code waiting to validate it.

C: The [private] keyword restricts access to instance variables and methods so only code within the same class can access them.

Q: What does the private keyword do?
A: It marks instance variables or methods as accessible only from within the same class. This is encapsulation - hiding your data by marking instance variables private and forcing other code to go through setter and getter methods.

C: The DotCom class has a [name] variable (String) and [locationCells] variable (ArrayList<String>).

Q: What are the instance variables in the DotCom class?
A: A String variable called name to hold the DotCom's name (like "Pets.com") and an ArrayList<String> called locationCells to hold the cell locations (like "A3", "B5", "C2").

C: The checkUserGuess() method in DotComBust loops through all remaining DotComs and calls each DotCom's [checkYourself()] method.

Q: How does the DotComBust game check a user's guess against all DotComs?
A: The checkUserGuess() method loops through the dotComsList (an ArrayList of DotCom objects) and calls checkYourself() on each DotCom, passing the user's guess. If a DotCom returns "kill", it's removed from the list.

C: The GameHelper's placeDotCom() method returns an ArrayList<[String]> containing cell locations like ["A3", "B3", "C3"].

Q: What does the GameHelper's placeDotCom() method do?
A: It calculates a random location for a DotCom on the 7x7 grid, making sure it doesn't overlap with existing DotComs. It returns an ArrayList<String> with three consecutive cell locations (either horizontal or vertical).

C: A [boolean] variable can be used as a flag to control whether a loop continues or terminates.

Q: How can you use a boolean variable to control game flow?
A: Declare a boolean like "isAlive" and set it to true. Use it in a while loop condition (while isAlive). When the game is over, set isAlive to false, which will cause the loop to terminate.

C: The dot operator ([.]) is used to invoke methods on an object or access its public instance variables.

Q: How do you call a method on an object in Java?
A: Use the dot operator. For example: myList.add("Fred") calls the add() method on the myList object. Or dotCom.checkYourself(guess) calls checkYourself() on the dotCom object.
