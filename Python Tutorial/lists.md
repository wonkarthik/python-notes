
# lists
source: `{{ page.path }}`

A list is a sequence of values (similar to an array in other programming languages but more versatile)

The values in a list are called items or sometimes elements.

The important properties of Python lists are as follows:

* Lists are ordered – Lists remember the order of items inserted.
* Accessed by index – Items in a list can be accessed using an index.
* Lists can contain any sort of object – It can be numbers, strings, tuples and even other lists.
* Lists are changeable (mutable) – You can change a list in-place, add new items, and delete or update existing items.

```tip
# Python Lists

1. Lists is a collection of values/elements.
2. list is represented in [] brackets.
3. list allows both Homeogenous & Hetrogenous values/elements.
4. Lists are mutable.
5. list allow duplicate values/elements.
6. lists allow indexing and slicing.
7. Implication of iterations is Time-consuming.
8. The list is better for performing operations, such as insertion and deletion.
9. Lists consume more memory.
10. Lists have several built-in methods

```
Python List Tutorial.

```note
## Lists operations

1.  Creating Lists                                                               
2.  Accessing Lists                                                               
3.  Slicing Lists                                                                 
4.  Reassigning Lists                                                             
5.  Deleting Lists                                                                
6.  Multidimension Lists                                                          
7.  Concatenation Lists                                                           
8.  Operation Lists                                                               
9.  Iterable Lists                                                                
10. Lists Comprehension                                                           
11. `Built-in Functions :`  min,max,sum,len,all,any,list,sorted                     
12. `Built-in Methods   :`  append,insert,remove,pop,index,clear,reverse,count,sort 

```
##  Creating a list

To create a list in Python, simply add any number of comma separated values between square brackets. Like this
```
colors = ['red','green','blue']

planets = [ "Earth", "Mars", "Saturn", "Jupiter" ]

```
##  Accessing a list 

```
List indexing
my_list = ['p', 'r', 'o', 'b', 'e']
print(my_list[0])

# Nested List
n_list = ["Happy", [2, 0, 1, 5]] # nested list
print(n_list[0][1]) # nested indexing

```
##  slicing list
```
list = [1,2,3,5,4]
print(list[2:4])    # 3,5,4 
print(list[3:])     # 5,4
print(list[:3])     # 1,2,3
print (list[3:-1])  # 5
print (list[3:-2])  # []
print(list[:-2])    # 123
print(list[1:-2])   # 23
print(list[-2:-1])  # 5
print(list[-3:-5])  # []

l1= [10,20,30,40,50]
print(l1[1:-2]) # 20,30
print(l1[2:-2]) # 30
print(l1[1:-2]) # 20,30

```
```note
a[start:stop]  # items start through stop-1
a[start:]      # items start through the rest of the array
a[:stop]       # items from the beginning through stop-1
a[:]           # a copy of the whole array

slicing
a[start:stop:step] # start through not past stop, by step

a[-1]    # last item in the array
a[-2:]   # last two items in the array
a[:-2]   # everything except the last two items

a[::-1]    # all items in the array, reversed
a[1::-1]   # the first two items, reversed
a[:-3:-1]  # the last two items, reversed
a[-3::-1]  # everything except the last two items, reversed

Both +ve and -ve index no are move in -> direction
in +ve index start values is greater than stop values of the list  then it will be empty
in -ve index start value is greater than stop value of the list then it will be empty ex: [ -5,-6]  
```
```
syntax = [start:stop]

l2= [10,20,30,40,50,60,70]
print(l2[1:-2])     # 20 -50
print(l2[2:-5])     # []
print(l2[2:-4])     # 30
print(l2[3:-3])     # 40
print(l2[1:-3])     # 20-40
print(l2[-7:-3])    # 10-40
print(l2[-6:4])     # 20-40
print(l2[:-3])      # 10-40
print(l2[-3:])      # 50-70


[start : stop : steps]  

`Step increment : ` 
a = [1, 2, 3, 4, 5, 6, 7, 8]
print(a[1:4])       # [2,3,4]
print(a[1:4:2])     # [2,4]
print(a[::2])       # [1,3,5,7]
print(a[::3])       # [1,4,7]
print(a[::-1])      # [8,7,6,5,4,3,2,1]
print(a[::-2])      # [8,6,4,2]
print(a[1:-2:2])    # [2,4,6]
```

## Re-assigning multiple elements
```
list=["caramel","gold","silver","occur"]

# reassign full list
print(list)
list=["red","green","blue","orange"]
print(list)

# reassign few elements 
list=["caramel","gold","silver","occur","bauxite"]
list[2:]=["bronze","zinc"]
print(list)
# ['caramel', 'gold', 'bronze', 'zinc']

list=["caramel","gold","helim","silver","occur","bauxite"]
list[:2]=["bronze","zinc"]
print(list)
# ['bronze', 'zinc', 'helim', 'silver', 'occur', 'bauxite']

list=["caramel","gold","silver","occur"]
list[2:3]=["bronze","copper"]
print(list)
# ['caramel', 'gold', 'bronze', 'copper', 'occur']

list=["caramel","gold","silver","occur","zinc","bauxite"]
list[0:5:2]=["bronze","copper","platinum"]
print(list)
# ['bronze', 'gold', 'copper', 'occur', 'platinum', 'bauxite']

Reassigning a single element
list=["caramel","gold","silver","occur"]
list[3]="platinum"
print(list) 
# ['caramel', 'gold', 'silver', 'platinum']

here we can't add the new element it throw error we need to reassign whole list

```
## deleting multiple elements

list=["caramel","gold","silver","occur"]
del list
print(list)

list=["caramel","gold","silver","occur","Bauxite"]
del list[2:5]
print(list)     # ['caramel', 'gold']
del list[2:]
print(list)     # ['caramel', 'gold']
del list[:2]
print(list)     # ['silver', 'occur', 'Bauxite']

delete single element
list=["caramel","gold","silver","occur"]
del list[1]
print(list)     # ['caramel', 'silver', 'occur']

## Multidimensional list in python
```
grocery_list=[['caramel','P&B','Jelly'],['onions','potatoes'],['flour','oil']
print(grocery_list[0][0])
# caramel

a=[[[1,2],[3,4],5],[6,7]]
test=a[0][1][1]
# 4

```
## Concatenation of python list

```
`1. Concatenation Operator(+)`
a,b,c=[3,1,2],[5,4,6],[7,8]
print(a+b+c)                  # [3,1,2,5,4,6,7,8]

`2. loops : `
list1=[1,2,3]
list2=[8,4,5]

for list in list2:
    list1.append(list)
print(list1)                   # [1,2,3,8,4,5]

list1=[1,2,3,4]
list2=[5,6,7,8]
list3=[9,10,11,12]
result= []
for x in list1:
    result.append(x)
for y in list2:
    result.append(y)
for z in list3:
    result.append(z)    
print(result)                   # [1,2,3,4,5,6,7,8,9,10,11,12]

`3. Comprehensions : `

list1=[1,2,3,4]  
list2=[5,6,7,8]
list3=[9,10,11,12]

result = [element for lis in [list1, list2] for element in lis]
print(result)                   # [1,2,3,4,5,6,7,8]

result1 = [ element for list in [list1,list2,list3] for element in list]
print(result1)                   # [1,2,3,4,5,6,7,8,9,10,11,12]           

result2 = [element for lis in [list1] for element in lis]
print(result2)                  # [1,2,3,5]    
even=[2*i for i in range(1,11)]
print(even)                     # [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

list1=[1,2,3]
list2=[4,5,6]
CombLst=[(x,y) for x in list1 for y in list2]
print(CombLst)              

# [1,2,3,4,5,6]

list = [x for x in range(21) if x%2==0]
print(list)             

# [0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

obj=["Even" if i%2==0 else "Odd" for i in range(10)]
print(obj)                           

# ['Even', 'Odd', 'Even', 'Odd', 'Even', 'Odd', 'Even', 'Odd', 'Even', 'Odd']

squares = [x*x for x in range(11)]
print(squares)                      

# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

mylist=['Dave','Micheal','Harry','Jon']
k= []
for x in mylist:
    if(len(x)>4):
        k.append(x.upper())
    else:
        k.append(x.lower())
print(k)
             
`4. * Operator (Unpacking)`
list1=[1,2,3,4]  
list2=[5,6,7,8]
list3=[9,10,11,12]
print([*list1,*list2,*list3])   

# [1,2,3,4,5,6,7,8,9,10,11,12]

`5. extend() Built-in Method`
list1=[1,2,3,4]  
list2=[5,6,7,8]
list3=[9,10,11,12]

concatenating lists using extend() method
list1.extend(list2)
list1.extend(list3)
print(list1)           

# [1,2,3,4,5,6,7,8,9,10,11,12]
```

## Python List operations
```
multiplications
a=[1,2,3]
a*=3 
print(a)                # [1, 2, 3, 1, 2, 3, 1, 2, 3]
```

# Built -in list functions

|Method	        |Description                                                  |
|---------------|-------------------------------------------------------------|
|all()	        | Returns True if all list items are true                     |
|any()	        | Returns True if any list item is true                       |
|enumerate()	| Takes a list and returns an enumerate object                |
|len()	        | Returns the number of items in the list                     |
|list()	        | Converts an iterable (tuple, string, set etc.) to a list    |
|max()	        | Returns the largest item of the list                        |
|min()	        | Returns the smallest item of the list                       |
|sorted()	    | Returns a sorted list                                       |
|sum()	        | Sums items of the list                                      |

```

list = [0,1,2,3,4,5,6,5] 
print(len(list))                # 8
print(max(list))                # 6
print(min(list))                # 0
print(sum(list))                # 26
print(sorted(list))             # [0, 1, 2, 3, 4, 5, 5, 6]
print(list("Hockey"))           # error "Hokey" string not found
print(any(['','','']))          # False
print(any(['','0','0','','']))  # True
#It returns True if all items in the list have a True value
print(all(['','','']))          # False
print(all(['1','2','1']))       # True

```

## Buit in methods 


|Method	         | Description                                                          |
|----------------|----------------------------------------------------------------------|
|append()	     | Adds an item to the end of the list                                  |
|insert()	     | Inserts an item at a given position                                  |
|extend()	     | Extends the list by appending all the items from the iterable        |
|remove()	     | Removes first instance of the specified item                         |
|pop()	         | Removes the item at the given position in the list                   |
|clear()	     | Removes all items from the list                                      |
|copy()	         | Returns a shallow copy of the list                                   |
|count()	     | Returns the count of specified item in the list                      |
|index()	     | Returns the index of first instance of the specified item            |
|reverse()	     | Reverses the items of the list in place                              |
|sort()	         | Sorts the items of the list in place                                 |

```
list = [2,8,3,4]
print(list.append(5))       # it adds an item to end of the list
print(list.insert(3,5))     # it insert an item at specified position after element 3
print(list.remove(2))       # removes the 2 element from the list 
print(list.pop(3))          # here 3 is the index value it removes the element in specified index and display values
print(list.clear())         # it empties the list

list1 = [ 1,3,5,3,8,9]
print(list1.index(3))       # it returns index no search for first matching index no of the items
print(list1.count(3))       # it return count value of 3 in the list of elements
print(list1.sort())         # it sorts the list in ascending order 
print(list1.reverse())      # Prints the list in reverse order

print(list("Hockey"))       # ['H', 'o', 'c', 'k', 'e', 'y']
print(list("Hockey","bold"))
```