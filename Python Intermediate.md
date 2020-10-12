# Python Intermediate #
based on: https://www.youtube.com/watch?v=HGOBQPFzWKo
by Patrick Loeber  
Python Engineer: https://www.youtube.com/channel/UCbXgNpp0jedKWcQiULLbDTA

## 01. Lists ##

mylist = ["banana", "cherry", "apple"]  
print (mylist)

- a list can also contain different data types
- index starts at 0, so mylist[0] produces a "banana"
- a negative index will start counting at the end, e.g. mylist[-1] will give an "apple"
- iterate over list items  
    for fruit in mylist:  
        print(fruit)
- check whether item is in list  
    if "banana" in mylist:  
        print ("yes")  
    else:  
        print ("no")
- how many items are in my list  
    print(len(mylist))
- mylist.append ("lemon") will add a "lemon" at the end of the list 
- insert an item at a specific position   
    mylist.insert(1, "pineapple")  
    print (mylist)
- remove an item from the end of the list   
    item = mylist.pop()
- remove a specific element  
    item = mylist.remove("cherry")
- remove all elements from a list  
    item = mylist.clear()
- reverse the list  
    item = mylist.reverse()
- sort the list   
    item = mylist.sort()        # sorts in-place  
    new_list = sorted(mylist)   # assigns a sorted list to a new list
- initialize lists  
    mylist = [0] * 5        # creates a list with five zeros
- concatenate lists  
    mylist3 = mylist + mylist2
- slicing  
    mylist = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]  
    a = mylist[1:5]         # creates a = [2, 3, 4]  
    a = mylist[2:]          # goes from given index to the end  
    a = mylist[::2]         # takes every second item  
    b = a[::-1]             # reverses list
- copy a list  
    mylist_org = ["banana", "cherry", "apple"]  
    mylist_cpy = list_org  
    mylist_cpy.append ("lemon")     # modifies both copied and original list, since both refer to the same memory location  
    mylist_cpy = list_org.copy()    # real copy  
    mylist_cpy = list(list_org)     # using the list function  
    mylist_cpy = list_org[:]        # real copy thru slicing  
- list comprehension  
    mylist = [1, 2, 3, 4, 5, 6]  
    mylist_sq = [x*x for x in mylist]  
    print (mylist)  
    print (mylist_sq)

## 02. Tuples ##
- collection data type that is ordered and immutable, allows duplicate elements
- uses parentheses   
    my_tuple = ("Max", 28, "Boston")  
    my_tuple = ("Max")               # not a tuple, but a string  
    my_tuple = ("Max",)              # this is a tuple
- indexes start at 0 as well
- negative index also counts from the end
- tuple items cannot be modified = immutable
- iteration over tuple elements: in
- check whether item is in tuple, same as with lists
- number of elements  
    my_tuple = ('a', 'p', 'p', 'l', 'e')  
    print (len(my_tuple))  
    print (my_tuple.count('p'))     # returns 2  
    print (my_tuple.count('o'))     # returns 0 - not in tuple  
    print (my_tuple.index('l'))     # returns 3 - first occurance of 'l'  
- convert tuple to list and vice versa  
    my_list = list(my_tuple)  
    my_tuple2 = tuple (my_list)
- slicing - same as list
- unpacking a tuple  
    my_tuple = ("Max", 28, "Boston")  
    name, age, city = my_tuple  
  number of elements in tuple have to match the variables on the left
- unpack multiple items using an asterisk  
    my_tuple = (0, 1, 2, 3, 4)  
    i1, *i2, i3 = my_tuple  
    print (i1)          # 0 = first item  
    print (i3)          # 4 = very last item  
    print (i2)          # [1, 2, 3] as a list  
- more effective storage of tuples vs lists  
    import sys  
    mylist = [0, 1, 2, "hello", True]           # both list and tuple have the same elements  
    mytuple = (1, 2, "hello", True)  
    print(sys.getsizeof(mylist), " bytes")      # returns 104 bytes  
    print(sys.getsizeof(mytuple), " bytes")     # returns  88 bytes  
  a list is larger than a tuple although it has the same elements
- list manipulation is more time consuming than working with tuples  
    import timeit  
    print (timeit.timeit(stmt="[0, 1, 2, 3, 4, 5]", number=1000000))  
    print (timeit.timeit(stmt="(0, 1, 2, 3, 4, 5)", number=1000000))  

## 03. Dictionaries ##
key-value pair, unordered, mutable (= add or change information)  
  
    mydict = {"name": "Max", "age": 28, "city": "New York"}  
    mydict2 = dict (name="Mary", age=27, city="Boston")         # no quotes for the keys  
    value = mydict["name"]  
    mydict["email"] = "max@xyz.com"  
    del mydict["name"]  
    mydict.popitem()                    # deletes the last item of the dictionary  
    if "name" in mydict:  
        print(mydict["name"])           # check and print item  
    #----------------------------------  
    try:  
        print(mydict["name"])  
    except:  
        print("Error")  
    #----------------------------------
    for key in mydict.keys():           # iterate over keys, values or both  
        print(key)  
    for value in mydict.values():  
        print(value)  
    for key, value in mydict.items():  
        print(key,value)  
    #----------------------------------  
    mydict_cpy = mydict                 # both dictionaries point to the same memory location  
    mydict_cpy = mydict.copy()          # create real copy  
    mydict_cpy = dict(mydict)  
    #----------------------------------  
    mydict = {"name": "Max", "age": 28, "email": "max@xyz.com"}  
    mydict2 = dict(name="Mary", age=27, city="Boston")  
    mydict.update(my_dict2)             # all pre-existing key-value pairs were overwritten, new added  
    #----------------------------------  
    ```
- any immutable data type can be used as a key  
  
    my_dict = {3: 9, 6: 36, 9: 81}  
    value = my_dict[3]                  # unfortunate choice, since confusion is bound to happen  
    print(value)                        # will return 9  
- tuples are possible as keys, but not lists (since it can be changed after its creation)    

## 04. Sets ##
selection data type, unordered, mutable, no duplicate elements  

    myset = {1, 2, 3}
    myset = {1, 2, 3, 1, 2}             # each element is only kept once
    myset = set("Hello")                # {'o', 'l', 'H', 'e'} -> only one 'l', arbitrary order
    myset = {}          # will result in an empty dictionary!
    myset = set()       # empty set
    #----------------------------------
    myset.add(1)
    myset.add(2)
    myset.add(3)
    myset.discard(3)
    myset.clear()
    myset.pop()
    for x in myset:
        print(x)
    if 1 in myset: 
        print("yes")            # if the element is not in the set, no exception is thrown
    #----------------------------------
    odds = {1, 3, 5, 7, 9}
    evens= {0, 2, 4, 6, 8}
    primes = {2, 3, 4, 7}

    u = odds.union(evens)
    i = odds.intersection(primes)
    #----------------------------------
    setA = {1, 2, 3, 4, 5, 6, 7, 8, 9}
    setb = {1, 2, 3, 10, 11, 12}

    diff = setA.difference(setB)
    print(diff)                 # {4, 5, 6, 7, 8, 9} = elements which are in setA, but not in setB

    diff2 = setB.symmetric_difference(setA)
    print(diff2)                # returns all elements that are in either set, but not in both

    setA = {1, 2, 3, 4, 5, 6}
    setb = {1, 2, 3}
    print(setA.issubset(setB))  # all elements of setA have to be in setB to yield True
    print(setB.issuperset(setA))
    print(setA.isdisjoint(setB))    # yields True if both elements do not have elements in common

    setA = {1, 2, 3, 4, 5, 6}
    setB = setA                 # setB will point to the same location as setA
    setB = setA.copy()          # these two will create "real" copies
    setB = set(setA)
    a = frozenset([1, 2, 3, 4]) # cannot change after creation

## 05. Strings ##
ordered and immutable data type used for text representation
-- insert Strings section from Python 101 here --

    my_string = """Hello \
    World"""                    # continue in new line, but do not insert CR-LF

    my_string = "Hello World"
    substring = my_string[::2]  # takes only every second character
    substring = my_string[::-1] # reverts the string
    print (substring)

    greeting = "Hello"
    name = "Tom"
    if 'el' in greeting: 
        print("yes")

    my_string = "Hello World"
    print (my_string.endswith("ld"))
    print (my_string.find('pp'))
    print (my_string.replace('World', 'Universe'))

    my_string = 'How are you doing'
    my_list = my_string.split()     # default delimiter is space
    my_list = my_string.split(",")
    print(my_list)          

    new_string = ''.join(my_list)
    print (new_string)

    my_list = ['a'] * 6
    print(my_list)

    # bad 
    my_string = ''
    for i in my_list:
        my_string += i              # since strings are immutable, this will always create new strings
    print(my_string)

    # good
    my_string = ''.join(my_list)
    print(my_string)

## 06. Collections ##
collections: Counter, namedtuple, OrderedDict, defaultdict, deque

    from collections import Counter
    a = "aaaaabbbbccc"
    my_counter = Counter(a)
    print(my_counter)

    Counter({'a': 5, 'b': 4, 'c': 3})

    my_counter.items()                  # all key-value pairs
    my_counter.keys()                   #
    my_counter.values()                 #  dicr_values([5, 4, 3])

    print(my_counter.most_common(1))    # print most common element as a list of tuples: [('a', 5)]
    print(my_counter.most_common(2))    # [('a', 5), ('b', 4)]
    #----------------------------------

    from collections import namedtuple
    Point = namedtuple('Point', 'x,y')
    pt = Point(1, -4)
    print(pt)

    >>Point(x=1, y=-4)

    print(pt.x, pt.y)
    #----------------------------------

    from collection import OrderedDict  # not necessary anymore since Python 3.7
    ordered_dict = OrderedDict()
    ordered_dict['a'] = 1
    ordered_dict['b'] = 2
    ordered_dict['c'] = 3
    ordered_dict['d'] = 4
    #----------------------------------
    
    from collections import defaultdict # dictionary will have a default value
    d = defaultdict(int)    # using a normal dictionary, it will raise a key error
    d['a'] = 1
    d['b'] = 2
    print(d['b'])
    print(d['c'])           # default value of int is 0

    #----------------------------------
    # deque = double-ended queue
    from collections import deque
    d = deque()
    d.append(1)
    d.append(2)
    print(d)
    d.appendleft(3)
    print(d)                    # deque([3, 1, 2])
    d.pop()
    d.popleft()
    d.clear()
    d.extend([4, 5, 6])
    d.extendleft([4, 5, 6])     #  deque([6, 5, 4, 3, 1, 2])  
        
## 07. Itertools ##
itertools: product, permutations, combinations, accumulate, groupby, infinite iterators

    from itertools import product
    a = [1, 2]
    b = [3, 4]
    prod = product(a,b)
    print (list(prod))          # [(1, 3), (1, 4), (2, 3), (2, 4)]
    
    prod = product(a, b, repeat=2)
    #----------------------------------

    from itertools import permutations
    # will return all possible orderings
    perm = permutations(a, 2)   # max. length of orderings
    #----------------------------------

    from itertools import combinations
    # will create all possible combinations with a specified length
    a = [1, 2, 3, 4]
    comb = combinations(a, 2)   # no combinations of the same argument, no repetition
    print(list(comb))           # [(1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4)]  

    from itertools import combinations_with_replacement
    #----------------------------------

    from itertools import accumulate
    a = [1, 2, 3, 4]
    acc = accumulate(a)         # by default, create the sums

    from itertools import accumulate
    import operator
    a = [1, 2, 3, 4]
    acc = accumulate(a, func=operator.mul)

    from itertools import accumulate
    import operator
    a = [1, 2, 5, 3, 4]
    acc = accumulate(a, func=max)
    print(a)                    # [1, 2, 5, 3, 4]
    print(list(acc))            # [1, 2, 5, 5, 5]

    #----------------------------------
    from itertools import groupby

    def smaller_than_3(x):
        return x < 3

    a = [1, 2, 3, 4]
    group_obj = groupby(a, key=smaller_than_3)
    for key, value in group_obj         # True  [1, 2]
        print(key, list(value))         # False [3, 4]
    #----------------------------------
    from itertools import groupby
    a = [1, 2, 3, 4]
    group_obj = groupby(a, key=lambda x: x<3)
    for key, value in group_obj:
        print(key, list(value))
    #----------------------------------
    from itertools import groupby

    persons = [{'name': 'Tim', 'age': 25}, {'name': 'Dan', 'age': 25}, {'name': 'Lisa', 'age': 27}, {'name': 'Claire', 'age': 28}]
    group_obj = groupby(persons, key=lambda x: x['age'])
    for key, value in group_obj:
        print(key, list(value))

    OUTPUT
    25 [{'name': 'Tim', 'age': 25}, {'name': 'Dan', 'age': 25}]
    27 [{'name': 'Lisa', 'age': 27}]
    28 [{'name': 'Claire', 'age': 28}]
    #----------------------------------
    from itertools import count, cycle, repeat

    for i in count(10):
        print(i)            # will start infinite count from 10

    a = [1, 2, 3]
    for i in cycle(a):
        print(i)            # cycle indefinitely through a

    a = [1, 2, 3]
    for i in repeat(1):
        print(i)

    for i in repeat(1, 4):
        print(i)            # repeat over 1 - 4 times

## 08. Lambda Functions ##
lambdas are small, one-line functions with parameter(s)

    lambda arguments: expression

    add10 = lambda x: x+10
    print(add10(5))

    mult = lambda x,y: x*y
    #----------------------------------
    points2D = [(1, 2), (15, 1), (5, -1), (10, 4)]
    points2D_sortedX = sorted(points2D)
    points2D_sortedY = sorted(points2D, key=lambda x: x[1])

    print(points2D)
    print(points2D_sortedX)         # sorted by x value
    print(points2D_sortedY)         # sorted by y value
    #----------------------------------
    # map(func, seq)
    a = [1, 2, 3, 4, 5]
    b = map(lambda x: x*2, a)
    print(list(b))                  # each element got multiplied by 2

    c = [x*2 for x in a]            # list comprehension
    print(c)
    #----------------------------------
    # filter(func, seq)
    a = [1, 2, 3, 4, 5, 6]
    b = filter(lambda x: x%2==0, a)
    print(list(b))                  # only get the even numbers

    c = [x for x in a if x%2==0]    # list comprehension
    print(c)
    #----------------------------------
    # reduce(func, seq)
    from functools import reduce
    a = [1, 2, 3, 4]
    product_a = reduce(lambda x,y: x*y, a)
    print(product_a)                # result: 24


## 09. Exceptions and Errors ##
A syntax error occurs when the parser detects a syntactical incorrect expression.

Errors
- TypeError
- ModuleNotFoundError
- NameError (name is not defined)
- FileNotFoundError (e.g. 'No such file or directory')
- ValueError (e.g. 'x not in list')
- IndexError (e.g. list index out of range)
- KeyError (e.g. key is not inside the dictionary)
- ZeroDivisionError

Exceptions
- Raising your own exceptions
    x = -5
    if x < 0:
        raise Exception('x should be positive')

- Assertion -> an expection is raised if the assertion is not True
    x = -5
    assert (x>= 0), 'x is not positive'
    >>>Assertion Error

- Handling exceptions
    try:
        a = 5 / 0
    except:
        print('an error happened')
    # program will continue here

    try:
        a = 5 / 0
    except Exception as e:
        print(e)
    # exception message will be printed

- it is good practise to catch the exception which is raised
    try:
        a = 5 / 1           # a = 5 / 0
        b = a + 4           # b = a + '10'
    except ZeroDivisionError as e:
        print(e)
    except TypeError as e:
        print(e)
    else:
        print('everything is fine')
    finally:
        print('cleaning up...')         # is run no matter whether there is an exception or not

- creating your own error classes as a subclass derived from the Exception baseclass
    class ValueTooHighError(Exception):
        pass

    class ValueTooSmallError(Exception):
        def __init__(self, message, value)
            self.message = message
            self.value = value

    def test_value(x):
        if x > 100:
            raise ValueTooHighError('value is too high')
        if x < 5:
            raise ValueTooSmallError('value is too small', x)

    try:
        test_value(200)
    except ValueTooHighError as e:
        print(e)
    except ValueTooSmallError as e:
        print(e.message, e.value)
    #----------------------------------

## 10. Logging ##
- import logging
- Log levels: debug, info, warning, error, critical
  ```
  import logging  
  ### using logrecord attributes - https://docs.python.org/3/library/logging.html#logrecord-attributes
  logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(name)s - %(levelname)s - %(message)s', datefmt='%m/%d/%Y %H:%M%S')
  logging.debug('This is a debug message')
  logging.info('This is an info message') 
  logging.warning('This is a warning message')  
  logging.error('This is an error message')  
  logging.critical('This is a critical message')

Use a helper module - best practice
    import logging
    
    logger = logging.getLogger(__name__)
    logger.info('hello from helper')
    #----------------------------------

    import logging

    logger = logging.getLogger(__name__)

    # create handler
    stream_h = logging.StreamHandler()
    file_h = logging.FileHandler('file.log')

    # level and format
    stream_h.setLevel(logging.WARNING)
    file_h.setLevel(logging.ERROR)

    formatter = logging.Formatter('%(name)s - %(levelnames - %(message)s')
    stream_h.setFormatter(formatter)
    file_h.setFormatter(formatter)

    logger.addHandler(stream_h)
    logger.addhandler(file_h)

    logger.warning('this is a warning')
    logger.error('this is an error')
    #----------------------------------

    import logging
    import logging.config

    logging.config.fileConfig('logging.conf')

    logger = logging.getLogger('simpleExample')
    logger.debug('this is a debug message')

Capturing Stack Traces
    import logging

    try:
        a = [1,2,3]
        val = a[4]

    except IndexError as e:
        logging.error(e. exc_info=True)
    #----------------------------------

    import logging
    import traceback

    try:   
        a = [1,2,3]
        val = a[4]
    except: 
        logging.error("The error is %s", traceback.format_exc())

Rotating log files
    import logging
    from logging.handlers import RotatingFileHandler

    logger = logging.getLogger(__name__)
    logger.setLevel(logging.INFO)

    # roll over after 2 KB, and keep backup logs app.log.1, app.log.2, etc.
    handler = RotatingFileHandler('app.log', maxBytes=2000, backupCount=5)
    logger.addHandler(handler)

    # underscore means that we do not care about a variable
    for _ in range(10000):
        logger.info('Hello, world!')

    Rotating based on Date/Time
    import logging
    import time
    from logging.handlers import TimedRotatingFileHandler
   
    logger = logging.getLogger(__name__)
    logger.setLevel(logging.INFO)

    # s, m, h, d, midnight, w0 (weekday, w0=Monday)
    handler = TimedRotatingFileHandler('timed_test.log', when='s', interval=5, backupCount=5)
    logger.addHandler(handler)

    # underscore means that we do not care about a variable
    for _ in range(10):
        logger.info('Hello, world!')
        time.sleep(5)

    The log files get named automatically including the time and date

Python-JSON-Logger
    https://github.com/madzak/python-json-logger

02:42:49
## 11. JSON ##

## 12. Random Numbers ##

## 13. Decorators ##

## 14. Generators ##

## 15. Threading vs Multiprocessing ##

## 16. Multithreading ##

## 17. Multiprocessing ##

## 18. Function Arguments ##

## 19. The Asterisk (*) Operator ##

## 20. Shallow vs Deep Copying ##

## 21. Context Managers ##


