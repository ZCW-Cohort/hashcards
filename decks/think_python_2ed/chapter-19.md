Q: What is a conditional expression in Python?
A: An expression that allows you to choose one of two values based on a condition, written as `value_if_true if condition else value_if_false`.

Q: How can you rewrite an if-else statement that assigns one of two values to a variable?
A: Use a conditional expression: `y = math.log(x) if x > 0 else float('nan')` instead of a multi-line if-else statement.

C: A [conditional expression] can replace a conditional statement if both branches contain simple expressions that are either returned or assigned to the same variable.

Q: What is a list comprehension?
A: An expression with a for loop in square brackets that yields a new list, such as `[s.capitalize() for s in t]`.

Q: How do you write a list comprehension that filters elements?
A: Include an if clause after the for loop: `[s for s in t if s.isupper()]`.

C: List comprehensions are concise and easy to read for simple expressions, and are usually [faster] than the equivalent for loops.

Q: What is a disadvantage of list comprehensions?
A: They are harder to debug because you can't put a print statement inside the loop.

Q: What is a generator expression?
A: An expression with a for loop in parentheses that yields a generator object, similar to list comprehensions but with parentheses instead of square brackets.

C: A generator expression does not compute the values [all at once]; it waits to be asked.

Q: How do you get the next value from a generator?
A: Use the built-in function `next(g)`, which raises `StopIteration` when the sequence is exhausted.

Q: What are generator expressions often used with?
A: Functions like sum, max, and min: `sum(x**2 for x in range(5))`.

Q: What does the `any` function do?
A: It takes a sequence of boolean values and returns True if any of the values are True.

C: Using `any` with a generator expression is efficient because it stops immediately if it finds a [True] value.

Q: What does the `all` function do?
A: It returns True if every element of the sequence is True.

Q: What is a set in Python?
A: A built-in type that behaves like a collection of dictionary keys with no values, where adding elements is fast and checking membership is fast.

Q: How do you perform set subtraction in Python?
A: Use the `difference` method or the `-` operator: `set(d1) - set(d2)`.

C: The `<=` operator checks whether one set is a [subset] of another, including the possibility that they are equal.

Q: What is a Counter?
A: A type from the collections module that is like a set, except if an element appears more than once, the Counter keeps track of how many times it appears.

Q: How do you initialize a Counter?
A: Import it from collections and initialize with a string, list, or anything that supports iteration: `Counter('parrot')`.

C: Unlike dictionaries, Counters don't raise an exception if you access an element that doesn't appear. Instead, they return [0].

Q: What does the `most_common` method of a Counter do?
A: It returns a list of value-frequency pairs, sorted from most common to least.

Q: What is a defaultdict?
A: A dictionary-like object from the collections module that can generate a new value on the fly if you access a key that doesn't exist.

Q: How do you create a defaultdict?
A: Provide a factory function when creating it: `d = defaultdict(list)`, where the function is used to create new values.

C: When creating a defaultdict, the argument is [list] (a class object), not list() (a new list instance).

Q: What is a factory function?
A: A function used to create objects, usually passed as a parameter.

Q: What is a named tuple?
A: A quick way to define simple classes that are basically collections of related values, created using `namedtuple` from the collections module.

Q: How do you create a named tuple class?
A: `Point = namedtuple('Point', ['x', 'y'])`, where the first argument is the class name and the second is a list of attribute names.

C: Named tuples automatically provide methods like [__init__] and [__str__] so you don't have to write them.

Q: How can you access elements of a named tuple?
A: By name (`p.x, p.y`) or by treating it as a regular tuple (`p[0], p[1]`).

Q: What is a drawback of named tuples?
A: Simple classes don't always stay simple, and you might decide later that you want to add methods to a named tuple.

Q: How do you gather keyword arguments in a function?
A: Use the `**` operator: `def printall(*args, **kwargs)`.

C: The keyword gathering parameter can be named anything, but [kwargs] is a common choice.

Q: What does gathering keyword arguments produce?
A: A dictionary that maps from keywords to values.

Q: How do you use the scatter operator with a dictionary to call a function?
A: Use `**` before the dictionary: `Point(**d)` where d is a dict with the appropriate keys.

Q: What happens if you pass a dictionary to a function without the scatter operator?
A: The function treats the dictionary as a single positional argument.

C: [Conditional expression] - An expression that has one of two values, depending on a condition.

C: [List comprehension] - An expression with a for loop in square brackets that yields a new list.

C: [Generator expression] - An expression with a for loop in parentheses that yields a generator object.

C: [Multiset] - A mathematical entity that represents a mapping between the elements of a set and the number of times they appear.

C: [Factory] - A function, usually passed as a parameter, used to create objects.
