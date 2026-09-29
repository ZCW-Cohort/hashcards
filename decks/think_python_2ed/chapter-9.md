Q: What is the purpose of this chapter's case study?
A: Solving word puzzles by searching for words that have certain properties, such as finding the longest palindromes in English and searching for words whose letters appear in alphabetical order.

C: The program development plan presented in this chapter is [reduction to a previously solved problem].

Q: What is the Moby lexicon project?
A: A collection of word lists contributed to the public domain by Grady Ward, including a list of 113,809 official crossword words.

Q: What does the built-in function open() do?
A: It takes the name of a file as a parameter and returns a file object you can use to read the file.

C: A common name for a [file object] used for input is fin.

Q: What does the readline() method do?
A: It reads characters from the file until it gets to a newline and returns the result as a string.

C: The sequence [\n] represents the newline character that separates words in the file.

Q: What does the strip() method do?
A: It removes whitespace characters, including newlines, from the beginning and end of a string.

Q: How can you use a file object in a loop?
A: You can use a file object as part of a for loop to iterate through each line in the file.

Q: What function returns True if a word doesn't have the letter "e" in it?
A: has_no_e

C: The function [avoids] takes a word and a string of forbidden letters, and returns True if the word doesn't use any of the forbidden letters.

Q: What does the uses_only function do?
A: It takes a word and a string of letters, and returns True if the word contains only letters in the list.

C: The function [uses_all] takes a word and a string of required letters, and returns True if the word uses all the required letters at least once.

Q: What does is_abecedarian check for?
A: It returns True if the letters in a word appear in alphabetical order (double letters are ok).

C: The [search pattern] is a common approach used to solve all of the exercises in section 9.2.

Q: In the has_no_e function, when do you return False?
A: As soon as you find the letter "e" in the word.

Q: In the has_no_e function, when do you return True?
A: When you exit the loop normally without finding an "e".

C: The [avoids] function is a more general version of has_no_e but has the same structure.

Q: How does uses_only differ from avoids?
A: The sense of the condition is reversed - instead of forbidden letters, it has available letters, and returns False if it finds a letter not in available.

Q: How does uses_all reverse the role of word and string of letters?
A: Instead of traversing the letters in word, the loop traverses the required letters, checking if each required letter appears in the word.

C: [Reduction to a previously solved problem] means that you recognize the problem you are working on as an instance of a solved problem and apply an existing solution.

Q: How can uses_all be written using uses_only?
A: return uses_only(required, word)

Q: Why is comparing adjacent letters tricky with a for loop in is_abecedarian?
A: Because you need to keep track of the previous letter to compare it with the current one.

Q: What are three ways to implement is_abecedarian?
A: Using a for loop with a previous variable, using recursion, or using a while loop with indices.

C: In the while loop version of is_abecedarian, the loop starts at i=[0] and ends when i=[len(word)-1].

Q: What does the is_palindrome function with two indices do?
A: It uses one index starting at the beginning going up and another starting at the end going down, comparing characters at each position.

Q: Why is testing programs hard according to this chapter?
A: It is difficult or impossible to choose a set of words that test for all possible errors.

Q: What are the two obvious cases to check for has_no_e?
A: Words that have an 'e' should return False, and words that don't should return True.

C: The [empty string] is an example of a special case where errors often lurk.

Q: What are some subcases to test for words that have an "e"?
A: Words with an "e" at the beginning, the end, and somewhere in the middle; long words, short words, and very short words like the empty string.

Q: What did Edsger W. Dijkstra say about program testing?
A: Program testing can be used to show the presence of bugs, but never to show their absence!

Q: What is a file object?
A: A value that represents an open file.

Q: What is reduction to a previously solved problem?
A: A way of solving a problem by expressing it as an instance of a previously solved problem.

Q: What is a special case?
A: A test case that is atypical or non-obvious (and less likely to be handled correctly).
