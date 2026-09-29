Q: What is Remote Method Invocation (RMI)?
A: A Java technology that allows method calls on objects running in different JVMs, making remote method calls appear like local method calls.

C: Method calls are always between two objects on the [same heap].

Q: What are the four main components needed for a remote method call design?
A: Server, client, server helper (skeleton), and client helper (stub).

C: The client helper is called a [stub] and the server helper is called a [skeleton].

Q: What is the role of the client helper (stub) in RMI?
A: It acts as a proxy for the real service, pretending to be the service object. It packages method call information and sends it over the network to the server.

C: The [stub] is a proxy for the Real Thing, handling all low-level networking and I/O details.

Q: What are the five steps for making a remote service?
A: 1) Make a Remote Interface, 2) Make a Remote Implementation, 3) Generate stubs and skeletons using rmic, 4) Start the RMI registry (rmiregistry), 5) Start the remote service.

C: A remote interface must extend [java.rmi.Remote].

Q: Why must all methods in a remote interface declare RemoteException?
A: Because remote method calls involve networking and I/O which are risky operations, and clients must acknowledge the risks by handling or declaring the exceptions.

C: Arguments and return values of remote methods must be [primitives] or [Serializable].

Q: What does the rmic tool do?
A: It takes a service implementation and creates two new classes - the stub (client helper) and the skeleton (server helper).

C: The RMI registry is like the [white pages] of a phone book where clients look up services.

Q: What class should a remote implementation extend?
A: UnicastRemoteObject (from the java.rmi.server package).

C: A remote service must have a constructor that declares a [RemoteException].

Q: How does a client get the stub object?
A: By doing a lookup on the RMI registry using Naming.lookup() with the service name.

C: The Naming.lookup() method returns type [Object], so you must cast it to the remote interface type.

Q: What are the three most common mistakes programmers make with RMI?
A: 1) Forgetting to start rmiregistry before starting the remote service, 2) Forgetting to make arguments and return types serializable, 3) Forgetting to give the stub class to the client.

C: When registering a service, RMI actually puts the [stub] in the registry, not the service itself.

Q: What is a servlet?
A: A Java program that runs on (and with) an HTTP web server, executing code on the server in response to client web page interactions.

C: Servlets extend [HttpServlet] and override methods like doGet() or doPost().

Q: How does a servlet send a response back to the client?
A: By getting a PrintWriter output stream from the response parameter and writing out an HTML page.

C: To compile a servlet, you need the [servlets.jar] file which is not part of the standard Java libraries.

Q: What is JSP and how does it differ from servlets?
A: JSP (Java Server Pages) are HTML pages with embedded Java code, whereas servlets are Java classes with HTML in output statements. JSPs are ultimately converted to servlets by the web server.

C: The most common use of J2EE is to mix [servlets] and [EJBs] together.

Q: What does an Enterprise JavaBeans (EJB) server provide?
A: Services like transactions, security, concurrency, database management, and networking that aren't available with straight RMI.

C: An EJB server steps into the middle of an RMI call and layers in [services].

Q: What are the key features of Jini?
A: Adaptive discovery and self-healing networks, built on top of RMI.

C: With Jini, the client only needs to know the [interface] implemented by the service, not its name or location.

Q: How do Jini lookup services announce themselves?
A: They send a message using IP multicast to the network saying they are available.

C: In Jini, services register by [capability] (interface) rather than by name.

Q: What is a Jini lease?
A: A time-limited registration that services must renew with the lookup service, allowing the lookup service to know when services go offline.

C: If a service fails to renew its [lease], the lookup service drops it from the registry.

Q: In the Universal Service Browser project, what is the Service interface for?
A: It defines the getGuiPanel() method that every universal service must implement, allowing the client to display any service's GUI without knowing the actual class.

C: The Service interface extends [Serializable] so services can be shipped over the network.

Q: What does the ServiceServer remote interface provide?
A: Two methods: getServiceList() to get an array of available services, and getService() to retrieve a specific service.

C: In the Universal Service Browser, services are stored in a [HashMap] collection.

Q: How does the client display a selected service in the Universal Service Browser?
A: It calls getService() on the remote server to get the serialized service, then calls getGuiPanel() on it and adds the returned JPanel to the browser GUI.

C: The [getGuiPanel()] method must return a JPanel that can be displayed in the browser.

Q: What are the protocols that can be used with RMI?
A: JRMP (RMI's native Java-to-Java protocol) or IIOP (CORBA protocol for non-Java objects).

C: [JRMP] is RMI's native protocol, made just for Java-to-Java remote calls.

Q: What is dynamic class downloading in RMI?
A: A feature where stub objects are stamped with a URL that tells the RMI system where to find the class file, allowing automatic HTTP retrieval if the class isn't found locally.

C: With dynamic class downloading, the client can retrieve class files via [HTTP Get] if they're not available locally.

Q: What must be true for an object to be sent as an argument or return value in RMI?
A: It must be either a primitive type or implement Serializable so it can be packaged and shipped across the network.
