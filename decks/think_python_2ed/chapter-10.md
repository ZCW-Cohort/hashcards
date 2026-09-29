Q: What is a list in Python?
A: A sequence of values, where the values can be any type.

Q: What are the values in a list called?
A: Elements or sometimes items.

C: The simplest way to create a new list is to enclose the elements in [square brackets].

C: A list within another list is [nested].

C: A list that contains no elements is called an [empty list].

Q: How do you create an empty list?
A: With empty brackets: []

Q: Are lists mutable or immutable?
A: Mutable.

C: Unlike strings, [lists] are mutable.

Q: What happens if you try to read or write an element that does not exist?
A: You get an IndexError.

Q: How do negative indices work with lists?
A: They count backward from the end of the list.

Q: Does the 'in' operator work on lists?
A: Yes.

Q: What is the most common way to traverse the elements of a list?
A: With a for loop.

C: To traverse a list and update elements, you need the [indices].

Q: What does the + operator do with lists?
A: Concatenates lists.

Q: What does the * operator do with lists?
A: Repeats a list a given number of times.

Q: Does the slice operator work on lists?
A: Yes.

C: If you omit the first index in a slice, the slice starts at the [beginning].

C: If you omit the second index in a slice, the slice goes to the [end].

Q: What does t[:] create?
A: A copy of the whole list.

C: A slice operator on the [left side] of an assignment can update multiple elements.

Q: What does the append method do?
A: Adds a new element to the end of a list.

Q: What does the extend method do?
A: Takes a list as an argument and appends all of the elements.

Q: What does the sort method do?
A: Arranges the elements of the list from low to high.

Q: What do most list methods return?
A: None (they are void methods that modify the list).

C: An operation that combines a sequence of elements into a single value is called [reduce].

Q: What is an accumulator?
A: A variable used in a loop to add up or accumulate a result.

Q: What built-in function adds up all elements of a list?
A: sum

C: An operation that "maps" a function onto each element in a sequence is called a [map].

C: An operation that selects some elements and filters out others is called a [filter].

Q: What does the pop method do?
A: Modifies the list and returns the element that was removed.

Q: What does pop() without an index do?
A: Deletes and returns the last element.

Q: What does the del operator do with lists?
A: Deletes an element (but doesn't return it).

Q: What does the remove method do?
A: Removes an element by value (not index).

Q: What does the remove method return?
A: None.

C: To convert from a string to a list of characters, you can use [list].

Q: What does the split method do?
A: Breaks a string into words (or parts based on a delimiter).

Q: What is a delimiter in the context of split?
A: An optional argument that specifies which characters to use as word boundaries.

Q: What does the join method do?
A: Takes a list of strings and concatenates the elements.

C: [join] is the inverse of split.

Q: How do you call the join method?
A: Invoke it on the delimiter and pass the list as a parameter.

Q: What operator checks whether two variables refer to the same object?
A: The is operator.

C: If two objects are [equivalent], they have the same elements, but if they are [identical], they are the same object.

Q: What is a reference?
A: The association of a variable with an object.

Q: What is aliasing?
A: When an object has more than one reference (more than one name).

C: If the aliased object is [mutable], changes made with one alias affect the other.

Q: When you pass a list to a function, what does the function get?
A: A reference to the list.

Q: If a function modifies a list parameter, does the caller see the change?
A: Yes.

C: The [append] method modifies a list, but the [+] operator creates a new list.

Q: Why doesn't t = t.sort() work as expected?
A: Because sort returns None, so t becomes None.

Q: How can you make a copy of a list to avoid aliasing?
A: Use a slice with no indices: t2 = t[:]

Q: What built-in function returns a new sorted list without modifying the original?
A: sorted

C: A [list] is a sequence of values.

C: [element]: One of the values in a list (or other sequence), also called items.

C: [nested list]: A list that is an element of another list.

C: [accumulator]: A variable used in a loop to add up or accumulate a result.

C: [augmented assignment]: A statement that updates the value of a variable using an operator like +=.

C: [reduce]: A processing pattern that traverses a sequence and accumulates the elements into a single result.

C: [map]: A processing pattern that traverses a sequence and performs an operation on each element.

C: [filter]: A processing pattern that traverses a list and selects the elements that satisfy some criterion.

C: [object]: Something a variable can refer to. An object has a type and a value.

C: [equivalent]: Having the same value.

C: [identical]: Being the same object (which implies equivalence).

C: [reference]: The association between a variable and its value.

C: [aliasing]: A circumstance where two or more variables refer to the same object.

C: [delimiter]: A character or string used to indicate where a string should be split.
