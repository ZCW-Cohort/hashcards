Q: What is a dictionary in Python?
A: A mapping from keys to their corresponding values.

C: In a list, the indices have to be integers; in a dictionary they can be (almost) [any type].

Q: What is a key-value pair?
A: The association of a key and a value, sometimes called an item.

C: The function [dict] creates a new dictionary with no items.

Q: What do squiggly-brackets {} represent?
A: An empty dictionary.

C: To add items to a dictionary, you can use [square brackets].

Q: Is the order of items in a dictionary predictable?
A: No, the order of items in a dictionary is unpredictable.

C: The [len] function works on dictionaries; it returns the number of key-value pairs.

Q: What does the in operator do on dictionaries?
A: It tells you whether something appears as a key in the dictionary.

C: To see whether something appears as a value in a dictionary, you can use the method [values], which returns a collection of values, and then use the in operator.

Q: What data structure do Python dictionaries use?
A: A hashtable.

C: The in operator takes about the [same] amount of time no matter how many items are in the dictionary.

Q: What is a histogram?
A: A statistical term for a collection of counters (or frequencies).

C: Dictionaries have a method called [get] that takes a key and a default value.

Q: What does the get method return if the key appears in the dictionary?
A: The corresponding value; otherwise it returns the default value.

C: If you use a dictionary in a for statement, it traverses the [keys] of the dictionary.

Q: How do you traverse the keys of a dictionary in sorted order?
A: Use the built-in function sorted.

Q: What is a lookup?
A: A dictionary operation that takes a key and finds the corresponding value.

Q: What is a reverse lookup?
A: A dictionary operation that takes a value and finds one or more keys that map to it.

C: The [raise] statement causes an exception.

Q: What is LookupError?
A: A built-in exception used to indicate that a lookup operation failed.

C: A reverse lookup is much [slower] than a forward lookup.

Q: Can lists appear as values in a dictionary?
A: Yes.

Q: Can lists be used as keys in a dictionary?
A: No, lists cannot be keys because they are not hashable.

C: A [singleton] is a list (or other sequence) with a single element.

Q: What is a hash?
A: A function that takes a value (of any kind) and returns an integer.

C: Dictionaries use integers called [hash values] to store and look up key-value pairs.

Q: Why do dictionary keys have to be hashable?
A: Because if the keys are mutable, modifying a key would cause it to hash to a different location, breaking the dictionary.

C: Keys have to be [hashable], and why mutable types like lists aren't.

Q: Can dictionaries be used as keys in other dictionaries?
A: No, because dictionaries are mutable and therefore not hashable.

C: Since dictionaries are mutable, they can't be used as keys, but they [can] be used as values.

Q: What is a memo?
A: A computed value stored to avoid unnecessary future computation.

C: A [call graph] shows a set of function frames, with lines connecting each frame to the frames of the functions it calls.

Q: What is a global variable?
A: A variable defined outside a function that can be accessed from any function.

C: Variables in [__main__] are sometimes called global because they can be accessed from any function.

Q: What are flags?
A: Boolean variables that indicate whether a condition is true.

C: To reassign a global variable inside a function you have to [declare] the global variable before you use it.

Q: What does the global statement do?
A: It tells the interpreter that when you reference a variable name in the function, you mean the global variable, not a local one.

C: If a global variable refers to a mutable value, you can modify the value [without declaring] the variable.

Q: What happens if you try to reassign a global variable inside a function without declaring it global?
A: Python creates a new local variable with that name instead of modifying the global variable.

Q: What is a sanity check?
A: Code that checks for errors automatically by detecting results that are "insane" (for example, checking that an average is not greater than the largest element).

C: A [consistency check] compares the results of two different computations to see if they are consistent.

Q: What does the pprint module provide?
A: A pprint function that displays built-in types in a more human-readable format.

Q: What is mapping?
A: A relationship in which each element of one set corresponds to an element of another set.

Q: What is a dictionary?
A: A mapping from keys to their corresponding values.

Q: What is a key-value pair?
A: The representation of the mapping from a key to a value.

Q: What is an item in a dictionary?
A: Another name for a key-value pair.

Q: What is a key?
A: An object that appears in a dictionary as the first part of a key-value pair.

Q: What is a value in a dictionary?
A: An object that appears in a dictionary as the second part of a key-value pair.

Q: What is an implementation?
A: A way of performing a computation.

Q: What is a hashtable?
A: The algorithm used to implement Python dictionaries.

Q: What is a hash function?
A: A function used by a hashtable to compute the location for a key.

Q: What is hashable?
A: A type that has a hash function. Immutable types like integers, floats and strings are hashable; mutable types like lists and dictionaries are not.

Q: What is a lookup?
A: A dictionary operation that takes a key and finds the corresponding value.

Q: What is a reverse lookup?
A: A dictionary operation that takes a value and finds one or more keys that map to it.

Q: What is a raise statement?
A: A statement that (deliberately) raises an exception.

Q: What is a singleton?
A: A list (or other sequence) with a single element.

Q: What is a call graph?
A: A diagram that shows every frame created during the execution of a program, with an arrow from each caller to each callee.

Q: What is a memo?
A: A computed value stored to avoid unnecessary future computation.

Q: What is a global variable?
A: A variable defined outside a function. Global variables can be accessed from any function.

Q: What is a global statement?
A: A statement that declares a variable name global.

Q: What is a flag?
A: A boolean variable used to indicate whether a condition is true.

Q: What is a declaration?
A: A statement like global that tells the interpreter something about a variable.
