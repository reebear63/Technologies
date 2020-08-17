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
- for loop
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

### String Handling ###
