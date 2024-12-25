# Hands-On Data Structures and Algorithms with Python Notes

📕 Title: Hands-On Data Structures and Algorithms with Python

👨‍💻 Authors: Dr. Basant Agarwal

📚 Publisher: Packt

#️⃣ Edition: 3rd Edition

💾 Topics: Python, Data Structures and Algorithms

📄 Pages: 497

## 📝 Table of Contents

- Ch1. Python Data Types and Structures
- Ch2. Introduction to Algorithm Design
- Ch3. Algorithm Design Techniques and Strategies
- Ch4. Linked Lists
- Ch5. Stacks and Queues
- Ch6. Trees
- Ch7. Heaps and Priority Queues
- Ch8. Hash Tables
- Ch9. Graphs and Algorithms
- Ch10. Searching
- Ch11. Sorting
- Ch12. Selection Algorithms
- Ch13. String Matching Algorithms

## 🛠️ Resources

[Book Page](https://www.packtpub.com/product/hands-on-data-structures-and-algorithms-with-python-third-edition/9781801073448)

[Github Repo](https://github.com/PacktPublishing/Hands-On-Data-Structures-and-Algorithms-with-Python-Third-Edition)

## Ch1. Python Data Types and Structures

[Python Docs Reference](https://docs.python.org/3/reference/index.html)
[Python Docs Tutorial](https://docs.python.org/3/tutorial/index.html)

Main built-in types:

- Numeric types: Integer (int), float, complex
- Boolean types: bool
- Sequence types: String (str), range, list, tuple
- Mapping types: dictionary (dict)
- Set types: set, frozenset

Integers like 45, 1000 or -25.

Floats are accurate up to 15 decimal points.

Complex numbers, which include a real and an imaginary part. Example: 3 + 4j.

Boolean provides a value of either True or False. Any non-zero value is truthy, zero is falsy.

```python
print(bool(0))
print(bool(False))
print(bool("Hi"))
```

Sequence data types are used to store multiple values in a single variable in an organized and efficient way. There are four basic sequence types: string, range, lists, and tuples.

A string is an immutable sequence of characters represented in single, double, or triple quotes.

The string type in Python is called str.

The + operator concatenates strings

The _ operator can be used to create multiple copies of a string. When it is applied with an integer (n, let’s say) and a string, the _ operator returns a string consisting of n concatenated copies of the string. For example:

```python
st = 'data.'
print(st * 3)
print(3 * st)
```

Output:

```
data.data.data.
data.data.data.
```

Range: The range data type represents an immutable sequence of numbers. Mainly used in for and while loops.

Ex: `range(start, stop, step)`

```python
print(list(range(10)))data.data.data.
print(list(range(1,10,2)))
print(list(range(20,10,-2)))
```

Output:

```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[1, 3, 5, 7, 9]
[20, 18, 16, 14, 12]
```

Lists: Python lists are used to store multiple items in a single variable. Duplicate values are allowed in
a list, and elements can be of different types.

```python
a = ['food', 'bus', 'apple', 'queen']
print(a)
mylist = [10, "India", "world", 8]
# accessing elements in list.
print(mylist[1])
```

Output:

```
['food', 'bus', 'apple', 'queen']
India
```

- List elements can be accessed by its index
- List elements are ordered and dynamic
- The list data structure is mutable, whereas most of the other data types, such as integer and float are immutable
- A list can contain any arbitrary objects
- Several operators and builtin functions can also be applied in lists, such as in, not in, concatenation (+), and replication (`*`) operators. Moreover, other built-in functions, such as len(), min(), and max(), are also available.

Membership, identity, and logical operations

Membership operators: Membership means we wish to test if a given value is stored in the sequence.

Two common ones in Python are `in` and `not in`.

```python
val = 104
mylist = [100, 210, 430, 840, 108]
if val not in mylist:
		print("Value is NOT present in mylist")
else:
		print("Value is present in mylist")
```

Output:

```
Value is NOT present in mylist
```

Identity operators: Identity operators are used to compare objects. The different types of identity operators are `is`and `is not`.

```python
Firstlist = []
Secondlist = []
if Firstlist == Secondlist:
		print("Both are equal")
else:
		print("Both are not equal")

if Firstlist is Secondlist:
		print("Both variables are pointing to the same object")
else:
		print("Both variables are not pointing to the same object")

thirdList = Firstlist

if thirdList is Secondlist:
		print("Both are pointing to the same object")
else:
		print("Both are not pointing to the same object")
```

Output:

```
Both are equal
Both variables are not pointing to the same object
Both are not pointing to the same object
```

Logical operators

These operators are used to combine conditional statements (True or False). There are three types of logical operators: `AND`, `OR`, and `NOT`.

Tuples

Tuples are used to store multiple items in a single variable. It is a read-only collection where data is ordered (zero-based indexing) and unchangeable/immutable. Tuples are used instead of lists when we wish to store the data that should not be changed in the program.

```python
tuple_name = ("entry1", "entry2", "entry3")
my_tuple = ("Shyam", 23, True, "male")
```

Tuples in Python support zero-based indexing, negative indexing, and slicing.

### Complex data types: dictionaries, sets and frozensets

Dictionaries

A dictionary is also a collection of objects. Stores data in unordered key-value pairs. _A key must be of a hashable and immutable data type, and value can be any arbitrary Python object._

In this context,an object is hashable if it has a hash value that does not change during its lifetime in the program.

Items in the dictionary are enclosed in curly braces, {}, separated by a comma:

```python
dict = {
		<key>: <value>,
		<key>: <value>,
		<key>: <value>
}
```

Keys in dictionaries are case-sensitive, they should be unique, and cannot be duplicated; however, the values in the dictionary can be duplicated.

Values in a dictionary can be fetched based on the key. For example: `my_dict['1']`.

A dictionary differs from lists in the sense that dictionary elements can be accessed using keys, whereas the list elements are accessed via indexing.

Some methods on dictionaries:

```python
print('name' in person)
print('fname' not in person)
print(len(person))

mydict.clear() # removes all elements from a dict
mydict.get(<key>) # Returns the correspoding value, if not found returns None
mydict.items() # Returns a list of the items in key value pairs
mydict.keys()
mydict.values()
mydict.pop(<key>) # Removes the key-value and returns the value
mydict.popitem() # Removes the last key value added and returns it as a tuple
mydict.update(<obj>) # Merges one dict into another
```

Sets

A set is an unordered collection of hashable objects. It is iterable, mutable, and has unique elements. The order of the elements is also not defined. While the addition and removal of items are allowed, the items themselves within the set must be immutable and hashable. Sets support membership testing operators (in, not in), and operations such as intersection, union, difference, and symmetric difference.

They are created by using the built-in set() function or curly braces {}.

```python
x1 = set(['and', 'python', 'data', 'structure'])
x2 = {'and', 'python', 'data', 'structure'}
```

It is important to note that sets are unordered data structures, and the order of items in sets is not preserved.

Sets are generally used to perform mathematical operations, such as intersection, union, difference, and complement. The len() method gives the number of items in a set, and the in and not in operators can be used in sets to test for membership.

```python
x = {'data', 'structure', 'and', 'python'}
print(len(x))
print('structure' in x)
```

Union operation returns the two sets merged, repeated items are discarded
Intersection operation returns only the item that is repeated
Difference returns all the elements that are in set1 but not in set2
Symmetric difference returns all elements that are in set1 or set2 but not both
You can test wheter a set is a subset of another with `.issubset()` and the `<=` operator.

Immutable sets

In Python, `frozenset` is another built-in type data structure, which is, in all respects, exactly like a set, except that it is immutable, and so cannot be changed after creation.

```python
x = frozenset(['data', 'structure', 'and', 'python'])
```

You cannot create a set of sets, because the elements of a set must be immutable, but you can create a set of frozensets.

```python
a11 = set(['data'])
a21 = set(['structure'])
a31 = set(['python'])
x1 = {a11, a21, a31}
```

Output:

```
TypeError: unhashable type: 'set'
```

### Python’s collections module

Let's go over modules, packages and scripts.

A module is a Python script with the .py extension that contains a collection of functions, classes, and variables. A package is a directory that contains collections of modules. it has an `__init__.py` file, which lets the interpreter know that it is a package.

Data types and operations of the collections module

- namedtuple
- deque
- defaultdict
- ChainMap
- Counter
- UserDict UserList
- UserString

### Ch2. Introduction to Algorithm Design

### Ch3. Algorithm Design Techniques and Strategies

### Ch4. Linked Lists

### Ch5. Stacks and Queues

### Ch6. Trees

### Ch7. Heaps and Priority Queues

### Ch8. Hash Tables

### Ch9. Graphs and Algorithms

### Ch10. Searching

### Ch11. Sorting

### Ch12. Selection Algorithms

### Ch13. String Matching Algorithms
