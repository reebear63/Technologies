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

## 06. Collections ##

## 07. Itertools ##

## 08. Lambda Functions ##

## 09. Exceptions and Errors ##

## 10. Logging ##

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


