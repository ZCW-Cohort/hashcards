C: This chapter focuses on building a [Battleship-style game] called ["Sink a Dot Com"], where you write [prepcode], [test code], and [real code].

Q: What are the three main things you write when creating a new class?
A: Prepcode, test code, and real (Java) code. Prepcode describes what to do (not how), test code validates the implementation, and real code is the actual Java implementation.

C: Prepcode should describe [what to do], not [how to do it]. Implementation comes later.

Q: Why should you write test code before implementing the methods?
A: Writing test code first helps clarify your thoughts about what the method needs to do. As soon as your implementation is done, you already have test code waiting to validate it. If you don't do it now, you'll never do it.

C: The enhanced for loop (also called ["for each"] or ["for in"]) makes it easier to iterate over all elements in an [array] or other [collection].

Q: What is the syntax of an enhanced for loop?
A: for (Type element : collection) { }. For example: for (String name : nameArray) { }. It reads as "for each element in the collection, assign the element to the variable and run the loop body."

C: The regular for loop has three parts: [initialization], [boolean test], and [iteration expression].

Q: What are the three parts of a regular for loop and what do they do?
A: Initialization (declare and initialize a variable), boolean test (the conditional that must resolve to true or false), and iteration expression (what happens at the end of each loop). Example: for (int i = 0; i < 100; i++)

C: Use [for] loops over [while] loops when you know how many times you want to repeat the loop code.

Q: What is the difference between for and while loops?
A: A while loop has only the boolean test and is good when you don't know how many times to loop. A for loop has built-in initialization and iteration expression, making it cleaner when you know exactly how many times to loop.

C: The post-increment operator [++] adds 1 to a variable. The pre-increment [++x] increments first, then uses the value. The post-increment [x++] uses the value, then increments.

Q: What does x++ do and how is it different from ++x?
A: Both add 1 to x. But ++x increments first then uses the new value, while x++ uses the current value then increments. This matters when the increment is part of a larger expression. For example: int x = 0; int z = ++x gives z = 1, but int z = x++ gives z = 0.

C: The [break] statement gets you out of a loop immediately, even if the boolean test condition is still [true].

Q: What does the break statement do in a loop?
A: It exits the loop immediately. No iteration, no boolean test, just get out now. It's useful when you've found what you're looking for and don't need to continue looping.

C: Integer.parseInt() converts a [String] to an [int]. It works only on Strings that represent [digits] (0-9).

Q: How do you convert a String to an int in Java?
A: Use Integer.parseInt(). For example: int guess = Integer.parseInt("3"). The Integer class ships with Java and the parseInt method knows how to parse a String into the int it represents.

Q: What happens if you try to parse a non-numeric String?
A: The code will blow up at runtime (throw an exception). Integer.parseInt() works only on Strings that represent ASCII values for digits (0,1,2,3,4,5,6,7,8,9). Trying to parse "two" or "blurp" will cause an error.

C: Math.random() returns a [double] from zero to just less than [one]. You often need to [cast] it to an int.

Q: How do you generate a random number in Java?
A: Use Math.random(), which returns a double from 0 to just less than 1. To get a random int in a range, use a formula like: int randomNum = (int) (Math.random() * 5) to get 0-4.

C: [Casting] forces a value to become a different type. A [long] can be cast to an [int], but you might lose data.

Q: What is casting and how do you cast primitives?
A: Casting forces a bigger primitive into a smaller one. Use parentheses with the type: int x = (int) y. The cast chops the value down to the smaller size. If the original value was too big, what's left will be a weird (but calculable) number.

C: You [cannot] cast anything to a [boolean] or vice versa.

Q: Can you cast a boolean to another type?
A: No. Don't even think about casting anything to a boolean or vice versa. Just walk away.

C: In Extreme Programming (XP), you write the [test code first], make [small but frequent releases], and [don't release] anything until it passes all tests.

Q: What are some key practices of Extreme Programming?
A: Write test code first, make small frequent releases, develop in iteration cycles, don't add functionality not in the spec, no killer schedules (work regular hours), refactor whenever you notice the opportunity, don't release until it passes all tests, keep it simple, and program in pairs.

C: The enhanced for loop declares an [iteration variable] that holds one element from the [collection] with each iteration.

Q: What must be true about the iteration variable in an enhanced for loop?
A: The type of the iteration variable must be compatible with the elements in the array. You can't declare an int iteration variable to use with a String[] array.

C: A method can declare only [one] return value, but if you want to return multiple values, the return type can be an [array].

Q: Can a method return multiple values?
A: Sort of. A method can declare only one return value, but if you want to return multiple values, the declared return type can be an array. You can stuff values into the array and pass it back.

C: Java is [pass-by-value], which means [pass-by-copy]. The method gets a [copy] of the value, not the [original variable].

Q: What does pass-by-value mean in Java?
A: When you pass a variable to a method, Java makes a copy of the bits in the variable and passes that copy. The method cannot change the bits that were in the calling variable. The original variable doesn't change.

C: When developing a program, start with a [high-level design] and create a [flowchart] showing the program flow.

Q: What should you do first when building a program?
A: Start with a high-level design. Figure out the general flow of the program using a flowchart. Identify what the program needs to do, then figure out what kind of objects you'll need to do the work. Think about the things in the program rather than the procedures.

C: A [SimpleDotCom] game uses a single row of [seven] cells and [one] DotCom, instead of the full 2-D grid with three DotComs.

Q: What is the simplified version of the Sink a Dot Com game?
A: The Simple Dot Com Game hides the DotCom in a single row (not a 2-D grid) and uses one DotCom (not three). The DotCom occupies three consecutive cells out of seven possible cells. Locations are simple integers (0-6) instead of "A2", "C4", etc.

C: The virtual row in the Simple Dot Com game is [virtual] - it doesn't exist anywhere in the [program]. You only need an array that holds the [three cells] the DotCom occupies.

Q: Do you need to create an array representing the entire game grid?
A: No. As long as both the game and user know the DotCom is hidden in three consecutive cells out of seven possible cells, the row itself doesn't have to be represented in code. You only need an array that holds just the three cells the DotCom occupies.

C: The [GameHelper] class provides the getUserInput() method that gets [command-line input] from the user and returns it as a [String].

Q: How does the game get user input?
A: Using the GameHelper class, which has a getUserInput() method. This method takes a String argument to prompt the user, displays it at the command-line, reads the user's input after they hit RETURN, and returns the result as a String.

C: The [++] operator can be used as [pre-increment] or [post-increment]. The [--] operator can be used as [pre-decrement] or [post-decrement].

Q: What's the difference between x++ and x--?
A: x++ adds 1 to x (increment), while x-- subtracts 1 from x (decrement). Both are shorthand: x++ is the same as x = x + 1, and x-- is the same as x = x - 1.

C: When converting a String to an int, the Integer class has a method called [parseInt()] that knows how to parse a String into the [int it represents].

Q: Why do you need to convert a String to an int in the game?
A: The user types their guess as a String (like "2" or "5"), but the cell locations are ints in an array. You can't compare an int to a String. So you use Integer.parseInt() to convert the String "2" into the int 2.

C: In a for loop, the iteration expression runs at the [end] of each loop iteration.

Q: When does the iteration expression in a for loop execute?
A: At the end of each loop iteration. This is important to remember - it happens after the loop body executes, before the boolean test is checked again for the next iteration.