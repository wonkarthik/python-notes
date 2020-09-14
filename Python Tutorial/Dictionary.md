# Dictionary
source: `{{ page.path }}`

Python dictionary is an unordered collection of items. Each item of a dictionary has a key/value pair.Dictionaries are optimized to retrieve values when the key is known.

Creating a dictionary is as simple as placing items inside curly braces {} separated by commas.An item has a key and a corresponding value that is expressed as a pair (key: value).

While the values can be of any data type and can repeat, keys must be of immutable type (string, number or tuple with immutable elements) and must be unique.

![](./images/dict1.PNG)

```tip
1. dict is a collection of "key : value" pairs.
2. dict is represented in {} brackets.
3. dict allows both Homeogenous & Hetrogenous values/elements.
4. dict are mutable.
5. dict doesn't allow duplicate keys but allow values.
6. dict doesn't allow indexing and slicing.
7. dict maintain insertion order
```
```note
1. Creating a Dictionary
2. Accessing a Dictionary
3. Reassigning a dictionary
4. Deleting a Dictionary
5. In-Built function on a Dictionary
6. In-Built Methods on a Dictionary
7. Operations on a Dictionary
8. iterating on a Dictionary
9. Nested Dictionary
```
## Creating a Dictionary
You can create a dictionary by placing a comma-separated list of `key:value` pairs in curly braces `{}`. Each key is separated from its associated value by a colon 
```python
# empty dictionary
my_dict = {}

# dictionary with integer keys
my_dict = {1: 'apple', 2: 'ball'}

# dictionary with mixed keys
my_dict = {'name': 'John', 1: [2, 4, 3]}

# using dict()
my_dict = dict({1:'apple', 2:'ball'})

# from sequence having each item as a pair
my_dict = dict([(1,'apple'), (2,'ball')])

# Declaring one key more than once
my_dict={1:2, 1:3, 1:4, 2:4}

# Python Dictionary Comprehension
my_dict={x*x:x for x in range(8)}

# Create a dictionary with list of zipped keys/values
keys = ['name', 'age', 'job']
values = ['Bob', 25, 'Dev']

print(dict(zip(keys, values)))
# Prints {'name': 'Bob', 'age': 25, 'job': 'Dev'}

# Initialize dictionary with default value '0' for each key
keys = ['a', 'b', 'c']
defaultValue = 0

print(dict.fromkeys(keys,defaultValue))
# Prints {'a': 0, 'b': 0, 'c': 0}
```
## Accessing a Dictionary
The order of key:value pairs is not always the same.

While indexing is used with other data types to access values, a dictionary uses keys. Keys can be used either inside square brackets `[]` or with the `get()` method.

If we use the square brackets [], `KeyError` is raised in case a key is not found in the dictionary. On the other hand, the `get()` method returns None if the key is not found.

```python
# get vs [] for retrieving elements
my_dict = {'name': 'Jack', 'age': 26}

# Output: Jack
print(my_dict['name'])

# Output: 26
print(my_dict.get('age'))

# Trying to access keys which doesn't exist throws error
# Output None
print(my_dict.get('address'))

# KeyError
print(my_dict['address'])

# example 2
D = {'name': 'Bob',
     'age': 25,
     'job': 'Dev'}

print(D['name'])
# Prints Bob

print(D['salary'])
# Triggers KeyError: 'salary'
# When key is present

print(D.get('name'))
# Prints Bob

# When key is absent
print(D.get('salary'))
# Prints None

```
## Reassigning a dictionary

Dictionaries are mutable. We can add new items or change the value of existing items using an assignment operator.

If the key is already present, then the existing value gets updated. In case the key is not present, a new (key: value) pair is added to the dictionary.
```python
# Changing and adding Dictionary Elements
my_dict = {'name': 'Jack', 'age': 26}

# update value
my_dict['age'] = 27

#Output: {'age': 27, 'name': 'Jack'}
print(my_dict)

# add item
my_dict['address'] = 'Downtown'

# Output: {'address': 'Downtown', 'age': 27, 'name': 'Jack'}
print(my_dict)

# Merging two dictionaries
D1 = {'name': 'Bob',
      'age': 25,
      'job': 'Dev'}

D2 = {'age': 30,
      'city': 'New York',
      'email': 'bob@web.com'}

D1.update(D2)
print(D1)
# Prints {'name': 'Bob', 'age': 30, 'job': 'Dev',
#         'city': 'New York', 'email': 'bob@web.com'}
```
## Deleting a Dictionary
There are several ways to remove items from a dictionary.

Remove an Item by Key
If you know the key of the item you want, you can use pop() method. It removes the key and returns its value.
```python
# Removing elements from a dictionary

# create a dictionary
squares = {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# remove a particular item, returns its value
# Output: 16
print(squares.pop(4))

# Output: {1: 1, 2: 4, 3: 9, 5: 25}
print(squares)

# remove an arbitrary item, return (key,value)
# Output: (5, 25)
print(squares.popitem())

# Output: {1: 1, 2: 4, 3: 9}
print(squares)

# remove all items
squares.clear()

# Output: {}
print(squares)

# delete the dictionary itself
del squares

# Throws Error
print(squares)

# example 2
D = {'name': 'Bob',
     'age': 25,
     'job': 'Dev'}

x = D.pop('age')
print(D)                # Prints {'name': 'Bob', 'job': 'Dev'}

# get removed value
print(x)                # Prints 25

del D['age']
print(D)                # Prints {'name': 'Bob', 'job': 'Dev'}

# The popitem() method removes and returns the last inserted item.
x = D.popitem()
print(D)                # Prints {'name': 'Bob', 'age': 25}

# Remove all Items
D.clear()
print(D)                # Prints {}

```
## In-Built function on a Dictionary

Built-in functions like all(), any(), len(), cmp(), sorted(), etc. are commonly used with dictionaries to perform different tasks.

|Function       | Description                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------|
|all()	        | Return True if all keys of the dictionary are True (or if the dictionary is empty).           |
|any()	        | Return True if any key of the dictionary is true. If the dictionary is empty, return False.   |
|len()	        | Return the length (the number of items) in the dictionary.                                    |
|cmp()	        | Compares items of two dictionaries. (Not available in Python 3)                               |
|sorted()	    | Return a new sorted list of keys in the dictionary.                                           |

```python
# Dictionary Built-in Functions
squares = {0: 0, 1: 1, 3: 9, 5: 25, 7: 49, 9: 81}

print(all(squares))         # False

print(any(squares))         # True

print(len(squares))         # 6

print(sorted(squares))      # [0, 1, 3, 5, 7, 9]
```
## In-Built Methods on a Dictionary

|Method	                   | Description                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------|
|clear()	               | Removes all items from the dictionary.                                                                  |
|copy()	                   | Returns a shallow copy of the dictionary.                                                               |
|fromkeys(seq[, v])	       | Returns a new dictionary with keys from seq and value equal to v (defaults to None).                    |
|get(key[,d])	           | Returns the value of the key. If the key does not exist, returns d (defaults to None).                  |
|items()	               | Return a new object of the dictionary's items in (key, value) format.                                   |
|keys()	                   | Returns a new object of the dictionary's keys.                                                          |
|pop(key[,d])	           | Removes the item with the key and returns its value or d if key is not found. If d is not provided and  |
|                          | the key is not found, it raises KeyError.                                                               |
|popitem()	               | Removes and returns an arbitrary item (key, value). Raises KeyError if the dictionary is empty.         |
|setdefault(key[,d])	   | Returns the corresponding value if the key is in the dictionary. If not, inserts the key with a value   |
|                          | of d and returns d (defaults to None).                                                                  |
|update([other])	       | Updates the dictionary with the key/value pairs from other, overwriting existing keys.                  |
|values()	               | Returns a new object of the dictionary's values                                                         |


data = {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
print((data))
print(data.keys())          # dict_keys([0, 1, 2, 3, 4, 5])
print(data.values())        # dict_values([0, 1, 4, 9, 16, 25])
print(data.items())         # dict_items([(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)])
print(data.get(3,0))        # it will give the value of key 3 = 9
                            # if there is no key it return `none`
print(data.clear())         # it clears the dictionary
data1=data.copy()           # 
print(data1)                # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
print(data1.pop(4))         # used to remove and display an item from the dictionary 16
                            # this has no default None value for the second parameter it throw keyerror
print(data1.popitem())      # last inserted item in dictionary (5,25)
print(data.fromkeys({1,2,3,4,7},0)) # {1: 0, 2: 0, 3: 0, 4: 0, 7: 0}
print(data.fromkeys({'1','2','3','4','7'}))  # {'2': None, '4': None, '3': None, '7': None, '1': None}
dict1={1:1,2:2}
dict2={4:5,5:2}
dict1.update(dict2)         # Then it updates the dictionary to hold values from the 
                            # other dictionary that it doesn’t already.
print(dict1)                # {1: 1, 2: 2, 4: 5, 5: 2} 


## Operations on a Dictionary

## iterating on a Dictionary

## Nested Dictionary