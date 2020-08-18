# Basics of Python Scripting Language #

## Introduction ##

### History ###
- Python is a simple, easy to learn, powerful, high-level and object-oriented programming language
- dynamic typing
- multipurpose programming language
- can easily integrate with C, C++, Java, etc.
- started by Guido van Rossum at CWI in the Netherlands (CWI = Centrum Wiskunde & Informatica)
- predecessor: ABC programming language, capable of exception handling, interfacing with the Amoeba Operating System
- influenced by: ABC and Modula-3

**Amoeba**
Amoeba is a distributed operating system developed by Andrew S. Tanenbaum and others at the Vrije Universiteit Amsterdam. The aim of the Amoeba project was to build a timesharing system that makes an entire network of computers appear to the user as a single machine. Development at the Vrije Universiteit was stopped: the source code of the latest version (5.3) was last modified on 30 July 1996.
The Python programming language was originally developed for this platform.

**ABC**
ABC is an imperative general-purpose programming language and programming environment developed at CWI, Netherlands by Leo Geurts, Lambert Meertens, and Steven Pemberton. It is interactive, structured, high-level, and intended to be used instead of BASIC, Pascal, or AWK. It is not meant to be a systems-programming language but is intended for teaching and prototyping.
The language had a major influence on the design of the Python programming language; Guido van Rossum, who developed Python, previously worked for several years on the ABC system in the mid 1980s.

**Minix**
Andrew S. Tanenbaum created MINIX at Vrije Universiteit in Amsterdam to exemplify the principles conveyed in his textbook, "Operating Systems: Design and Implementation" (1987). Early versions of Minix were created by Tanenbaum for educational purposes. Starting with MINIX 3, the primary aim of development shifted from education to the creation of a highly reliable and self-healing microkernel OS. Minix is now developed as open-source software.
Linus Torvalds used and appreciated Minix, but his design deviated from the Minix architecture in significant ways, most notably by employing a monolithic kernel instead of a microkernel. This was disapproved of by Tanenbaum in the "Tanenbaum-Torvalds debate". Tanenbaum explained again his rational for using a microkernel in May 2006.

### Variables ###
- Variable is the name of a memory location where data is stored.
- identifiers are the names given to the fundamental building blocks in a program
- these can be variables, classes, objects, functions, lists, directories, etc.
- there are certain rules for naming identifiers
  - an identifier is a sequence of characters and numbers
  - no special characters except underscore (_) are allowed
  - a keyword shall not be used as an identifier name
  - Python is case-sensitive
  - the first character of an identifier can be a letter or an underscore, but not a digit

**Literals**
- Literals can be defined as data that is stored in a variable or constant
- multi-line String - a piece of text that is spread along multiple lines
  - adding a backslash at the end of each line
  - using triple quotation marks
- Numeric literals are immutable and can be of four different numerical types: int, long, float, complex
- Boolean literals: True or False
- Special literals: None
- Literal Collections: tuples, lists, and dictionaries
  - Lists contain items of different data types
    - values stored in lists are separated by commas and enclosed within square brackets []
    - values can be retrieved using the slice operator ([] and [:])
    - the plus sign is the concatenation and asterisk the repetition operator
    - lists item count starts at 0

**Operators**
- Arithmetic (+, -, *, /, %, **)
- Relational (<, >, <=, >=, ==, !=, <>)
- Assignment (=, /=, +=, -=, *=, %=, **=)
- Logical (and, or, not)
- Membership (in, not in)
- Identity (is, is not)

### Comments ###
# single lined comment
''' this is
    a multi-line
    comment '''

### Constructs ###
**if statement**
a = 10
if a == 10:
    do something
print "hello world"
- if statement
- if else statement
- nested if else statement

**Iterations**
- for loop: range (start, end, step)
    for x in range(4,10, 2):
      print(x)

    for c in "welcome":
      print(c)

    list1 = ["apple", "banana", "papaya"]
    for fruit in list1:
      print(fruit)
- nested for loop
- while loop
- break: the break statement is a jump statement used to pass the control to the end of the loop
- continue: used to skip the current iteration and forces the next loop iteration
- pass: ???

### Functions ###
- a function is a block of code
- there are two types of functions
  - built-in functions
  - user-defined functions

* Defining a function
* Calling a function
* Function Arguments
  * Default Arguments
    a default argument provides a default value to a parameter which is not provided in the function call
* Anonymous Functions
  - functions which are not bound to a name
  - created using the keyword "lambda"
  - takes any number of arguments and returns an evaluated expression
  - created without the def keyword
* Variable scopes
  The scope of a variable can be determined by the part in which it is declared.
  - local variables
    - declared inside a function body
    - cannot be accessed outside the function scope
  - global variables
    - defined outside all functions
    - can be accessed across all functions and in the main program

**Samples**
def simplemethod():
  print("called simple method)

simplemethod()
----------------------------------------------
def add(a,b):
  return a+b

res = add(2, 4)
print (res)
----------------------------------------------

### String Handling ###
- strings are text enclosed in single or double quotes
- Python treats single and double quotes the same
- Characters in strings can be accessed either from the front (forward indexing: 0, 1, 2, ...) or the back (backward indexing: -1, -2, ...) by using []
- String Operators
  - basic: '+' and '*'
  - membership: 'in' and 'not in'
  - relational: <, >, <=, >=, ==, !=, <>
  - string comparison is based on ASCII or Unicode order
- String slicing
  - a String slice can be defined as a substring: str[0:6], str[:6], str[3:]
- String Handling functions
  - capitalize()
  - count(string)
  - endswith(string)
  - find(string)
  - index(string)
  - isalnum()
  - isalpha()
  - isdigit()
  - islower()
  - isupper()
  - isspace()
  - len(string)
  - lower()
  - upper()
  - startswith(string)
  - swapcase()
  - lstrip() - strip characters from left
  - rstrip() - strip characters from right, space is default

### Collections ###

**Lists**
- lists are a data structure capable of holding different types of data
- lists are mutable, i.e. Python will not create a new list if we modify an element in the list
- lists are containers which hold other objects in a given order
- a Python list is enclosed between square [] brackets
- elements are stored with a starting index of 0
- lists can be created by putting the values inside square brackets and separated by commas
- replcating / repeating lists can be performed by using the '*' operator and specifying a number of times:
      list1 = [10,20]
      print (list1 * 2)
- list slicing: a part of a list (slice) can be retrieved based on an index
- updating elements in a list: to update or change the value of a list item, assign a new value to that list index
- the append() method is used to add a new element to the end of the list
- deleting an element from a list: the del statement can be used to delete one item or a slice of items from a list - del list1[0:3]
- min(list): minimum value in list
- max(list)
- len(list)
- cmp(list)
- index(object)
- count(object): number of times an object occurs in a list
- pop() / pop(int)
- insert(index, object)
- extend(sequence): extends a list with the given sequence
- remove(object)
- reverse()
- sort()

**Tuples**
- a tuple is a sequence of immutable objects, therefore a tuple cannot be changed
- objects are enclosed within parentheses and separated by commas
- tuples are similar to lists - difference is that lists have mutable objects whereas tuples have immutable objects

- processing of tuples are faster than lists
- stored data is safe as tuple objects are immutable and therefore cannot be changed
- tuples are used for string formatting

- tuples can also be nested
- tuples are accessed in the same way as lists
- adding tuples: using the concatenation operator '+'
- replicating tuples: using '*'
- tuple slicing
- min(tuple)
- max(tuple)
- len(tuple)
- cmp(tuple1, tuple2)
- tuple(sequence)

**Dictionary**


### Object Oriented Programming ###

* Object
  all functions have a built-in attribute __doc__, which returns the doc string defined in the function's source code

* Class
  a class is a logical entity that has some specific attributes and methods

* Method
  a method is a function that is associated with an object

* Inheritance
  Inheritance means that an object acquires all properties and behaviors (methods) of a parent class

* Polymorphism
  Polymorphism means "many forms" or "many shapes"; one task can be performed in different ways

* Encapsulation
  restricts access to methods and variables; code and data are wrapped together within a single unit

* Data Abstraction
  Abstraction is used to hide internal implementation details and exposes only functionalities   

* Constructor
  A constructor is a special type of method that is used to instantiate an object based on the definition found in the class. Constructors are normally used to initialize to instance variables.
  * A constructor is a class function that begins with a double underscore (__); the name of the constructor is always __init__()
  * When creating an object, a constructor can accept arguments
  * every class must have a constructor, even if it simply relies on the default constructor


### Control Structures ###

## More Interesting Topics ##
- Jupyter Notebooks
- 
