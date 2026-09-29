C: A [JFrame] is the object that represents a window on the screen.

Q: What are the four steps to making a GUI?
A: 1) Make a frame (a JFrame), 2) Make a widget (button, text field, etc.), 3) Add the widget to the frame, 4) Display it (give it a size and make it visible).

C: You don't add things to the [frame] directly. You add things to the frame's [content pane].

Q: How do you add a widget to a JFrame?
A: Use frame.getContentPane().add(widget);

C: To make the window display, you must give it a [size] and make it [visible].

Q: What does setDefaultCloseOperation do?
A: It makes the program quit as soon as you close the window. Without this line, the window will just sit there on the screen forever.

C: In Java, the process of getting and handling a user event is called [event-handling].

Q: What two things do you need to get a button to do something when clicked?
A: A method to be called when the user clicks (the thing you want to happen as a result of the button click), and a way to know when to trigger that method.

C: If you want to know about a button's events, you must [implement] an interface that says, "I'm listening for your events."

Q: What is a listener interface?
A: A listener interface is the bridge between the listener (you) and event source (the button). When you implement a listener interface, you give the button a way to call you back.

C: Every event type has a matching [listener] interface.

Q: What are the three steps to getting a button's ActionEvent?
A: 1) Implement the ActionListener interface, 2) Register with the button (tell it you want to listen for events), 3) Define the event-handling method (implement the actionPerformed() method from the ActionListener interface).

C: The listener interface gives the event source a way to [call you back], because the interface defines the method(s) the event source will call when an event happens.

Q: What does it mean to register for events?
A: To register for events, you call the source's registration method. Registration methods always take the form of: add<EventType>Listener. For example, button.addActionListener(this).

C: To register for a button's ActionEvents, call [button.addActionListener(this)].

Q: What is the event-handler method for ActionEvents?
A: actionPerformed(ActionEvent event)

C: The event object passed into the event-handler method carries [information] about the event, including the source of the event.

Q: What are the three roles in event-handling?
A: Event source (sends the event), listener (gets the event), and event object (holds data about the event).

C: An [event source] is an object that can turn user actions (click a mouse, type a key, close a window) into events.

Q: How do you know if an object is an event source?
A: Look in the API for a method that starts with 'add', ends with 'Listener', and takes a listener interface argument. For example, addKeyListener(KeyListener k) means the class is a source of KeyEvents.

C: A button is a source of [ActionEvents].

Q: What are three ways to put things on your GUI?
A: 1) Put widgets on a frame, 2) Draw 2D graphics on a widget, 3) Put a JPEG on a widget.

C: To draw your own graphics, make a subclass of [JPanel] and override the [paintComponent()] method.

Q: What is the paintComponent() method?
A: The paintComponent() method is called by the GUI system to say "Hey widget, time to paint yourself." All of your graphics code goes inside this method. You never call this method yourself.

C: The argument to paintComponent() is a [Graphics] object that gives you a surface to draw on, which will end up on the screen.

Q: What are some typical methods to call on a Graphics object?
A: g.setColor(Color.blue), g.fillRect(20,50,100,120), g.drawImage(image,3,4,this), g.fillOval(70,70,100,100).

C: The object referenced by the Graphics parameter to paintComponent() is actually an instance of the [Graphics2D] class.

Q: How do you use Graphics2D methods in paintComponent()?
A: You must cast the Graphics parameter to Graphics2D: Graphics2D g2d = (Graphics2D) g;

C: A [GradientPaint] lets you paint with a gradient blend instead of a solid color.

Q: What are the five regions of a frame by default?
A: North, South, East, West, and Center.

C: When you add a widget to a frame, you should always specify [which region] you want the widget to go in.

Q: What is the proper way to add a widget to a frame?
A: frame.getContentPane().add(BorderLayout.CENTER, button); - specifying both the region and the widget.

C: You can add only [one] thing to each region of a frame.

Q: How can you add more than one widget to a region?
A: That one thing might be a panel that holds three other things including a panel that holds two more things, and so on.

C: An [inner class] is a class defined within another class.

Q: What is the benefit of an inner class?
A: An inner class can use all the methods and variables of the outer class, even the private ones. The inner class gets to use those variables and methods just as if they were declared within the inner class.

C: An inner class instance must be tied to a specific [outer class instance].

Q: How do you make an instance of an inner class from code within the outer class?
A: Code in an outer class can instantiate one of its own inner classes in exactly the same way it instantiates any other class: new MyInner()

C: Inner classes are useful when you need to implement the same [interface] more than once in a class.

Q: Why can't you implement the same method twice in a Java class?
A: You can't implement a method more than once in a normal Java class. But using inner classes, each inner class can implement the same interface, so you can have different implementations of the same interface methods.

C: Inner classes let the outer and inner classes pass different [IS-A] tests.

Q: What happens if you need to pass the IS-A test for two different classes that aren't in the same inheritance tree?
A: You can always implement more than one interface, but you can extend only one class. You can only be one kind of IS-A when it comes to class types. An inner class can extend a different class than the outer class.

C: An inner object shares a special [bond] with an outer object.

Q: Can an inner object be tied to any outer object?
A: No. An inner object must be tied to a specific outer object on the heap. Once bonded, it's for life.

C: Simple animation works by painting an object at a particular x and y coordinate, then repainting the object at a [different] x and y coordinate.

Q: How do you make simple animation work?
A: 1) Paint an object at a particular x and y coordinate, 2) Repaint the object at a different x and y coordinate, 3) Repeat the previous step with changing x and y values for as long as the animation is supposed to continue.

C: To avoid smearing in animation, you must fill in the entire panel with the [background color] before painting the object each time.

Q: What method do you call to request that a component be repainted?
A: repaint()

C: When you call repaint() on a frame, the system calls [paintComponent()] on every widget in the frame.

Q: What is a ControllerEvent in MIDI?
A: A ControllerEvent is a type of MIDI event you can listen for. It's used as a workaround when you can't listen for the actual NOTE ON/OFF events you're making.

C: To listen for MIDI ControllerEvents, implement the [ControllerEventListener] interface.

Q: How do you register for ControllerEvents?
A: sequencer.addControllerEventListener(this, eventsIWant); where eventsIWant is an int array representing the list of ControllerEvents you want.

C: The event-handler method for ControllerEvents is [controlChange(ShortMessage event)].

Q: How do you create a ControllerEvent that fires at the same time as a NOTE ON event?
A: Add it to the track at the same tick: track.add(makeEvent(176,1,127,0,i)); where 176 is the message type for ControllerEvent, 127 is the event number, and i is the tick.