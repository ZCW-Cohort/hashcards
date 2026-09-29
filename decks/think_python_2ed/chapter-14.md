Q: What are the two types of programs discussed in Chapter 14?
A: Transient programs and persistent programs

Q: What is a persistent program?
A: A program that runs for a long time or all the time, keeps at least some of its data in permanent storage, and can pick up where it left off if it shuts down and restarts

Q: What mode parameter should you use when opening a file for writing?
A: 'w'

Q: What happens if you open an existing file in write mode?
A: It clears out the old data and starts fresh

Q: What does the write method return?
A: The number of characters that were written

C: The [format operator] is represented by the [%] symbol

C: The format sequence [%d] formats a value as a [decimal integer]

C: The format sequence [%g] formats a value as a [floating-point number]

C: The format sequence [%s] formats a value as a [string]

Q: When using multiple format sequences in a string, what must the second argument be?
A: A tuple

C: A string like '/home/dinsdale' that identifies a file or directory is called a [path]

C: A [relative path] starts from the current directory

C: An [absolute path] starts from the topmost directory in the file system

Q: What does os.getcwd() do?
A: Returns the name of the current working directory

Q: What does os.path.abspath() do?
A: Returns the absolute path to a file

Q: What does os.path.exists() check?
A: Whether a file or directory exists

Q: What does os.path.isdir() check?
A: Whether something is a directory

Q: What does os.path.isfile() check?
A: Whether something is a file

Q: What does os.listdir() return?
A: A list of the files and other directories in the given directory

Q: What does os.path.join() do?
A: Takes a directory and a file name and joins them into a complete path

Q: What error do you get if you try to open a file that doesn't exist?
A: FileNotFoundError

Q: What error do you get if you try to open a file without permission?
A: PermissionError

Q: What error do you get if you try to open a directory for reading?
A: IsADirectoryError

C: Handling an exception with a try statement is called [catching] an exception

Q: What is a database in the context of this chapter?
A: A file that is organized for storing data, mapping from keys to values, and persists on disk after the program ends

Q: What module provides an interface for creating and updating database files?
A: dbm

Q: What mode should you use when opening a database with dbm to create it if it doesn't exist?
A: 'c'

Q: What type of object does dbm return when you access an item?
A: A bytes object

C: A limitation of dbm is that the keys and values have to be [strings] or [bytes]

Q: What does the pickle module do?
A: Translates almost any type of object into a string suitable for storage in a database, and then translates strings back into objects

Q: What does pickle.dumps() do?
A: Takes an object as a parameter and returns a string representation

Q: What does pickle.loads() do?
A: Reconstitutes an object from a string representation

Q: What module combines pickle and dbm functionality?
A: shelve

C: A [pipe object] represents a running program

Q: What function launches a command from Python and returns a pipe object?
A: os.popen()

Q: What can you check to determine if a Python file is being run as a script versus being imported?
A: Check if __name__ == '__main__'

Q: What is the value of __name__ when a program is running as a script?
A: '__main__'

Q: What function can help debug whitespace issues by representing them with backslash sequences?
A: repr()

C: Some systems use [\n] to indicate end of line, others use [\r], and some use both

C: [persistent]: Pertaining to a program that runs indefinitely and keeps at least some of its data in permanent storage.

C: [format operator]: An operator, %, that takes a format string and a tuple and generates a string that includes the elements of the tuple formatted as specified by the format string.

C: [format string]: A string, used with the format operator, that contains format sequences.

C: [format sequence]: A sequence of characters in a format string, like %d, that specifies how a value should be formatted.

C: [text file]: A sequence of characters stored in permanent storage like a hard drive.

C: [directory]: A named collection of files, also called a folder.

C: [path]: A string that identifies a file.

C: [relative path]: A path that starts from the current directory.

C: [absolute path]: A path that starts from the topmost directory in the file system.

C: [catch]: To prevent an exception from terminating a program using the try and except statements.

C: [database]: A file whose contents are organized like a dictionary with keys that correspond to values.

C: [bytes object]: An object similar to a string.

C: [shell]: A program that allows users to type commands and then executes them by starting other programs.

C: [pipe object]: An object that represents a running program, allowing a Python program to run commands and read the results.
