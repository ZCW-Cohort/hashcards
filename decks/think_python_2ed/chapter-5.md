C: The [floor division] operator, //, divides two numbers and rounds down to an integer.

C: The [modulus operator], %, divides two numbers and returns the [remainder].

Q: How can you check if one number is divisible by another using the modulus operator?
A: If x % y is zero, then x is divisible by y.

C: x % 10 yields the [right-most digit] of x (in base 10).

C: A [boolean expression] is an expression that is either true or false.

C: The == operator compares two operands and produces [True] if they are equal and [False] otherwise.

Q: What type do True and False belong to?
A: bool

C: The [relational operators] are: ==, !=, >, <, >=, and <=.

Q: What is a common error when using relational operators?
A: Using a single equal sign (=) instead of a double equal sign (==). Remember that = is an assignment operator and == is a relational operator.

C: The three [logical operators] are: and, or, and not.

C: x > 0 and x < 10 is true only if x is greater than [0] and less than [10].

C: n%2 == 0 or n%3 == 0 is true if [either or both] of the conditions is true.

C: The [not] operator negates a boolean expression.

Q: How does Python interpret nonzero numbers in logical operations?
A: Any nonzero number is interpreted as True.

C: The boolean expression after if is called the [condition].

C: if statements have the same structure as function definitions: a [header] followed by an [indented body].

C: Statements like if that have a header and body are called [compound statements].

Q: What statement can you use to create a body with no statements as a placeholder?
A: The pass statement, which does nothing.

C: In [alternative execution], there are two possibilities and the condition determines which one runs.

C: In alternative execution, the alternatives are called [branches], because they are branches in the flow of execution.

C: A [chained conditional] is used when there are more than two possibilities and we need more than two branches.

C: [elif] is an abbreviation of "else if".

Q: In a chained conditional, if more than one condition is true, which branch runs?
A: Only the first true branch runs.

C: A [nested conditional] is one conditional within another.

Q: Why should nested conditionals be avoided when possible?
A: They become difficult to read very quickly.

C: A function that calls itself is [recursive]; the process of executing it is called [recursion].

Q: What happens when a return statement is executed?
A: The flow of execution immediately returns to the caller, and the remaining lines of the function don't run.

C: For a recursive function, there might be more than one [frame] on the stack at the same time.

C: The bottom of the stack in a recursive function, where the recursion stops, is called the [base case].

Q: What is the base case in recursion?
A: A conditional branch in a recursive function that does not make a recursive call.

C: If a recursion never reaches a base case, it is known as [infinite recursion].

Q: What error does Python report when maximum recursion depth is reached?
A: RuntimeError: Maximum recursion depth exceeded

Q: How many frames are on the stack when Python reports maximum recursion depth exceeded?
A: 1000 recurse frames

C: Python provides a built-in function called [input] that stops the program and waits for the user to type something.

Q: What does the input function return?
A: What the user typed as a string.

C: The sequence [\n] represents a [newline], which is a special character that causes a line break.

Q: What should you do if you expect the user to type an integer with input?
A: Convert the return value to int using int().

Q: What are the most useful parts of an error message?
A:
- What kind of error it was
- Where it occurred

Q: Why can whitespace errors be tricky?
A: Because spaces and tabs are invisible and we are used to ignoring them.

Q: Where might the actual error be in relation to where the error message points?
A: The actual error might be earlier in the code, sometimes on a previous line.

C: [floor division]: An operator, denoted //, that divides two numbers and rounds down (toward negative infinity) to an integer.

C: [modulus operator]: An operator, denoted with a percent sign (%), that works on integers and returns the remainder when one number is divided by another.

C: [boolean expression]: An expression whose value is either True or False.

C: [relational operator]: One of the operators that compares its operands: ==, !=, >, <, >=, and <=.

C: [logical operator]: One of the operators that combines boolean expressions: and, or, and not.

C: [conditional statement]: A statement that controls the flow of execution depending on some condition.

C: [condition]: The boolean expression in a conditional statement that determines which branch runs.

C: [compound statement]: A statement that consists of a header and a body. The header ends with a colon (:). The body is indented relative to the header.

C: [branch]: One of the alternative sequences of statements in a conditional statement.

C: [chained conditional]: A conditional statement with a series of alternative branches.

C: [nested conditional]: A conditional statement that appears in one of the branches of another conditional statement.

C: [return statement]: A statement that causes a function to end immediately and return to the caller.

C: [recursion]: The process of calling the function that is currently executing.

C: [base case]: A conditional branch in a recursive function that does not make a recursive call.

C: [infinite recursion]: A recursion that doesn't have a base case, or never reaches it. Eventually, an infinite recursion causes a runtime error.
