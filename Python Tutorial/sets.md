# Sets

source: `{{ page.path }}`

A set object contains one or more items, not necessarily of the same type, which are separated by comma and enclosed in curly brackets {}.

Python set is an unordered collection of unique items. They are commonly used for computing mathematical operations such as union, intersection, difference, and symmetric difference.

```tip
1. sets is a collection of values/elements.
2. sets is represented in {} brackets.
3. sets allows both Homeogenous & Hetrogenous values/elements.
4. sets are mutable.
5. sets doesn't allow duplicate values/elements.
6. sets doesn't allow indexing and slicing.
7. sets doesnot maintain insertion order
```
```note
1. Creating a set
2. Accessing a set
3. Deleting a set
4. Operation on sets
5. The Frozenset
6. Updating a set
7. Functions on sets
8. Methods on sets
9. iterating on sets
```


## Create and Accessing a Set
You can create a set by placing a comma-separated sequence of items in curly braces {}.
```
# A set of strings
S = {'red', 'green', 'blue'}

# A set of mixed datatypes
S = {1, 'abc', 1.23, (3+4j), True}
Sets don’t allow duplicates. They are automatically removed during the creation of a set.

S = {'red', 'green', 'blue', 'red'}
print(S)
# Prints {'blue', 'green', 'red'}

You can also create a set using a type constructor called set().

# Set of items in an iterable
S = set('abc')
print(S)
# Prints {'a', 'b', 'c'}

# Set of successive integers
S = set(range(0, 4))
print(S)
# Prints {0, 1, 2, 3}

# Convert list into set
S = set([1, 2, 3])
print(S)
# Prints {1, 2, 3}

```
## Deleting a set 

```python
numbers={3,2,1,4,6,5}

1. `discard()` : This method takes the item to delete as an argument.

numbers.discard(3)
print(numbers)
{1, 2, 4, 5, 6}

As you can see in the resulting set, the item 3 has been removed.

2. `remove()`

Like the discard() method, remove() deletes an item from the set.

numbers.remove(5)
print(numbers)
{1, 2, 4, 6}

`discard() vs remove()`-

These two methods may appear the same to you, but there’s actually a difference. If you try deleting an item that doesn’t exist in the set, discard() ignores it, but remove() raises a KeyError.

numbers.discard(7)
print(numbers)
{1, 2, 4, 6}

print(numbers.remove(7))
Traceback (most recent call last):

File “<pyshell#37>”, line 1, in <module>
numbers.remove(7)
KeyError: 7

3. `pop()`

Like on a dictionary, you can call the pop() method on a set. However, here, it does not take an argument. Because 
a set doesn’t support indexing, there is absolutely no way to pass an index to the pop method. Hence, it pops out an 
arbitrary item. Furthermore, it prints out the item that was popped.

numbers.pop()
1

Let’s try popping anot/her element.
numbers.pop()
2

Let’s try it on another set as well.
{2,1,3}.pop()
1

4. `clear()`

Like the pop method(), the clear() method for a dictionary can be applied to a Python set as well. It empties the 
set in Python.

print(numbers.clear())

```

```python
## Updating a set
Python set is mutable. But as we have seen earlier, we can’t use indices to reassign it.

numbers={3,1,2,4,6,5}
numbers[3]

File “<pyshell#56>”, line 1, in <module>
numbers[3]
TypeError: ‘set’ object does not support indexing

So, we use two methods for this purpose- add() and update(). We have seen the update()
method on tuples, lists, and strings.

```

```javascript
numbers={3,1,2,4,6,5}

1 . `add()`  If you add an existing item in the set, the set remains unaffected.

print(numbers.add(3.5))
{1, 2, 3, 4, 5, 6, 3.5}

2. `update()` This method can add multiple items to the set at once, which it takes as arguments.

print(numbers.update([7,8],{1,2,9}))
{1, 2, 3, 4, 5, 6, 3.5, 7, 8, 9}

```

## set operations

|Method	                            |Description                                                                |
|-----------------------------------|---------------------------------------------------------------------------|
|union()	                        | Return a new set containing the union of two or more sets                 |
|update()	                        | Modify this set with the union of this set and other sets                 |
|intersection()	                    | Returns a new set which is the intersection of two or more sets           |
|intersection_update()	            | Removes the items from this set that are not present in other sets        |
|difference()	                    | Returns a new set containing the difference between two or more sets      |
|difference_update()	            | Removes the items from this set that are also included in another set     |
|symmetric_difference()	            | Returns a new set with the symmetric differences of two or more sets      |
|symmetric_difference_update()	    | Modify this set with the symmetric difference of this set and other set   |
|isdisjoint()	                    | Determines whether or not two sets have any elements in common            |
|issubset()	                        | Determines whether one set is a subset of the other                       |
|issuperset()	                    | Determines whether one set is a superset of the other                     |


A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

#### Set Union
Union of A and B is a set of all elements from both sets.You can perform union on two or more sets using union() method or  |  operator.

![](./images/union.PNG)

```python
# by operator
print(A | B)                         # {1, 2, 3, 4, 5, 6, 7, 8}
# by method
print(A.union(B))                    # {1, 2, 3, 4, 5, 6, 7, 8}
```

#### Set Intersection
Intersection of A and B is a set of elements that are common in both the sets.
Intersection is performed using & operator. Same can be accomplished using the intersection() method.
![](./images/intersection.PNG)

```python
# by operator
print(A & B)                         # {4, 5}
# by method
print(A.intersection(B))             # {4, 5}
```
#### Set Difference
Difference of the set B from set A(A - B) is a set of elements that are only in A but not in B. Similarly, 
B - A is a set of elements in B but not in A.

Difference is performed using - operator. Same can be accomplished using the difference() method

![](./images/difference.PNG)

```python
# by operator
print(A - B)                         # {1, 2, 3}
# by method
print(A.difference(B))               # {1, 2, 3}
```
#### Symmetric Difference :
Symmetric Difference of A and B is a set of elements in A and B but not in both (excluding the intersection).
Symmetric difference is performed using ^ operator. Same can be accomplished using the method symmetric_difference().

![](./images/assymetricdifference.PNG)

```python
# by operator
print(A ^ B)                         # {1, 2, 3, 6, 7, 8}   
# by method  
print(A.symmetric_difference(B))     # {1, 2, 3, 6, 7, 8}

```

#### Set intersection_update()

The intersection of two or more sets is the set of elements which are common to all sets.

A.intersection_update(*other_sets)

This method returns None (meaning it does not have a return value). It only updates the set calling the intersection_update() method.

For example:

result = A.intersection_update(B, C)

result will be None
A will be equal to the intersection of A, B, and C
B remains unchanged
C remains unchanged
```python
A = {1, 2, 3, 4}
B = {2, 3, 4, 5, 6}
C = {4, 5, 6, 9, 10}

result = A.intersection_update(B)

print('result =', result)           # result = None
print('A =', A)                     # A = {2,3,4}
print('B =', B)                     # B = {2,3,4,5}

intersection_update() with Two Parameters

result = C.intersection_update(B, A)

print('result =', result)           # result = None
print('C =', C)                     # C = {4}
print('B =', B)                     # B = {2, 3, 4, 5, 6}
print('A =', A)                     # A = {1, 2, 3, 4}
```
#### Set difference_update()

If A and B are two sets. The set difference of A and B is a set of elements that exists only in set A but not in B
```python
A.difference_update(B)
Here, A and B are two sets. difference_update() updates set A with the set difference of A-B.

A = {1, 2, 3, 4}
B = {2, 3, 4, 5, 6}
C = {4, 5, 6, 9, 10}

result = A.difference_update(B)
print('result =', result)           # result = None
print('A =', A)                     # A = {1}
print('B =', B)                     # B = {2, 3, 4, 5, 6}

print(C.difference_update(B, A))            # none
print('A =',A)                              # A = {1, 2, 3, 4}
print('B =',B)                              # B = {2, 3, 4, 5, 6}
print('C =',C)                              # C = {9, 10}
```

#### Set symmetric_difference_update()
The symmetric difference of two sets A and B is the set of elements that are in either A or B, but not in their intersection.
```python
A = {1, 2, 3, 4}
B = {2, 3, 4, 5, 6}
C = {4, 5, 6, 9, 10}

result = A.symmetric_difference_update(B)
print('result =', result)           # result = None
print('A =', A)                     # A = {1, 5, 6}
print('B =', B)                     # B = {2, 3, 4, 5, 6}

Here, the set A is updated with the symmetric difference of set A and B. However, the set B is unchanged.

result = C.symmetric_difference_update(B)
print("result = ", result)                  # result = none
print('A =',A)                              # A = {1, 2, 3, 4}
print('B =',B)                              # B = {2, 3, 4, 5, 6}
print('C =',C)                              # C = {9, 10}

"Note :" Multiple argument are not possible
```
#### isdisjoint()	
Two sets are said to be disjoint sets if they have no common elements.
```python
A = {1, 5, 9, 0}
B = {2, 4, -5}
Here A and B are disjoint sets.

A = {1, 2, 3, 4}
B = {5, 6, 7}
C = {4, 5, 6}

print('Are A and B disjoint?', A.isdisjoint(B))  # Are A and B disjoint? True
print('Are A and C disjoint?', A.isdisjoint(C))  # Are A and C disjoint? False

A = {'a', 'b', 'c', 'd'}
B = ['b', 'e', 'f']
C = '5de4'
D ={1 : 'a', 2 : 'b'}
E ={'a' : 1, 'b' : 2}

print('Are A and B disjoint?', A.isdisjoint(B))   # Are A and B disjoint? False
print('Are A and C disjoint?', A.isdisjoint(C))   # Are A and C disjoint? False
print('Are A and D disjoint?', A.isdisjoint(D))   # Are A and D disjoint? True
print('Are A and E disjoint?', A.isdisjoint(E))   # Are A and E disjoint? False

```
#### issubset()	
Determines whether one set is a subset of the other

Set A is said to be the subset of set B if all elements of A are in B
```python
Syntax: A.issubset(B)

A = {1, 2, 3}
B = {1, 2, 3, 4, 5}
C = {1, 2, 4, 5}

print(A.issubset(B))                # Returns True

# B is not subset of A
print(B.issubset(A))                # Returns False

print(A.issubset(C))                # Returns False

print(C.issubset(B))                # Returns True

```
#### issuperset
Determines whether one set is a superset of the other

Set X is said to be the superset of set Y if all elements of Y are in X
```python
A = {1, 2, 3, 4, 5}
B = {1, 2, 3}
C = {1, 2, 3}

Set A is said to be the subset of set B if all elements of B are in A

`Syntax: A.issuperset(B)`

print(A.issuperset(B))      # Returns True
print(B.issuperset(A))      # Returns False
print(C.issuperset(B))      # Returns True

x = { 2, 4, 6, 8 }
y = { 2, 8 }
f1 = x.issuperset(y) # f1 = True
f2 = y.issuperset(x) # f2 = False

```
## Python Frozenset
Python provides another built-in type called a frozenset. Frozenset is just like set, only immutable (unchangeable).

You can create a frozenset using frozenset() method. It freezes the given sequence and makes it unchangeable.
```python
S = frozenset({'red', 'green', 'blue'})
print(S)
# Prints frozenset({'green', 'red', 'blue'})

As frozensets are unchangeable, you can perform non-modifying operations on them

# finding size
S = frozenset({'red', 'green', 'blue'})
print(len(S))
# Prints 3

# performing union
S = frozenset({'red', 'green', 'blue'})
print(S | {'yellow'})
# Prints frozenset({'blue', 'green', 'yellow', 'red'})
```
methods that attempt to modify a frozenset will raise error.
```python
# removing an item
S = frozenset({'red', 'green', 'blue'})
S.pop()
# Triggers AttributeError: 'frozenset' object has no attribute 'pop'

# adding an item
S = frozenset({'red', 'green', 'blue'})
S.add('yellow')
# Triggers AttributeError: 'frozenset' object has no attribute 'add'

Unlike sets, frozensets are unchangeable so they can be used as keys to a dictionary.

For example, D = {frozenset(['dev','mgr']):'Bob'}

```