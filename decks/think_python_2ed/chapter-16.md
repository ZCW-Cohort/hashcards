Q: What is the chapter about?
A: Writing functions that take programmer-defined objects as parameters and return them as results, functional programming style, and two new program development plans.

C: The [Time] class represents the time of day with attributes hour, minute, and second.

Q: What format sequence prints an integer using at least two digits, including a leading zero if necessary?
A: %.2d

Q: What is a pure function?
A: A function that does not modify any of the objects passed to it as arguments and has no effect other than returning a value.

C: The [prototype and patch] development plan involves writing a simple prototype and incrementally dealing with complications.

Q: What problem occurs with the simple add_time function when adding times?
A: It doesn't handle cases where seconds or minutes add up to more than sixty, requiring "carrying" to the next column.

Q: What are modifiers?
A: Functions that modify the objects they get as parameters, making changes visible to the caller.

C: Functions that use modifiers can also be written as [pure functions].

Q: What is functional programming style?
A: A style of program design in which the majority of functions are pure.

Q: What are the two development plans discussed in the chapter?
A: Prototype and patch, and designed development.

C: In designed development, [high-level insight] into the problem can make programming much easier.

Q: What insight makes working with Time objects easier?
A: A Time object is really a three-digit number in base 60 (sexagesimal).

C: The second attribute is the "ones column", the minute attribute is the "[sixties column]", and the hour attribute is the "thirty-six hundreds column".

Q: What does the divmod function do?
A: It divides the first argument by the second and returns the quotient and remainder as a tuple.

Q: What is a consistency check?
A: A test that verifies time_to_int(int_to_time(x)) == x for many values of x.

C: Converting between base 60 and base 10 provides a program that is [shorter], easier to read and debug, and more [reliable].

Q: Why does making a problem harder or more general sometimes make it easier?
A: Because there are fewer special cases and fewer opportunities for error.

Q: What are invariants?
A: Requirements or conditions that should always be true during program execution.

C: A Time object is well-formed if minute and second are between [0] and [60] (including 0 but not 60) and if hour is [positive].

Q: What does the valid_time function do?
A: It takes a Time object and returns False if it violates an invariant.

Q: What does an assert statement do?
A: It checks a given invariant and raises an exception if it fails.

Q: Why are assert statements useful?
A: They distinguish code that deals with normal conditions from code that checks for errors.

C: [prototype and patch]: A development plan that involves writing a rough draft of a program, testing, and correcting errors as they are found.

C: [designed development]: A development plan that involves high-level insight into the problem and more planning than incremental development or prototype development.

C: [pure function]: A function that does not modify any of the objects it receives as arguments. Most pure functions are fruitful.

C: [modifier]: A function that changes one or more of the objects it receives as arguments. Most modifiers are void; that is, they return None.

C: [functional programming style]: A style of program design in which the majority of functions are pure.

C: [invariant]: A condition that should always be true during the execution of a program.

C: [assert statement]: A statement that checks a condition and raises an exception if it fails.