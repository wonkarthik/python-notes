# Tuples

source: `{{ page.path }}`

A tuple is an ordered collection of values.
A tuple in Python is similar to a list. The difference between the two is that we cannot change the elements of a tuple once it is assigned whereas we can change the elements of a list.

Tuples are a lot like Tuples:

* Tuples are ordered – Tuples maintains a left-to-right positional ordering among the items they contain.
* Accessed by index – Items in a tuple can be accessed using an index.
* Tuples can contain any sort of object – It can be numbers, strings, Tuples and even other tuples.

except:

* Tuples are immutable – you can’t add, delete, or change items after the tuple is defined.

```tip
# Python Tuples

1. Tuples is a collection of values/elements.
2. Tuples is represented in () brackets.
3. Tuples allows both Homeogenous & Hetrogenous values/elements.
4. Tuples are immutable.
5. Tuples allow duplicate values/elements and insertion order.
6. Tuples allow indexing and slicing.
7. Implication of iterations is comparatively Faster
8. Tuples data type is appropriate for accessing the elements.
9. Tuples consume less memory as compared to the list.
10. Tuples does no have must built-in methods

```

```note

1. Creating a tuple 
2. Accessing a tuple 
3. Slicing a tuple 
4. Deleting a tuple 
5. Reassigning a tuple 
6. Functions on tuples
7. Methods on tuples
8. operations on tuple
9. iterating a tuple
10. nested tuples

```
## Creating a tuple

A tuple is created by placing all the items (elements) inside parentheses (), separated by commas. The parentheses are optional, however, it is a good practice to use them.

A tuple can have any number of items and they may be of different types (integer, float, list, string, 

```
# Different types of tuples

# Empty tuple
my_tuple = ()
print(my_tuple)
#()

# Tuple having integers
my_tuple = (1, 2, 3)
print(my_tuple)
# (1, 2, 3)

# tuple with mixed datatypes
my_tuple = (1, "Hello", 3.4)
print(my_tuple)
# (1, 'Hello', 3.4)

# nested tuple
my_tuple = ("mouse", [8, 4, 6], (1, 2, 3))
print(my_tuple)
# ('mouse', [8, 4, 6], (1, 2, 3))

```
A tuple can also be created without using parentheses. This is known as tuple packing.
```
my_tuple = 3, 4.6, "dog"
print(my_tuple)

# tuple unpacking is also possible
a, b, c = my_tuple

print(a)      # 3
print(b)      # 4.6
print(c)      # dog

my_tuple = ("hello")
print(type(my_tuple))  # <class 'str'>

# Creating a tuple having one element
my_tuple = ("hello",)
print(type(my_tuple))  # <class 'tuple'>

# Parentheses is optional
my_tuple = "hello",
print(type(my_tuple))  # <class 'tuple'>
```
## Slicing a tuple
```
# Positive index 
# Accessing tuple elements using indexing
my_tuple = ('p','e','r','m','i','t')

print(my_tuple[0])   # 'p' 
print(my_tuple[5])   # 't'

# IndexError: list index out of range
# print(my_tuple[6])

# Index must be an integer
# TypeError: list indices must be integers, not float
# my_tuple[2.0]

# nested tuple
n_tuple = ("mouse", [8, 4, 6], (1, 2, 3))

# nested index
print(n_tuple[0][3])       # 's'
print(n_tuple[1][1])       # 4
```
```
# Negative Index

The index of -1 refers to the last item, -2 to the second last item and so on.

# Negative indexing for accessing tuple elements
my_tuple = ('p', 'e', 'r', 'm', 'i', 't')

print(my_tuple[-1])         # t

print(my_tuple[-6])         # p
```
```
# Slicing
# Accessing tuple elements using slicing
my_tuple = ('p','r','o','g','r','a','m','i','z')

# elements 2nd to 4th
print(my_tuple[1:4])            # ('r', 'o', 'g')

# elements beginning to 2nd
print(my_tuple[:-7])            # ('p', 'r')

# elements 8th to end
print(my_tuple[7:])             # ('i', 'z')

# elements beginning to end
print(my_tuple[:])              # ('p', 'r', 'o', 'g', 'r', 'a', 'm', 'i', 'z')

# elements 1st to 7th with step 2
print(my_tuple[1:7:2])      # ('r', 'g', 'a')

# elements till 9th with negative step of -2
print(my_tuple[8::-2])      # ('z', 'm', 'r', 'o', 'p')

# start of 9 element and negative index of -7 with step -3
print(my_tuple[8:-7:-3])    # ('z', 'a')

``` 
## Deleting a tuple 

As we discussed above, a Python tuple is immutable. This also means that you can’t delete just a part of it. You must delete an entire tuple, if you may.
```
percentages=(99,95,90,89,93,96)
del percentages[4]

del percentages[4]
TypeError: 'tuple' object doesn't support item deletion
```

## Reassigning a tuple

```

my_tuple=(1,2,3,[4,5])
my_tuple[2]=6

File “<pyshell#43>”, line 1, in <module>

# Set and print the initial tuple
weekenddays = ("Saturday", "Sunday")  # "Saturday", "Sunday

# Reassign and print
weekenddays = ("Sat", "Sun")       # ('Sat', 'Sun')

Although you can't change tuple items, you can change list items within a tuple. Here's an example of doing that:

# Assign the tuple
t = (101, 202, ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]) 
print(t)             # (101, 202, ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'])

# Update the third list item
t[2][2] = "Humpday"
print(t)             # (101, 202, ['Monday', 'Tuesday', 'Humpday', 'Thursday', 'Friday'])

```
## Functions on tuples

Python also has a set of built-in functions that you can use with tuple objects.

|Method	        |Description                                                   |
|---------------|--------------------------------------------------------------|
|all()	        | Returns True if all Tuple items are true                     |
|any()	        | Returns True if any Tuple item is true                       |
|enumerate()	| Takes a Tuple and returns an enumerate object                |
|len()	        | Returns the number of items in the Tuple                     |
|Tuple()	    | Converts an iterable (tuple, string, set etc.) to a Tuple    |
|max()	        | Returns the largest item of the Tuple                        |
|min()	        | Returns the smallest item of the Tuple                       |
|sorted()	    | Returns a sorted Tuple                                       |
|sum()	        | Sums items of the Tuple                                      |

```
tuple = (0,1,2,3,4,5,6,5)

print(len(tuple))                # 8
print(max(tuple))                # 6
print(min(tuple))                # 0
print(sum(tuple))                # 26
print(sorted(tuple))             # [0, 1, 2, 3, 4, 5, 5, 6]
# print(tuple("Hockey"))         # error "Hockey" string not found
print(any(['','','']))           # False
print(any(['','0','0','','']))   # True
#It returns True if all items in the tuple have a True value
print(all(['','','']))           # False
print(all(['1','2','1']))        # True
print(enumerate(tuple))          # <enumerate object at 0x0000022EE875DC40>

```

## Methods in Tuple

Python has a set of built-in methods that you can call on tuple objects.

|Method	         | Description                                                            |
|----------------|------------------------------------------------------------------------|
|count()	     | Returns the count of specified item in the tuple                       |
|index()	     | Returns the index of first instance of the specified item              |

```
tuple = (1,2,3,2,4,5,2)

print(tuple.index(2))  # 1
# As you can see, we have 2s at indices 1, 3, and 6. But it returns only the first index.

print(tuple.count(2))  # 3 
# This method takes one argument and returns the number of times an item appears in the tuple.
```
## operations


|Operator	        |Description	                                                               |Example                              |
|-------------------|------------------------------------------------------------------------------|-------------------------------------|
| + Concatenation	|Returns a Tuple containing all the elements of the first and the second Tuple.| >>> L1=[1,2,3]                      |
|                   |                                                                              | >>> L2=[4,5,6]                      |
|                   |                                                                              | >>> L1+L2                           |
|                   |                                                                              | >>> L2+(7,)                         |
|                   |                                                                              | >>> (4,5,6,7)                       |   
|                   |                                                                              | [1, 2, 3, 4, 5, 6]                  |
| * Repetition	    |Concatenates multiple copies of the same Tuple.                               | >>> L1*4                            |
|                   |                                                                              | [1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3]|
|                   |                                                                              |                                     |
| [] slice	        |Returns the item at the given index. A negative index counts the position     |>>> L1=[1, 2, 3, 4, 5, 6]            |
|                   | from the right side.	                                                       |>>> L1[3]                            |
|                   |                                                                              | 4                                   |
|                   |                                                                              | >>> L1[-2]                          |
|                   |                                                                              | 5                                   |
|                   |                                                                              |                                     |
| [ : ]             | Range slice	Fetches items in the range specified by the two index operands | >>> L1=[1, 2, 3, 4, 5, 6]           |
|                   | separated by : symbol.                                                       | >>> L1[1:4]                         |
|                   | If the first operand is omitted, the range starts from the zero index. If the| [2, 3, 4]                           |
|                   | second operand is omitted, the range goes up to the end of the Tuple.	       | >>> L1[3:]                          |
|                   |                                                                              | [4, 5, 6]                           |
|                   |                                                                              | >>> L1[:3]                          |
|                   |                                                                              | [1, 2, 3]                           |  
| in                | Returns true if an item exists in the given Tuple.	                       | >>> L1=[1, 2, 3, 4, 5, 6]           |
|                   |                                                                              | >>> 4 in L1                         |
|                   |                                                                              | True                                |
|                   |                                                                              | >>> 10 in L1                        |
|                   |                                                                              | False                               |
| not in            | Returns true if an item does not exist in the given Tuple.	               | >>> L1=[1, 2, 3, 4, 5, 6]           |
|                   |                                                                              | >>> 5 not in L1                     |
|                   |                                                                              | False                               |
|                   |                                                                              | >>> 10 not in L1                    |
|                   |                                                                              | True                                |


## iterating Tuples

We can use a for loop to iterate through each item in a tuple
```
for i in (1,3,2):
    print(i)            # (1,3,2)

We can use a for loop to iterate through each item in a tuple.

# Using a for loop to iterate through a tuple
for name in ('John', 'Kate'):
    print("Hello", name)  

Hello John
Hello Kate    

```

## Nested tuples

```
tuple=((1,2,3),(4,(5,6)))
Suppose we want to access the item 6. For that, since we use indices, we write the following code.

tuple([1][1][1])
6

```

