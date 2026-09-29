Q: What is analysis of algorithms?
A: A branch of computer science that studies the performance of algorithms, especially their run time and space requirements.

Q: What is the practical goal of algorithm analysis?
A: To predict the performance of different algorithms in order to guide design decisions.

Q: Why is bubble sort considered the wrong way to sort a million integers?
A: Bubble sort is conceptually simple but slow for large datasets.

Q: What are three problems that make comparing algorithms difficult?
A:
- Relative performance might depend on hardware characteristics
- Relative performance might depend on details of the dataset
- Relative performance depends on the size of the problem

Q: What is a machine model in algorithm analysis?
A: A specification of a computing environment used to analyze the number of steps or operations an algorithm requires.

Q: What is the worst case scenario in algorithm analysis?
A: The input or situation that makes a given algorithm run slowest or require the most space.

Q: What is the leading term in a polynomial?
A: The term with the highest exponent.

C: For large values of n, any function that contains an [n²] term will grow faster than a function whose leading term is [n].

Q: What is a crossover point?
A: The problem size where two algorithms require the same run time or space, and one algorithm becomes better than another.

Q: What is an order of growth?
A: A set of functions whose growth behavior is considered equivalent for purposes of algorithm analysis.

C: Functions 2n, 100n and n + 1 all belong to the same order of growth, written [O(n)] in Big-Oh notation.

Q: What are the common orders of growth from best to worst?
A:
- O(1) - constant
- O(log n) - logarithmic
- O(n) - linear
- O(n log n) - linearithmic
- O(n²) - quadratic
- O(n³) - cubic
- O(cⁿ) - exponential

C: An algorithm with order of growth O(n) is called [linear] because its run time is proportional to problem size.

C: An algorithm with order of growth O(n²) is called [quadratic].

Q: Why don't logarithm bases matter in Big-Oh notation?
A: Changing bases is equivalent to multiplying by a constant, which doesn't change the order of growth.

Q: Why are exponential algorithms only useful for small problems?
A: Exponential functions grow very quickly.

Q: What is the order of growth of n³ + n²?
A: O(n³)

C: In Python, most arithmetic operations are [constant time].

Q: What is the exception to arithmetic operations being constant time in Python?
A: Very large integers, where run time increases with the number of digits.

C: Indexing operations in Python sequences or dictionaries are [constant time], regardless of the size of the data structure.

Q: What is the typical order of growth for a for loop that traverses a sequence?
A: Linear, as long as all operations in the body of the loop are constant time.

C: As a rule of thumb, if the body of a loop is in O(nᵃ) then the whole loop is in [O(nᵃ⁺¹)].

Q: What are the time complexities of indexing and len for strings and tuples?
A: Both are constant time.

Q: What is the time complexity of string concatenation?
A: Linear; the run time depends on the sum of the lengths of the operands.

Q: What is the time complexity of adding an element to the end of a Python list?
A: Constant time on average.

Q: What is the time complexity of removing an element from the end of a Python list?
A: Constant time.

Q: What is the time complexity of sorting a Python list?
A: O(n log n)

C: Most dictionary operations and methods in Python are [constant time].

Q: Why are the dictionary methods keys, values, and items constant time?
A: Because they return iterators. However, looping through the iterators is linear.

Q: What is a search algorithm?
A: An algorithm that takes a collection and a target item and determines whether the target is in the collection, often returning the index of the target.

Q: What is a linear search?
A: A search algorithm that traverses the items of a collection in order, stopping if it finds the target. In the worst case, it has to traverse the entire collection.

Q: What Python operations use linear search?
A: The in operator for sequences and string methods like find and count.

C: A bisection search has time complexity [O(log n)].

Q: What requirement must be met to use bisection search?
A: The elements of the sequence must be in order.

Q: How does bisection search work?
A: It starts with the middle item and checks whether the target comes before or after. Then it searches the appropriate half, cutting the remaining items in half each time.

Q: For a sequence of 1,000,000 items, approximately how many steps does bisection search take?
A: About 20 steps, which is about 50,000 times faster than linear search.

Q: What is a hashtable?
A: A data structure that can perform a search in constant time without requiring items to be sorted.

C: Python dictionaries are implemented using [hashtables].

Q: What two operations must a map data structure implement?
A: add(k, v) to add a key-value pair, and get(k) to look up and return the value for a key.

Q: In the LinearMap implementation, what is the time complexity of the add method?
A: Constant time, because it appends to a list.

Q: In the LinearMap implementation, what is the time complexity of the get method?
A: Linear, because it uses a for loop to search the list.

Q: What does the built-in hash function do?
A: It takes almost any Python object and returns an integer.

Q: What types are unhashable in Python?
A: Mutable types like lists and dictionaries.

Q: How does BetterMap improve on LinearMap?
A: It breaks the list of key-value pairs into 100 smaller LinearMaps, making it about 100 times faster, though still linear.

Q: What is the crucial idea that makes hashtables fast?
A: If you keep the maximum length of the LinearMaps bounded, the get operation becomes constant time. This is done by resizing when items exceed a threshold.

Q: What happens when a HashMap needs to be resized?
A: A new BetterMap is created (twice as big), and all items are rehashed into the new map.

Q: Why is rehashing necessary when resizing a hashtable?
A: Because changing the number of LinearMaps changes the denominator of the modulus operator, so objects need to be redistributed.

C: Although resizing is linear, the HashMap add operation is [constant time] on average because resizing doesn't happen every time.

Q: After n adds where n is a power of two, what is the total cost in units of work?
A: 2n - 2 units, so the average work per add is less than 2 units.

C: When resizing a hashtable, it should grow [geometrically] (multiply by a constant) rather than arithmetically to maintain constant average time.

Q: What happens to average time per add if a hashtable is resized arithmetically?
A: The average time per add becomes linear.

C: [Analysis of algorithms] is a way to compare algorithms in terms of their run time and/or space requirements.

C: A [machine model] is a simplified representation of a computer used to describe algorithms.

C: The [worst case] is the input that makes a given algorithm run slowest or require the most space.

C: In a polynomial, the [leading term] is the term with the highest exponent.

C: The [crossover point] is the problem size where two algorithms require the same run time or space.

C: An [order of growth] is a set of functions that all grow in a way considered equivalent for purposes of analysis of algorithms.

C: [Big-Oh notation] is notation for representing an order of growth; for example, O(n) represents the set of functions that grow linearly.

C: A [linear] algorithm has run time proportional to problem size, at least for large problem sizes.

C: A [quadratic] algorithm has run time proportional to n², where n is a measure of problem size.

C: A [search] is the problem of locating an element of a collection (like a list or dictionary) or determining that it is not present.

C: A [hashtable] is a data structure that represents a collection of key-value pairs and performs search in constant time.
