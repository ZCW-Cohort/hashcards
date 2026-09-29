Q: What Java package contains the classes for networking functionality?
A: java.net

Q: What are the two main types of sockets used in Java networking?
A: Client sockets and server sockets

Q: What is a Socket in Java?
A: An object that represents a network connection between two machines, allowing them to communicate by sending and receiving data

Q: What two pieces of information does a client need to make a Socket connection to a server?
A: The IP address (or domain name) and the TCP port number of the server

C: A TCP port is a [16-bit number] that identifies a specific program on the server.

C: TCP port numbers from [0 to 1023] are reserved for well-known services and should not be used for custom server programs.

Q: How do you create a client Socket connection in Java?
A: Socket chatSocket = new Socket("196.164.1.103", 5000);

Q: What stream classes are used to read text data from a Socket?
A: BufferedReader chained to an InputStreamReader, which is chained to the Socket's input stream

Q: What stream class is commonly used to write text data to a Socket?
A: PrintWriter

C: To read from a Socket, you need to chain a [BufferedReader] to an [InputStreamReader] to the Socket's [input stream].

Q: What does a ServerSocket do?
A: It waits for client requests on a specific port and creates Socket connections with clients when they connect

Q: What method does a ServerSocket use to wait for and accept client connections?
A: accept()

C: The [accept()] method blocks until a client connects, then returns a [Socket] on a different port for communicating with that client.

Q: Why does a ServerSocket need to create connections on different ports?
A: So the ServerSocket can continue waiting for other clients on the original port while communicating with connected clients on other ports

Q: What is a thread in Java?
A: A separate thread of execution with its own call stack, allowing multiple tasks to run concurrently

C: A thread (lowercase 't') is a separate [thread of execution] with its own [call stack].

C: A Thread (uppercase 'T') is a Java [class] in the [java.lang] package that represents a thread of execution.

Q: What interface must a class implement to define a job for a thread?
A: Runnable

Q: What method must be implemented by a class that implements Runnable?
A: public void run()

C: To launch a new thread, you need a [Runnable] to pass to the Thread's [constructor].

Q: How do you start a new thread in Java?
A: Create a Thread object with a Runnable, then call the start() method on the Thread object

Q: What are the three main states a thread can be in?
A: NEW, RUNNABLE, and RUNNING

C: A thread is in the [NEW] state when it has been instantiated but [start()] has not yet been called.

C: When you call [start()] on a Thread, it moves to the [RUNNABLE] state and a new [call stack] is created.

Q: What decides which runnable thread becomes the running thread?
A: The JVM's thread scheduler

Q: Can you control or guarantee thread scheduling behavior in Java?
A: No, there are no guarantees about scheduling. It varies by JVM and platform

C: The static [Thread.sleep()] method forces a thread to leave the [running state] for at least the specified duration.

Q: What exception does Thread.sleep() throw?
A: InterruptedException (a checked exception)

Q: After a thread wakes up from sleep, what state does it return to?
A: RUNNABLE (not RUNNING - it must wait to be selected by the scheduler again)

Q: What does the synchronized keyword do?
A: It prevents two threads from entering a synchronized method at the same time by requiring a thread to obtain the object's lock

C: Every Java object has a [lock] with only [one key] for that lock.

Q: When does a thread need an object's key?
A: When it wants to enter a synchronized method on that object

C: If an object has multiple synchronized methods, there is still only [one key]. Once any thread enters a synchronized method, [no other thread] can enter any synchronized method on that object.

Q: What is the "Lost Update" problem?
A: When one thread reads a value, gets interrupted, and another thread modifies that value before the first thread completes its operation, causing the first thread's update to be lost

Q: What is a race condition?
A: A situation where two or more threads access shared data concurrently and the outcome depends on the timing of their execution

Q: What is thread deadlock?
A: When two threads each hold a lock that the other needs, causing both to wait forever

C: Deadlock requires at least [two objects] and [two threads], where each thread holds a lock the other needs.

Q: Where should you use synchronization in your code?
A: On methods that access or modify data that could be accessed by multiple threads

Q: Should you synchronize everything to be safe?
A: No. Synchronization has performance overhead and can reduce concurrency. Only synchronize what is necessary

C: The goal of synchronization is to make specific sections of code work [atomically], as one unbreakable unit.

Q: What does it mean for code to execute atomically?
A: The code must run to completion as one unit without interruption from other threads

Q: Can you synchronize at a finer granularity than a whole method?
A: Yes, you can use synchronized(this) blocks within a method to synchronize only specific statements

Q: What is the purpose of the IncomingReader class in the SimpleChatClient?
A: It runs in a separate thread to continuously read incoming messages from the server while the main thread handles the GUI

C: A chat client needs [two things at once]: to [send messages] to the server and simultaneously [receive messages] from the server.

Q: Why can't a dead thread be restarted?
A: Once a thread's run() method completes, the thread moves to the dead state and loses its threadness permanently

