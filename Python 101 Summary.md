# Mike Driscoll: Python 101 #
2nd Edition, 2020

PEP - Python Enhancement Proposals
PEP Index https://www.python.org/dev/peps/

## Part I - The Basics ##

### 1. Installing Python ###
Most of the time, installing Python is straight-forward and easy to do. It can get tricky when you need to have multiple versions of Python installed on your machine at the same time, but if you are just starting out I think you'll find the installation process pretty painless.

### 2. Python Editors ###
- IDLE
- pyCharm Community Edition
- Visual Studio Code

### 3. Documenting Your Code ###
- Comments using #
- multiline comments using triple single quotes
- docstrings (PEP257) - created using triple double-quotes
- Python Style Guide (PEP8)

#### Tools ####
* pycodestyle (checks if your code follows PEP8) - https://pypi.org/project/pycodestyle/ 
* Pylint (in-depth static code testing tool that finds common issues with code) - https://pylint.org/
  
Python comes with several different ways to document your code. You can use **comments** to explain one or more lines of code. These should be used in moderation and where appropriate. You can also use **docstrings** to document your modules, functions, methods, and classes.  

### 4. Working with Strings ###
You will be using strings very often when you program. A string is a series of letters surrounded by single, double, or triple quotes. Python 3 defines strings as a "Text Sequence Type". You can cast other types to a string using the built-in str() function.

- In Python, backslashes can be used to create escape sequences.
    \b - backspace
    \n - line feed
    \r - ASCII carriage return
    \t - tab
    backslashes can be used to escape quotes
    also you can use single quote to limit strings containing double quotes and vice versa

- String Methods
- String Formatting
  string formatting or string substitution is where you have a string that you would like to insert into another string.
  Python has three different ways to accomplish string formatting:
  a) using the % method
  b) using .format()
  c) using formatted string literals (f-strings)

  ad a)
  print ('My name is %s' % name)
  print ('Hello %s, you must be at least %i to continue!' % (name, age))
  print ('Hello %(first_name)s, you must be at least %(age)i to continue!' % ('first_name': name, 'age': age))

  ad b) 
  print ('Hello {}, you must be at least {} to continue!'.format(name, age))

  ad c) f-strings
  Formatted string literals or f-strings are strings that have an "f" at the beginning and curly braces inside of them that contain expressions, much like the ones you saw in the previous section. These expressions tell the f-string about any special processing that needs to be done to the inserted string, just as justification, float precision, etc.
  The f-string was added in Python 3.6
  ´´´
  name = 'Mike'
  age = 20
  f'Hello {name}, you are {age} years old'
  print (f'My name is {name}\n')

- String Concatenation
  To concatenate strings together, you can use the + sign.

- String Slicing
  Slicing in strings works in much the same way that it does for Python lists.

Python strings are powerful and useful. They can be created using single, double, or triple quotes. Strings are objects, so they have methods. You also learned about string concatenation, string slicing, and three different methods of string formatting.
The newest flavor of string formatting is the f-string. It is also the most powerful and the currently preferred method for formatting strings.

### 5. Numeric Types ###


## Part II - Intermediate Materials ##


## Part III - Tutorials ##


## Part IV - Python Packaging and Distribution ##


