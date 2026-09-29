C: Exception handling is Java's mechanism for dealing with [risky] code that might fail at runtime.

Q: What happens when a method throws an exception?
A: The method is popped off the stack immediately, and the exception is thrown to the next method down the stack - the caller.

C: A method can throw an exception when something [fails] at runtime.

Q: How do you know if a method throws an exception?
A: You find a throws clause in the risky method's declaration.

C: An exception is always an object of type [Exception].

Q: What are the two ways to satisfy the compiler when you call a risky method?
A: HANDLE - wrap the risky call in a try/catch, or DECLARE - declare that your method throws the same exceptions as the risky method you're calling.

C: The compiler does NOT pay attention to exceptions that are of type [RuntimeException].

Q: What is a RuntimeException?
A: RuntimeException is a special type of exception that does not have to be declared or caught. RuntimeExceptions can be thrown anywhere, with or without throws declarations or try/catch blocks.

C: All Exceptions the compiler cares about are called [checked] exceptions.

Q: Why doesn't the compiler care about RuntimeExceptions?
A: Most RuntimeExceptions come from a problem in your code logic, rather than a condition that fails at runtime in ways that you cannot predict or prevent. You WANT RuntimeExceptions to happen at development and testing time.

C: A method throws an exception with the keyword [throw], followed by a new exception object.

Q: What is the syntax for wrapping risky code in a try/catch?
A: try { // risky code } catch(ExceptionType ex) { // recovery code }

C: Methods that might throw a checked exception must announce it with a [throws] Exception declaration.

Q: What is an exception object?
A: An exception is an object of type Exception. What you catch is an object. The catch argument is declared as a specific exception type, and the parameter reference variable is your reference to the exception object.

C: If you're prepared to handle the exception, wrap the call in a [try/catch], and put your exception handling code in the catch block.

Q: What are the two key methods that all exceptions inherit?
A: getMessage() and printStackTrace()

C: If you're not prepared to handle the exception, you can still make the compiler happy by officially [ducking] the exception.

Q: What is flow control in a try/catch when the try succeeds?
A: The try block runs, the catch block does NOT run, then the code below the catch runs.

C: A [try/catch] block tells the compiler that you know an exceptional thing could happen and that you're prepared to handle it.

Q: What is flow control in a try/catch when the try fails?
A: The try block runs but the risky code throws an exception, the rest of the try block doesn't run, the catch block runs, then the method continues on.

C: A [finally] block is where you put code that must run regardless of an exception.

Q: When does a finally block run?
A: If the try block fails (an exception), flow control immediately moves to the catch block. When the catch block completes, the finally block runs. If the try block succeeds (no exception), flow control skips over the catch block and moves to the finally block.

C: If the try block fails, flow control immediately moves to the [catch] block.

Q: Will a finally block run even if the try or catch block has a return statement?
A: Yes. Flow jumps to the finally, then back to the return.

C: If the try block succeeds, flow control skips over the [catch] block and moves to the finally block.

Q: Can a method throw multiple exceptions?
A: Yes. A method can throw multiple exceptions if it needs to. The method's declaration must declare all the checked exceptions it can throw.

C: A try/catch is for handling [exceptional] situations, not flaws in your code.

Q: How do you catch multiple exceptions?
A: Stack the catch blocks under the try, one after the other. The compiler will make sure that you've handled all the checked exceptions thrown by the method you're calling.

C: Exceptions are [polymorphic].

Q: Why are exceptions polymorphic?
A: Exceptions are objects, so like all good objects, they can be referred to polymorphically. A method doesn't have to explicitly declare every possible exception it might throw; it can declare a superclass of the exceptions.

C: You can DECLARE exceptions using a [supertype] of the exceptions you throw.

Q: Can you catch exceptions using a supertype?
A: Yes. You can catch exceptions using a supertype of the exception thrown. The catch doesn't have to be for the exact class of exception thrown.

C: You can CATCH exceptions using a [supertype] of the exception thrown.

Q: Should you always catch all exceptions with one big super polymorphic catch?
A: No. Just because you CAN doesn't mean you SHOULD. Write a different catch block for each exception that you need to handle uniquely.

C: Multiple catch blocks must be ordered from [smallest] to biggest.

Q: What happens if you put bigger catch baskets above smaller ones?
A: It won't compile. The compiler knows there's no point in adding catch blocks after a broad one - they'll never be reached.

C: You cannot put bigger baskets [above] smaller baskets.

Q: Can sibling exceptions be in any order in catch blocks?
A: Yes. Siblings can be in any order, because they can't catch one another's exceptions.

C: When you don't want to handle an exception, you can [duck] it by declaring it.

Q: What happens when you duck an exception by declaring it?
A: When a method throws an exception, that method is popped off the stack immediately, and the exception is thrown to the next method down the stack - the caller.

C: Ducking (by declaring) only delays the [inevitable].

Q: What happens if main() ducks an exception?
A: The exception is thrown back to the JVM, and the JVM shuts down.

C: A try MUST be followed by either a [catch] or a finally.

Q: Can you have a try with only a finally (no catch)?
A: Yes, a try with only a finally (no catch) is legal. But you must still declare the exception.

C: You cannot have a catch or finally without a [try].

Q: Can you put code between the try and the catch?
A: No. You cannot put code between the try and the catch.

C: A try with only a finally (no catch) must still [declare] the exception.

Q: What are the four things you need to make actual sound with MIDI?
A: Sequencer (the thing that plays the music), Sequence (the music to be played), Track (the part of the Sequence that holds the actual information), and MidiEvent (the actual music information: notes to play, how long, etc.)

C: The [Sequencer] is the thing that actually causes a song to be played.

Q: What is a Sequence?
A: The Sequence is the song, the musical piece that the Sequencer will play. Think of the Sequence as a music CD, but the whole CD plays just one song.

C: A [MidiEvent] is a message that the Sequencer can understand.

Q: What are the five steps to make MIDI sound?
A: 1) Get a Sequencer and open it, 2) Make a new Sequence, 3) Get a new Track from the Sequence, 4) Fill the Track with MidiEvents and give the Sequence to the Sequencer, 5) Start the Sequencer.

C: MIDI stands for Musical Instrument [Digital] Interface.

Q: What does a MIDI file contain?
A: MIDI data doesn't actually include any sound, but it does include the instructions that a MIDI-reading instrument can play back. MIDI data says what to do (play middle C, and here's how hard to hit it, and here's how long to hold it, etc.)

C: MIDI data doesn't actually include any [sound].

Q: What is a MidiEvent?
A: A MidiEvent is an instruction for part of a song. Most MidiEvents describe a thing to do and the moment in time to do it.

C: A MidiEvent says [what] to do and [when] to do it.

Q: What are the two parts you always need for a MidiEvent?
A: You always need a Message and a MidiEvent. The Message says what to do, and the MidiEvent says when to do it.

C: The [Message] says what to do, the MidiEvent says when to do it.

Q: What are the four arguments to a MIDI message's setMessage() method?
A: Message type (like 144 for NOTE ON or 128 for NOTE OFF), channel (like a musician in a band), note to play (a number from 0 to 127, going from low to high notes), and velocity (how fast and hard you press the key).

C: Message type [144] means NOTE ON.

Q: What does message type 128 mean?
A: 128 means NOTE OFF (stop playing).

C: Message type [128] means NOTE OFF.

Q: What does message type 192 do?
A: 192 is a change-instrument message. The third argument represents the actual instrument (a number between 0 and 127).

C: A MIDI message of type [192] changes the instrument.

Q: How do you change the duration of a note?
A: Change the note off event (not the message) so that it happens at an earlier or later beat.

C: JavaSound is part of the standard [J2SE] class library starting with version 1.3.

Q: What package contains the MIDI classes?
A: The javax.sound.midi package.