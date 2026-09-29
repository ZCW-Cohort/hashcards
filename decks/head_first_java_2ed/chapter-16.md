Q: What is the Java Collections Framework?
A: A set of classes and interfaces in the Java API that provide data structures for collecting and manipulating data without having to write custom sort algorithms.

Q: What are the three main interfaces in the Collection API?
A: List, Set, and Map

C: [ArrayList] maintains elements in the order they were inserted into the list.

C: A [Set] prevents duplicates in the collection.

Q: What method do you call to sort an ArrayList of Strings?
A: Collections.sort(list)

C: The Collections.sort() method can only take lists of [Comparable] objects.

Q: What two methods must you override to make objects sortable and prevent duplicates in a HashSet?
A: hashCode() and equals()

C: To implement the Comparable interface, you must implement the [compareTo()] method.

Q: What does the compareTo() method return?
A: A negative integer if this object is less than the specified object, zero if equal, or a positive integer if greater than the specified object.

C: A [Comparator] is external to the element type you're comparing and allows you to create multiple ways to sort the same type.

Q: What method must you implement when creating a Comparator?
A: compare(T o1, T o2)

C: When you use generics, the keyword "[extends]" means either extends OR implements, depending on whether the type is a class or interface.

Q: What's the difference between reference equality and object equality?
A: Reference equality means two references point to the same object on the heap (checked with ==). Object equality means two references point to different objects that are considered meaningfully equivalent (checked with equals()).

C: If two objects are equal, they MUST have matching [hashcodes].

Q: Why does HashSet use both hashCode() and equals()?
A: HashSet uses hashCode() to quickly find the bucket where an object might be stored, then uses equals() to check if the exact object is actually in that bucket.

C: A [TreeSet] keeps elements sorted and prevents duplicates.

Q: What are two ways to make TreeSet know how to sort elements?
A: Either the elements must implement Comparable, or you must pass a Comparator to the TreeSet constructor.

C: In a [Map], each element is actually two objects—a key and a value.

Q: Can a Map have duplicate keys?
A: No, but it can have duplicate values.

C: The [wildcard] syntax <?> allows you to create method arguments that accept collections of any subtype.

Q: When you use a wildcard in a method parameter like ArrayList<? extends Animal>, what can't you do?
A: You cannot add elements to the list. You can only invoke methods on the elements already in the list.

C: Array types are checked at [runtime], but collection type checks happen only at compile time.

Q: Why won't the compiler let you pass an ArrayList<Dog> to a method declared to take ArrayList<Animal>?
A: Because someone could add a Cat to what was supposed to be a Dogs-only list, and the compiler prevents this potential runtime error.

C: [ArrayList] is the most commonly used List implementation.

Q: What is the key difference between ArrayList and TreeSet regarding performance?
A: ArrayList inserts are very fast because elements just go at the end. TreeSet takes time to figure out where in the tree each new element must go.

C: [HashMap] lets you store and access elements as name/value pairs.

Q: What does LinkedHashMap do differently than HashMap?
A: It can remember the order in which elements were inserted or the order in which they were last accessed.

C: A [LinkedList] makes it easy to create structures like stacks or queues.

Q: What interface does ArrayList implement that makes it usable with Collections.sort()?
A: List

C: The [HashSet] prevents duplicates but does not maintain any particular order.

Q: What happens if you try to sort a TreeSet of objects that don't implement Comparable and you didn't provide a Comparator?
A: It fails at runtime when you add the second element to the set.

C: You can sort the same collection in different ways by creating different [Comparator] classes.

Q: What are the two forms of flashcards mentioned in this chapter's jukebox example?
A: Standard question and answer form (Q: and A:), and Cloze form (C:) where key words are enclosed in square brackets.

C: The [List] interface knows about index position in the collection.

Q: What does the Collections class contain?
A: Static utility methods for working with collections, including sort(), reverse(), shuffle(), and others.

C: When declaring a generic method, you can put the type parameter declaration [before] the return type.

Q: What's the alternative syntax to using wildcards for generic methods?
A: Declare the type parameter before the return type: public <T extends Animal> void method(ArrayList<T> list)

C: TreeSet elements MUST be [comparable] - either by implementing Comparable or by providing a Comparator to the constructor.

Q: In the Java Object Law for hashCode() and equals(), if two objects have the same hashcode, must they be equal?
A: No, but if two objects are equal, they MUST have the same hashcode.

C: The default behavior of hashCode() is to generate a [unique] integer for each object on the heap.

Q: What is the benefit of using a Set over a List when you need unique elements?
A: A Set automatically prevents duplicates, while a List allows the same element to appear multiple times.
