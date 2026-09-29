Q: What are the three main types of errors in debugging?
A: Syntax errors, runtime errors, and semantic errors

C: [Syntax errors] are discovered by the interpreter when translating source code into byte code and indicate something wrong with the structure of the program.

C: [Runtime errors] are produced by the interpreter if something goes wrong while the program is running.

C: [Semantic errors] are problems with a program that runs without producing error messages but doesn't do the right thing.

Q: Why are syntax error messages often not helpful?
A: The most common messages like "SyntaxError: invalid syntax" and "SyntaxError: invalid token" are not very informative, and the error location shown is where Python noticed the problem, not necessarily where the actual error is.

C: The syntax error is often [prior to the location] of the error message, often on the [preceding line].

Q: What are 8 ways to avoid common syntax errors?
A:
- Don't use Python keywords for variable names
- Include colons at the end of compound statement headers (for, while, if, def)
- Ensure strings have matching quotation marks (straight quotes, not curly)
- Terminate multiline strings with triple quotes properly
- Close all opening operators (, {, [
- Use == instead of = in conditionals
- Check indentation alignment
- Be careful with non-ASCII characters

C: An [unclosed opening operator] makes Python continue with the next line as part of the current statement.

Q: What should you do if you keep making changes but they make no difference?
A: Check that you're editing and running the same file, save your changes, verify the filename hasn't changed, check your development environment configuration, avoid naming conflicts with standard Python modules, and restart the interpreter if using import.

C: If you're not sure you're running the new code, put an [obvious and deliberate syntax error] at the beginning and run it again.

Q: What does it mean when a program "hangs"?
A: It means the program stops and seems to be doing nothing, often caught in an infinite loop or infinite recursion.

C: To debug an infinite loop, add a [print statement] immediately before the loop saying "entering the loop" and another after saying "exiting the loop".

Q: How do you debug an infinite loop?
A: Add print statements at the end of the loop that print the values of variables in the condition and the value of the condition itself to see why they're not being updated correctly.

C: Most infinite recursions cause a [Maximum recursion depth exceeded] error.

Q: How do you debug infinite recursion?
A: Make sure there is a base case that causes the function to return without a recursive invocation, and add print statements at the beginning of the function to print parameters and verify they're moving toward the base case.

Q: What is a traceback?
A: It identifies the function currently running, then the function that called it, and so on, tracing the sequence of function calls including line numbers where each call occurred.

C: A [NameError] means you're trying to use a variable that doesn't exist in the current environment.

Q: What are the possible causes of a TypeError?
A:
- Using a value improperly (e.g., indexing with a non-integer)
- Mismatch in format string items
- Passing wrong number of arguments to a function

C: A [KeyError] means you're trying to access a dictionary element using a key that doesn't exist.

Q: What does it mean if an AttributeError indicates an object has NoneType?
A: The object is None, often because you forgot to return a value from a function or used the result from a list method like sort that returns None.

C: An [IndexError] means the index you're using is greater than the length minus one.

Q: What are two ways to proceed when you get inundated with print statement output?
A: Simplify the output (remove/comment out unhelpful print statements) or simplify the program (scale down the problem, clean up dead code, reorganize).

C: The process of finding the [minimal test case] often leads you to the bug.

Q: Why are semantic errors the hardest to debug?
A: The interpreter provides no information about what is wrong; only you know what the program is supposed to do.

Q: What three questions should you ask when your program doesn't work?
A:
- Is there something the program was supposed to do but doesn't seem to be happening?
- Is something happening that shouldn't?
- Is a section of code producing an effect that is not what you expected?

C: If you write a program that doesn't do what you expect, often the problem is not in the program; it's in your [mental model].

Q: How do you correct your mental model of how a program works?
A: Break the program into its components (functions and methods) and test each component independently to find the discrepancy between your model and reality.

Q: Why should you break complex expressions into assignments to temporary variables?
A: They provide additional documentation through variable names, make code easier to read, and allow you to check types and display values of intermediate variables for debugging.

C: Multiplication and division have the [same precedence] and are evaluated from [left to right].

Q: How can you make the order of evaluation explicit in expressions?
A: Add parentheses to make the order clear, which makes the program correct and more readable.

Q: What should you do with a return statement that has a complex expression?
A: Use a temporary variable to store the result so you can display its value before returning.

Q: What are three symptoms of spending too much time at the computer debugging?
A:
- Frustration and rage
- Superstitious beliefs and magical thinking
- Random walk programming

C: Some of the best places to find bugs are [trains], [showers], and [in bed], just before you fall asleep.

Q: What should you prepare before bringing someone in to help debug?
A: Make the program as simple as possible, work on the smallest input that causes the error, have print statements in appropriate places with comprehensible output, and understand the problem well enough to describe it concisely.

Q: What information should you give someone helping you debug?
A:
- The error message and what part of the program it indicates
- The last thing you did before the error occurred
- What you've tried so far and what you've learned

Q: What should you do after finding a bug?
A: Think about what you could have done to find it faster so you can find similar bugs more quickly in the future.

C: The goal of debugging is not just to make the program work, but to [learn how to make the program work].

Q: What is a syntax error?
A: An error discovered by the interpreter when translating source code into byte code, indicating something is wrong with the structure of the program.

Q: What is a runtime error?
A: An error produced by the interpreter when something goes wrong while the program is running, usually including information about where the error occurred and what functions were executing.

Q: What is a semantic error?
A: A problem with a program that runs without producing error messages but doesn't do the right thing.

Q: What is the Python debugger?
A: pdb is useful for tracking down exceptions because it allows you to examine the state of the program immediately before the error.
