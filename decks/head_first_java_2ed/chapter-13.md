C: [Component] is the more correct term for what we've been calling a widget.

Q: What are the four steps to making a GUI?
A: 1) Make a window (a JFrame), 2) Make a component (button, text field, etc.), 3) Add the component to the frame, 4) Display it (give it a size and make it visible).

C: Almost everything you can stick in a GUI extends from [javax.swing.JComponent].

Q: What is a layout manager?
A: A layout manager is a Java object associated with a particular component, almost always a background component. The layout manager controls the components contained within the component the layout manager is associated with.

C: A layout manager controls the [size] and [placement] of components.

Q: What does it mean when we say a panel holds a button?
A: When we say hold we really mean add as in, a panel holds a button because the button was added to the panel using something like: myPanel.add(button).

C: The panel's layout manager controls only the things added [directly] to the panel, and does not control anything nested within those added components.

Q: How does the layout manager decide on component size and placement?
A: The layout manager asks each component how big that component prefers to be, then uses its layout policies to decide whether it should respect all, part, or none of the component's preferences.

C: Different layout managers have different [policies] for arranging components.

Q: What are the Big Three layout managers?
A: BorderLayout, FlowLayout, and BoxLayout.

C: [BorderLayout] is the default layout manager for a frame, and [FlowLayout] is the default layout manager for a panel.

Q: How does BorderLayout work?
A: A BorderLayout manager divides a background component into five regions. You can add only one component per region to a background controlled by a BorderLayout manager. Components laid out by this manager usually don't get to have their preferred size.

C: The five regions of BorderLayout are [east], [west], [north], [south], and [center].

Q: What size does BorderLayout give to components in different regions?
A: Components in the east and west get their preferred width, but not height. Components in the north and south get their preferred height, but not width. The component in the center gets whatever is left over (except in one special case).

C: With BorderLayout, you must specify the [region] when you add a component.

Q: How does FlowLayout work?
A: A FlowLayout manager acts kind of like a word processor, except with components instead of words. Each component is the size it wants to be, and they're laid out left to right in the order that they're added, with "word-wrap" turned on.

C: FlowLayout places components [left to right], [top to bottom], in the order they were added, wrapping to a new line when needed.

Q: How does BoxLayout work?
A: A BoxLayout manager is like FlowLayout in that each component gets to have its own size, and the components are placed in the order in which they're added. But, unlike FlowLayout, a BoxLayout manager can stack the components vertically (or horizontally, but usually we're just concerned with vertically).

C: BoxLayout can force components to start a new line, even if there's room to [fit horizontally].

Q: How do you change a panel's layout manager?
A: You have to call setLayout() on the panel with a new layout manager instance.

C: To use BoxLayout, you must specify the [component] being laid out and the [axis] to use.

Q: Why can't you add directly to a frame the way you can to a panel?
A: A JFrame is special because it's where the rubber meets the road in making something appear on the screen. While all your Swing components are pure Java, a JFrame has to connect to the underlying OS in order to access the display. You add to the frame's content pane.

C: You can swap the content pane with your own JPanel by calling [myFrame.setContentPane(myPanel)].

Q: What is a JTextField?
A: A text field component that allows single-line text input and editing.

C: When constructing a JTextField, the number passed to the constructor represents [columns], not pixels.

Q: How do you get an event when the user presses enter in a JTextField?
A: Register an ActionListener with the text field using field.addActionListener(myActionListener).

C: To get text out of a JTextField, use [field.getText()].

Q: What is JTextArea?
A: A text area component that can have more than one line of text. It takes a little configuration to make one, because it doesn't come out of the box with scroll bars or line wrapping.

C: To make a JTextArea scroll, you have to stick it in a [ScrollPane].

Q: How do you add a scrollable text area to a panel?
A: You give the text area to the scroll pane (through the scroll pane constructor), then add the scroll pane to the panel. You don't add the text area directly to the panel.

C: The constructor JTextArea(10, 20) creates a text area with [10] lines and [20] columns.

Q: What is a JCheckBox?
A: A checkbox component that can be selected or deselected by the user.

C: To listen for checkbox events, implement the [ItemListener] interface.

Q: What is the event-handler method for checkbox events?
A: itemStateChanged(ItemEvent ev)

C: To determine if a checkbox is selected, call [check.isSelected()].

Q: What is a JList?
A: A list component that displays a list of items from which the user can select one or more items.

C: A JList constructor takes an array of [any object type].

Q: How do you make a JList scrollable?
A: Make a JScrollPane and give it the list, then add the scroll pane (NOT the list) to the panel.

C: To restrict the user to selecting only ONE thing at a time in a list, use [list.setSelectionMode(ListSelectionModel.SINGLE_SELECTION)].

Q: What is the event-handler method for list selection events?
A: valueChanged(ListSelectionEvent lse)

C: The method getSelectedValue() returns an [Object], not necessarily a String.

Q: Why do you get the list selection event twice?
A: You'll get the event TWICE if you don't put in a test for lse.getValueIsAdjusting().

C: The pack() method is like [shrink-wrap] for the components.

Q: What happens when layout managers conflict with component preferences?
A: Some layout managers respect the size the component wants to be, some respect only part of the component's preferred size, and some respect the preference of only the largest of the components being layed out.

C: Layout managers take care of keeping your components from [overlapping] one another.

Q: What happens when the user resizes the window?
A: The layout manager automatically re-lays out all the components based on its policies and the new size of the background component.