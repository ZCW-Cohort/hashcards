C: The language feature most often associated with [object-oriented programming] is inheritance.

Q: What is inheritance?
A: The ability to define a new class that is a modified version of an existing class.

C: In a playing card deck, there are [fifty-two] cards, each belonging to one of [four] suits and one of [thirteen] ranks.

C: The suits in descending order in bridge are [Spades], [Hearts], [Diamonds], and [Clubs].

C: The ranks in a deck are [Ace], [2], [3], [4], [5], [6], [7], [8], [9], [10], [Jack], [Queen], and [King].

Q: What does "encode" mean in the context of programming?
A: To define a mapping between numbers and suits, or between numbers and ranks. This kind of encoding is not meant to be a secret (that would be "encryption").

C: In the Card class integer encoding, Spades maps to [3], Hearts maps to [2], Diamonds maps to [1], and Clubs maps to [0].

C: In the Card class integer encoding, Jack maps to [11], Queen maps to [12], and King maps to [13].

C: The default card created by Card() with default parameters is the [2 of Clubs].

Q: What are class attributes?
A: Variables that are defined inside a class but outside of any method. They are associated with the class object rather than a particular instance.

Q: What are instance attributes?
A: Variables that are associated with a particular instance of a class.

C: Variables like suit_names and rank_names are [class attributes], while variables like suit and rank are [instance attributes].

Q: Why is None used as the first element of rank_names?
A: Because there is no card with rank zero. By including None as a place-keeper, we get a mapping with the nice property that the index 2 maps to the string '2', and so on.

C: The [__lt__] method stands for "less than" and is used to override the behavior of relational operators for programmer-defined types.

Q: What parameters does __lt__ take?
A: Two parameters: self and other, and returns True if self is strictly less than other.

C: In the Card class comparison implementation, [suit] is more important than rank, so all of the Spades outrank all of the Diamonds.

Q: What is an efficient way to accumulate a large string?
A: Build a list of strings and then use the string method join.

C: The list method [pop] removes the last card in the list, meaning we are dealing from the bottom of the deck.

Q: What is a veneer?
A: A method or function that uses another method without doing much work. The metaphor comes from woodworking, where a veneer is a thin layer of good quality wood glued to the surface of a cheaper piece of wood to improve the appearance.

C: The add_card method is an example of a [veneer] that expresses a list operation in terms appropriate for decks.

Q: To define a new class that inherits from an existing class, what syntax do you use?
A: Put the name of the existing class in parentheses after the new class name.

C: When a new class inherits from an existing one, the existing one is called the [parent] and the new class is called the [child].

Q: What happens when you provide an init method in a child class?
A: It overrides the init method in the parent class.

Q: What methods does Hand inherit from Deck?
A: Methods like pop_card and add_card, as well as other methods defined in Deck.

C: The move_cards method takes two arguments: a [Hand object] and the [number of cards to deal].

Q: What are advantages of inheritance?
A:
- Some programs that would be repetitive without inheritance can be written more elegantly with it
- Inheritance can facilitate code reuse, since you can customize the behavior of parent classes without having to modify them
- The inheritance structure may reflect the natural structure of the problem, making the design easier to understand

Q: What are disadvantages of inheritance?
A:
- Inheritance can make programs difficult to read
- When a method is invoked, it is sometimes not clear where to find its definition
- The relevant code may be spread across several modules
- Many things that can be done using inheritance can be done as well or better without it

C: A [class diagram] is a more abstract representation of the structure of a program that shows classes and the relationships between them, rather than individual objects.

Q: What is a HAS-A relationship?
A: A relationship where objects in one class contain references to objects in another class. For example, "a Rectangle has a Point."

Q: What is an IS-A relationship?
A: A relationship where one class inherits from another. For example, "a Hand is a kind of a Deck."

Q: What is a dependency relationship?
A: A relationship where one class might depend on another in the sense that objects in one class take objects in the second class as parameters, or use objects in the second class as part of a computation.

C: In a class diagram, an arrow with a [hollow triangle] head represents an IS-A relationship.

C: In a class diagram, a standard [arrow] head represents a HAS-A relationship.

C: In a class diagram, the [star (*)] near the arrow head is a multiplicity that indicates how many objects are referenced.

C: Dependencies in class diagrams are normally shown with a [dashed arrow], or they are sometimes omitted if there are many of them.

Q: What does MRO stand for?
A: "Method resolution order", which is the sequence of classes Python searches to "resolve" a method name.

Q: What is the Liskov substitution principle?
A: When you override a method, the interface of the new method should be the same as the old. It should take the same parameters, return the same type, and obey the same preconditions and postconditions.

Q: What is object-oriented design?
A: A development plan where we identify objects we need and define classes to represent them. In each case there is an obvious correspondence between the object and some entity in the real world (or at least a mathematical world).

Q: What is data encapsulation?
A: A development plan for discovering class interfaces by encapsulating data. Start with functions that read and write global variables, then look for associations between global variables and the functions that use them, and encapsulate related variables as attributes of an object.

Q: What are the steps for data encapsulation?
A:
1. Start by writing functions that read and write global variables (when necessary)
2. Once you get the program working, look for associations between global variables and the functions that use them
3. Encapsulate related variables as attributes of an object
4. Transform the associated functions into methods of the new class

C: Transforming a program by changing the design without changing the behavior is called [refactoring].

Q: What is encode?
A: To represent one set of values using another set of values by constructing a mapping between them.

Q: What is a class attribute?
A: An attribute associated with a class object. Class attributes are defined inside a class definition but outside any method.

Q: What is an instance attribute?
A: An attribute associated with an instance of a class.

Q: What is a veneer?
A: A method or function that provides a different interface to another function without doing much computation.

Q: What is inheritance?
A: The ability to define a new class that is a modified version of a previously defined class.

Q: What is a parent class?
A: The class from which a child class inherits.

Q: What is a child class?
A: A new class created by inheriting from an existing class; also called a "subclass".

Q: What is an IS-A relationship?
A: A relationship between a child class and its parent class.

Q: What is a HAS-A relationship?
A: A relationship between two classes where instances of one class contain references to instances of the other.

Q: What is a dependency?
A: A relationship between two classes where instances of one class use instances of the other class, but do not store them as attributes.

Q: What is a class diagram?
A: A diagram that shows the classes in a program and the relationships between them.

Q: What is multiplicity?
A: A notation in a class diagram that shows, for a HAS-A relationship, how many references there are to instances of another class.

Q: What is data encapsulation?
A: A program development plan that involves a prototype using global variables and a final version that makes the global variables into instance attributes.