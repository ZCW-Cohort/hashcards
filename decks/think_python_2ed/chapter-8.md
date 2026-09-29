C: A [string] is a [sequence], which means it is an ordered collection of other values.

Q: How do you access individual characters in a string?
A: Using the bracket operator with an index, like fruit[1]

C: The expression in brackets is called an [index], which indicates which character in the sequence you want.

Q: What is the index of the first character in a string?
A: 0 (zero)

C: In Python, the index is an [offset] from the beginning of the string, and the offset of the first letter is [zero].

Q: What happens if you try to use a float as a string index?
A: You get a TypeError: string indices must be integers

Q: What does the len() function return for a string?
A: The number of characters in the string

C: The built-in function [len] returns the number of characters in a string.

Q: Why does fruit[length] cause an IndexError when length = len(fruit)?
A: Because indices start at 0, so the last character is at index length-1, not length

Q: How do negative indices work in Python strings?
A: They count backward from the end of the string (e.g., fruit[-1] is the last letter)

C: The expression fruit[-1] yields the [last letter], fruit[-2] yields the [second to last], and so on.

Q: What is traversal in the context of strings?
A: A pattern of processing that involves processing a string one character at a time, from beginning to end

C: A [traversal] is a pattern of processing where you start at the beginning, select each character in turn, do something to it, and continue until the end.

Q: What are two ways to write a traversal of a string?
A:
- Using a while loop with an index
- Using a for loop to iterate over characters

Q: In the ducklings example, what output does the loop produce for 'JKLMNOPQ' + 'ack'?
A: Jack, Kack, Lack, Mack, Nack, Oack, Pack, Qack

C: A [slice] is a segment of a string.

Q: What does the operator [n:m] return?
A: The part of the string from the n-eth character to the m-eth character, including the first but excluding the last

C: If you omit the first index (before the colon), the slice starts at the [beginning of the string]. If you omit the second index, the slice goes to the [end of the string].

Q: What is the result when the first index is greater than or equal to the second in a slice?
A: An empty string, represented by two quotation marks ''

C: An [empty string] contains no characters and has length 0, but other than that, it is the same as any other string.

Q: Can you change a character in a string using the bracket operator on the left side of an assignment?
A: No, you get a TypeError because strings are immutable

C: Strings are [immutable], which means you can't change an existing string.

Q: How do you create a variation of an existing string?
A: Create a new string using concatenation and slicing, like 'J' + greeting[1:]

Q: What does the find function return if the character is not found in the word?
A: -1

C: The pattern of computation where you traverse a sequence and return when you find what you're looking for is called a [search].

Q: What pattern of computation is demonstrated by counting letters in a string?
A: A counter pattern

C: A [counter] is a variable initialized to 0 and then incremented each time something is found.

Q: What is a method?
A: Similar to a function—it takes arguments and returns a value—but the syntax is different (uses dot notation)

C: A method call is called an [invocation].

Q: How does the method syntax differ from function syntax?
A: Instead of function syntax like upper(word), it uses method syntax like word.upper()

Q: What does the string method upper() do?
A: Takes a string and returns a new string with all uppercase letters

Q: What can the find method find that the function version cannot?
A: Substrings, not just individual characters

C: The find method can take a second argument for the index where it should [start], and a third argument for the index where it should [stop].

Q: What is an optional argument?
A: A function or method argument that is not required

Q: What does the 'in' operator do with strings?
A: Returns True if the first string appears as a substring in the second

C: The word [in] is a boolean operator that takes two strings and returns True if the first appears as a substring in the second.

Q: Do relational operators work on strings?
A: Yes, they can be used for equality testing and alphabetical ordering

Q: How does Python handle uppercase and lowercase letters in string comparison?
A: All uppercase letters come before all lowercase letters

Q: What is a common way to address case sensitivity in string comparison?
A: Convert strings to a standard format, such as all lowercase, before performing the comparison

C: The [guardian pattern] is when you check a condition early and return immediately if it's not met.

Q: What is the guardian pattern in the is_reverse function?
A: Checking if the words are the same length first, and returning False immediately if not

Q: What debugging technique is suggested for IndexError with indices?
A: Print the values of the indices immediately before the line where the error appears

Q: What is a state diagram useful for?
A: Getting a better idea of what is happening during execution, especially with loops and indices

Q: What is an object?
A: Something a variable can refer to. For now, you can use "object" and "value" interchangeably.

Q: What is a sequence?
A: An ordered collection of values where each value is identified by an integer index.

Q: What is an item?
A: One of the values in a sequence.

Q: What is an index?
A: An integer value used to select an item in a sequence, such as a character in a string. In Python indices start from 0.

Q: What is a slice?
A: A part of a string specified by a range of indices.

Q: What is an empty string?
A: A string with no characters and length 0, represented by two quotation marks.

Q: What does immutable mean?
A: The property of a sequence whose items cannot be changed.

Q: What does traverse mean?
A: To iterate through the items in a sequence, performing a similar operation on each.

Q: What is a search pattern?
A: A pattern of traversal that stops when it finds what it is looking for.

Q: What is a counter?
A: A variable used to count something, usually initialized to zero and then incremented.

Q: What is an invocation?
A: A statement that calls a method.

Q: What is an optional argument?
A: A function or method argument that is not required.
