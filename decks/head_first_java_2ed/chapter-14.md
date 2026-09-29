C: Objects can be [flattened] and [inflated] through serialization.

Q: What are the two main options for saving object state in Java?
A: 1) Use serialization to write flattened objects to a file, which can be read back and inflated into living objects. 2) Write a plain text file with delimiters that other programs can parse.

C: [Behavior] lives in the class, but [state] lives within each individual object.

Q: What are connection streams and chain streams?
A: Connection streams represent connections to destinations and sources such as files or network sockets. Chain streams work only if chained to other streams and cannot connect on their own.

C: To serialize an object to a file, make a [FileOutputStream] and chain it into an [ObjectOutputStream].

Q: What are the four steps for writing a serialized object to a file?
A: 1) Make a FileOutputStream, 2) Make an ObjectOutputStream, 3) Write the object, 4) Close the ObjectOutputStream.

C: If the file doesn't exist, [FileOutputStream] will create it automatically.

Q: How do you make a class serializable?
A: Implement the Serializable interface. It's a marker interface with no methods to implement.

C: When an object is serialized, all the objects it refers to from [instance variables] are also serialized.

Q: What happens when you serialize an object with instance variable references to other objects?
A: When an object is serialized, all the objects it refers to from instance variables are also serialized. And all the objects those objects refer to are serialized. The entire object graph is saved automatically.

C: Serialization saves the entire [object graph].

Q: What does it mean that "serialization is all or nothing"?
A: Either the entire object graph is serialized correctly or serialization fails. You can't serialize a Pond object if its Duck instance variable refuses to be serialized.

C: Mark an instance variable as [transient] if it can't or shouldn't be saved.

Q: What happens to transient variables during serialization?
A: Transient variables are skipped during serialization. They come back as null for object references or default values for primitives when the object is deserialized.

C: [Static] variables are not serialized because they mean "one per class" not "one per object".

Q: What are the steps for deserializing an object from a file?
A: 1) Make a FileInputStream, 2) Make an ObjectInputStream, 3) Read the objects, 4) Cast the objects, 5) Close the ObjectInputStream.

C: The return type of readObject() is type [Object], so deserialized objects must be cast to their real type.

Q: What happens during deserialization?
A: 1) The object is read from the stream. 2) The JVM determines the object's class type. 3) The JVM attempts to find and load the class. 4) A new object is given space on the heap, but the constructor does NOT run. 5) If the object has a non-serializable class up its inheritance tree, that constructor will run. 6) Instance variables are given values from the serialized state.

C: When an object is deserialized, the serialized object's [constructor] does NOT run.

Q: What is serialVersionUID and why is it important?
A: Each time an object is serialized, it's stamped with a version ID number called serialVersionUID. When deserializing, if the class has changed and has a different serialVersionUID, deserialization will fail. You can control this by putting a serialVersionUID in your class.

C: To get a serialVersionUID for a class, use the [serialver] tool that ships with your Java development kit.

Q: What are some changes to a class that can hurt deserialization?
A: Deleting an instance variable, changing the declared type of an instance variable, changing a non-transient instance variable to transient, moving a class up or down the inheritance hierarchy, changing a class from Serializable to not Serializable, and changing an instance variable to static.

C: To write a String to a text file, start with a [FileWriter] connection stream.

Q: How do you write a String to a text file?
A: Create a FileWriter object and call its write() method with the String. Chain the FileWriter to a BufferedWriter for efficiency.

C: A [File] object represents a file on disk, but doesn't actually represent the contents of the file.

Q: What are some things you can do with a File object?
A: 1) Make a File object representing an existing file, 2) Make a new directory, 3) List the contents of a directory, 4) Get the absolute path of a file or directory, 5) Delete a file or directory.

C: [BufferedWriter] holds data in a buffer until it's full, making file writing more efficient.

Q: How do you read text from a file?
A: Use a File object to represent the file, a FileReader to do the actual reading, and a BufferedReader to make the reading more efficient. Read lines in a while loop, ending when readLine() returns null.

C: The String [split()] method lets you break a String into pieces using a separator.

Q: What does the String split() method do?
A: It takes a separator and breaks the String into pieces, putting them in a String array. The separator doesn't count as a token.

C: [FileReader] and [FileWriter] are for working with text files, not serialized objects.

Q: What is the difference between serialization and writing to a text file?
A: Serialization saves the entire object graph automatically and is for data used only by Java programs. Text files are for data that other programs need to read, require explicit formatting with delimiters, and need manual parsing.

C: When using BufferedWriter, you can call [flush()] to send data before the buffer is full.

Q: What happens if two objects in an object graph are the same object?
A: Serialization is smart enough to know when two objects in the graph are the same. Only one of the objects is saved, and during deserialization, any references to that single object are restored.

C: If a superclass is not serializable, the [constructor] for that non-serializable class will run during deserialization.

Q: Why would you mark a variable as transient?
A: 1) The class of the instance variable isn't serializable, 2) The object relies on runtime-specific information that can't be saved (like network connections, threads, or file objects), 3) For security reasons you don't want that variable saved.

C: Connection streams represent a connection to a [source] or [destination], while chain streams cannot connect on their own and must be chained to a [connection stream].

Q: What is the purpose of BufferedReader and BufferedWriter?
A: They provide buffering for more efficient reading and writing. Instead of going to the disk for each operation, they hold data in memory until the buffer is full, reducing the number of expensive disk operations.