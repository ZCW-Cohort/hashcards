Q: What are the three main deployment options for Java applications?
A: Local (100% on client as executable JAR), Combination (client-server with Java Web Start or RMI), and Remote (100% on server as Servlets accessed through web browser)

C: Organizing your project requires separating [source code] and [class files] into different directories.

Q: What does the -d compiler flag do?
A: It tells the compiler to put the compiled class files into a specified directory instead of the same directory as the source code.

C: A [JAR] file is a Java Archive based on the pkzip format that bundles all your classes into a single file.

Q: What is a manifest file and what does it contain?
A: A manifest file is a text file that goes in a JAR and contains metadata about the JAR files. For an executable JAR, it must specify which class has the main() method.

Q: How do you create an executable JAR?
A: Create a manifest.txt file with "Main-Class: ClassName", then run: jar -cvmf manifest.txt app.jar *.class

C: To run an executable JAR file, use the command: java -jar [filename.jar]

Q: Why should you put your classes into packages?
A: To prevent class name conflicts with other developers' classes and to organize your code in a meaningful hierarchy.

C: Package names should be prefixed with your [reverse domain name] to guarantee uniqueness.

Q: What must be the first statement in a source code file when using packages?
A: The package statement must be the first statement, before any import statements.

C: To be truly in a package, a class must be in a [directory structure] that exactly matches the package hierarchy.

Q: How do you compile a class in a package using the -d flag?
A: From the source directory: javac -d ../classes com/packagename/ClassName.java

Q: How do you run a class that's in a package?
A: From the classes directory, use the fully-qualified class name: java com.packagename.ClassName

C: When you use the -d flag, the compiler will [build the directories] if they don't exist.

Q: When creating a JAR with packages, what must be inside the JAR?
A: The complete package directory structure must be inside the JAR, starting with the first directory of the package (usually "com").

C: To create a JAR with packages: jar -cvmf manifest.txt packEx.jar [com]

Q: What are the two jar commands for examining JAR contents?
A: jar -tf filename.jar (lists contents) and jar -xf filename.jar (extracts contents)

C: The jar tool automatically creates a [META-INF] directory and puts the manifest information in [MANIFEST.MF].

Q: What is Java Web Start?
A: A technology that lets you deploy stand-alone client applications from the Web, with automatic updating capabilities.

C: A Java Web Start application consists of two main pieces: an [executable JAR] and a [.jnlp file].

Q: What is a .jnlp file?
A: A Java Network Launch Protocol file - an XML document that describes the JWS application, including the JAR location and the main class.

C: The [JWS helper app] is a small Java program on the client that manages downloading, updating, and launching JWS applications.

Q: What happens when a user clicks a Web page link to a JWS application?
A: The browser requests the .jnlp file, starts the JWS helper app, which reads the .jnlp file, requests the JAR from the server, and launches the application by calling its main() method.

C: The codebase tag in a .jnlp file specifies the [root directory] where your web start files are located on the server.

Q: What does the offline-allowed tag in a .jnlp file mean?
A: It means the user can run the program without being connected to the internet, though automatic updating won't work offline.

C: To make a JWS app work, you must add the mime type [application/x-java-jnlp-file] to your web server configuration.

Q: What are the five steps for deploying a Java Web Start application?
A: Make an executable JAR, write a .jnlp file, place JAR and .jnlp on web server, add mime type to server, create web page with link to .jnlp file.

C: The [application-desc] tag in a .jnlp file specifies which class has the main() method.

Q: How is Java Web Start different from an applet?
A: JWS apps run outside the browser as stand-alone applications and can be relaunched without the browser. Applets must run inside the browser and have more restrictions.

C: JWS applications are restricted from reading and writing to the user's hard drive except in a [special restricted area] with user permission.

Q: What is the standard organizational structure for Java projects?
A: Create a project directory with separate "source" and "classes" subdirectories inside it.

C: When you separate source and classes, you compile from the [source] directory and run from the [classes] directory.

Q: What happens if you try to run a class in a package from the wrong directory?
A: The JVM won't find the class because it looks for a directory structure matching the package hierarchy.

C: The package directory structure must start [immediately inside] the JAR file, not nested in other directories.

Q: Why is it important to use the -d flag when compiling?
A: It automatically creates the correct package directory structure and prevents typos in manually creating directories.

C: All classes in a source file must be in the [same package] because there can be only one package statement per source file.

Q: What is the purpose of the reverse domain naming convention for packages?
A: Domain names are guaranteed to be unique, so using your reverse domain prevents package name collisions with other developers.

C: Package names typically use [lowercase] letters, while class names use [capitalized] first letters.

Q: Can the JVM use classes directly from a JAR without extracting them?
A: Yes, the JVM can load and run classes directly from a JAR file.

Q: What information do the "information" tags in a .jnlp file provide?
A: Metadata like title, vendor, description, and icon that the JWS helper app uses when displaying the application.

C: The [j2se version] tag in a .jnlp file specifies the minimum version of Java required to run the application.

Q: After a JWS application is downloaded, how can users launch it again?
A: Users can open the Java Web Start helper application and launch the app from there without going through the web browser.

Q: What is the key benefit of JWS's automatic updating feature?
A: JWS can detect when even a single class file has changed on the server and automatically download and integrate the updated code.

C: To compile all .java files in a package directory: javac -d ../classes com/packagename/[*.java]

Q: What does the jar tool do with your manifest.txt file?
A: It reads the contents and puts them into the MANIFEST.MF file inside the META-INF directory in the JAR.

C: The three deployment options range from [100% Local] to [Combination] to [100% Remote].
