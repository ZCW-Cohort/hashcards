Q: What is a tuple in Python?
A: An immutable sequence of values that can be any type and are indexed by integers.

C: A [tuple] is a comma-separated list of values.

Q: How do you create a tuple with a single element?
A: You have to include a final comma, like `t1 = 'a',`

Q: What happens if you try to modify an element of a tuple?
A: You get a TypeError because tuples are immutable and don't support item assignment.

C: The bracket operator indexes an element, and the [slice] operator selects a range of elements.

Q: How do relational operators compare tuples?
A: Python starts by comparing the first element from each sequence. If they are equal, it goes on to the next elements, and so on, until it finds elements that differ.

C: [Tuple assignment] allows you to swap the values of two variables elegantly using `a, b = b, a`.

Q: What requirement exists for the number of variables and values in tuple assignment?
A: The number of variables on the left and the number of values on the right have to be the same.

Q: What does the built-in function divmod do?
A: It takes two arguments and returns a tuple of two values: the quotient and remainder.

C: A parameter name that begins with [*] gathers arguments into a tuple.

Q: What is the complement of gather?
A: Scatter, which uses the * operator to make a sequence behave like multiple arguments.

Q: What does the built-in function zip do?
A: It takes two or more sequences and interleaves them, returning a zip object that iterates through pairs.

C: If the sequences passed to zip are not the same length, the result has the length of the [shorter] one.

Q: How can you traverse the elements of a sequence and their indices simultaneously?
A: Use the built-in function enumerate in a for loop.

Q: What does the dictionary method items return?
A: A sequence of tuples, where each tuple is a key-value pair.

C: You can use a list of tuples to initialize a new dictionary using the [dict] function.

Q: Why are tuples commonly used as keys in dictionaries?
A: Because you can't use lists as keys, and tuples are immutable.

Q: What are three cases where you might prefer tuples over lists?
A:
- In return statements, it's syntactically simpler to create a tuple
- When using a sequence as a dictionary key, you need an immutable type
- When passing a sequence as an argument to reduce unexpected behavior due to aliasing

C: Because tuples are immutable, they don't provide methods like [sort] and [reverse].

Q: What built-in functions can you use instead of sort and reverse methods for tuples?
A: sorted, which returns a new list with elements in sorted order, and reversed, which returns an iterator that traverses in reverse order.

Q: What is a shape error?
A: An error caused when a data structure has the wrong type, size, or structure.

C: [tuple]: An immutable sequence of elements.

C: [tuple assignment]: An assignment with a sequence on the right side and a tuple of variables on the left. The right side is evaluated and then its elements are assigned to the variables on the left.

C: [gather]: An operation that collects multiple arguments into a tuple.

C: [scatter]: An operation that makes a sequence behave like multiple arguments.

C: [zip object]: The result of calling a built-in function zip; an object that iterates through a sequence of tuples.

C: [iterator]: An object that can iterate through a sequence, but which does not provide list operators and methods.

C: [data structure]: A collection of related values, often organized in lists, dictionaries, tuples, etc.

C: [shape error]: An error caused because a value has the wrong shape; that is, the wrong type or size.
