# Python Intermediate #
based on: https://www.youtube.com/watch?v=HGOBQPFzWKo
by Patrick Loeber
Python Engineer: https://www.youtube.com/channel/UCbXgNpp0jedKWcQiULLbDTA

## Lists ##

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

## Tuples ##
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

## Dictionaries ##
