Q: What is iteration?
A: The ability to run a block of statements repeatedly.

C: A new assignment makes an existing variable refer to a [new] value and stop referring to the [old] value.

Q: Why is the equal sign (=) in Python not a mathematical proposition of equality?
A:
- Equality is symmetric (if a=7 then 7=a), but assignment is not (a=7 is legal but 7=a is not)
- In mathematics, equality is permanent, but in Python, variables can be reassigned to different values

C: [Reassigning] variables is often useful, but you should use it with caution. If the values of variables change frequently, it can make the code difficult to read and debug.

Q: What is an update in Python?
A: A kind of reassignment where the new value of the variable depends on the old value.

C: Before you can update a variable, you have to [initialize] it, usually with a simple assignment.

Q: What is the term for updating a variable by adding 1?
A: Increment.

Q: What is the term for updating a variable by subtracting 1?
A: Decrement.

C: In a computer program, repetition is also called [iteration].

Q: What are the three steps in the flow of execution for a while statement?
A:
1. Determine whether the condition is true or false
2. If false, exit the while statement and continue execution at the next statement
3. If the condition is true, run the body and then go back to step 1

C: This type of flow is called a [loop] because the third step loops back around to the top.

Q: What is an infinite loop?
A: A loop that will repeat forever because the loop condition never becomes false.

C: The body of the loop should change the value of one or more variables so that the condition becomes [false] eventually and the loop [terminates].

Q: What is the Collatz conjecture related to?
A: Whether a specific sequence (where n is divided by 2 if even, or replaced with n*3+1 if odd) terminates for all positive values of n. No one has been able to prove or disprove it.

C: The [break] statement is used to jump out of a loop.

Q: What is a common pattern for while loops using break?
A: Using while True with a break statement inside the loop body, which allows checking the condition anywhere in the loop and expressing the stop condition affirmatively.

C: Newton's method computes square roots by starting with an estimate x and computing a better estimate with the formula y = [(x + a/x) / 2].

Q: Why is it dangerous to test float equality?
A: Floating-point values are only approximately right: most rational numbers (like 1/3) and irrational numbers (like √2) can't be represented exactly with a float.

C: Rather than checking whether x and y are exactly equal, it is safer to use the built-in function [abs] to compute the absolute value of the difference between them.

Q: What is an algorithm?
A: A mechanical process for solving a category of problems.

Q: What is one characteristic of algorithms?
A: They do not require any intelligence to carry out. They are mechanical processes where each step follows from the last according to a simple set of rules.

Q: What is "debugging by bisection"?
A: A debugging technique where you look at the middle of the program for an intermediate value you can check, which halves the number of lines to search with each check.

C: If the mid-point check is incorrect, there must be a problem in the [first] half of the program. If it is correct, the problem is in the [second] half.

Q: What is reassignment?
A: Assigning a new value to a variable that already exists.

Q: What is update?
A: An assignment where the new value of the variable depends on the old.

Q: What is initialization?
A: An assignment that gives an initial value to a variable that will be updated.

Q: What is increment?
A: An update that increases the value of a variable (often by one).

Q: What is decrement?
A: An update that decreases the value of a variable.

Q: What is iteration?
A: Repeated execution of a set of statements using either a recursive function call or a loop.

Q: What is an infinite loop?
A: A loop in which the terminating condition is never satisfied.

Q: What is an algorithm?
A: A general process for solving a category of problems.
