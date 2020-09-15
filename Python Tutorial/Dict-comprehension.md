# Dict comprehension

source: `{{ page.path }}`

`Dictionary comprehension` is a way to build a new dictionary by applying an expression to each item in an iterable.
Dictionaries are data types in Python which allows us to store data in key/value pair. For example:
```python
D = {}
for x in range(5):
    D[x] = x**2

print(D)        # Prints {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```
General syntax for a dictionary comprehension is:

![](./images/dict2.PNG)
![](./images/dict3.PNG)

```python
D = {c: c*3 for c in "RED"}
print(D)                        # {'R': 'RRR', 'E': 'EEE', 'D': 'DDD'}

L = ['ReD', 'GrEeN', 'BlUe']
D = {c.lower(): c.upper() for c in L}
print(D)                        # Prints {'blue': 'BLUE', 'green': 'GREEN', 'red': 'RED'}
```
#### Extracting a Subset of a Dictionary
Sometimes you want to extract particular keys from a dictionary. This is easily accomplished using a dictionary comprehension.
```python
D = {0:'A', 1:'B', 3:'C', 4:'D', 5:'E'}
keys = [0,3,5]
x = {k: D[k] for k in keys}
print(x)                        # {0: 'A', 3: 'C', 5: 'E'}
```
#### Filter Dictionary Contents
Suppose you want to make a new dictionary with selected keys removed. Here’s a simple code that deletes specified keys from a dictionary.
```python
D = {0:'A', 1:'B', 3:'C', 4:'D', 5:'E'}
remove = [0,3,5]
x = {k: D[k] for k in D.keys() - remove}
print(x)                        # {1: 'B', 4: 'D'}               
```
#### Invert Mapping / Reverse lookup
Given a dictionary d and a key k, it is easy to find the corresponding value v = d[k]. This operation is called a lookup.

But what if you want to retrieve a key k using a value v in a dictionary? You have to do `reverse lookup`. 
```python
D = {0: 'red', 1: 'green', 2: 'blue'}
R = {v: k for k,v in D.items()}
print(R)                        # Prints {'red': 0, 'green': 1, 'blue': 2}
```

#### Dictionary Comprehension with Enumerate
Sometimes you want to create a dictionary from the list with list index number as key and list element as value. To achieve this wrap the list in `enumerate()` function and pass it as an iterable to the dict comprehension.
```python
L = ['red', 'green', 'blue']
D = {k:v for k,v in enumerate(L)}
print(D)                        # Prints {0: 'red', 1: 'green', 2: 'blue'}

Such dictionaries with element index are often useful in a variety of scenarios such as reading a file by lines.

D = {ix: line for ix, line in enumerate(open('myFile.txt'))}
print(D)
# {0: 'First line\n',
#  1: 'Second line\n',
#  2: 'Third line\n'}
```
#### Initialize Dictionary with Comprehension
Dictionary comprehensions are also useful for initializing dictionaries from keys lists, in much the same way as the `fromkeys()` method. Following example Initializes a dictionary with default value ‘0’ for each key.
```python
keys = ['red', 'green', 'blue']

# using dict comprehension
D = {k: 0 for k in keys}
print(D)                        # Prints {'red': 0, 'green': 0, 'blue': 0}

# equivalent to using fromkeys() method
D = dict.fromkeys(keys, 0)
print(D)                        # Prints {'red': 0, 'green': 0, 'blue': 0}
```
A standard way to dynamically initialize a dictionary is to combine its keys and values with `zip`, and pass the result to the `dict()` function. However, you can achieve the same result with a dictionary comprehension.
```python
keys = ['name', 'age', 'job']
values = ['Bob', 25, 'Dev']

# using dict comprehension
D = {k: v for (k, v) in zip(keys, values)}
print(D)                        # Prints {'name': 'Bob', 'age': 25, 'job': 'Dev'}

# equivalent to using dict() on zipped keys/values
D = dict(zip(keys, values))
print(D)                        # Prints {'name': 'Bob', 'age': 25, 'job': 'Dev'}
```
#### Dictionary Comprehension with if Clause
A dictionary comprehension may have an optional associated if clause to filter items out of the result.

Iterable’s items are skipped for which the if clause is not true.
```tip
        { key:value for var in iterable if_clause }
```
The following example collects squares of even items (i.e. items having no remainder for division by 2) in a range.
```python

D = {x: x**2 for x in range(6) if x % 2 == 0}

print(D)                        # Prints {0: 0, 2: 4, 4: 16}

This dictionary comprehension is the same as a for loop that contains an if statement:

D = {}
for x in range(5):
    if x % 2 == 0:
        D[x] = x**2

print(D)                         # Prints {0: 0, 2: 4, 4: 16}
```        
#### Nested Dictionary Comprehension
The initial value in a dictionary comprehension can be any expression, including another dictionary comprehension.
```tip
        { key: {dict comprehension} for var in iterable } 
```
For example, here’s a simple list comprehension that uses a nested for clause.
```python
D = {(k,v): k+v for k in range(2) for v in range(2)}
print(D)                        # Prints {(0, 1): 1, (1, 0): 1, (0, 0): 0, (1, 1): 2}

# is equivalent to
D = {}
for k in range(2):
    for v in range(2):
        D[(k,v)] = k+v
print(D)                        # Prints {(0, 1): 1, (1, 0): 1, (0, 0): 0, (1, 1): 2}
```

#### dictionary comprehension example
```python
square_dict = {num: num*num for num in range(1, 11)}
print(square_dict)

{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100}

```
In both programs, we have created a dictionary square_dict with number-square key/value pair.

However, using dictionary comprehension allowed us to create a dictionary in a single line.

`Syntax: dictionary = {key: value for vars in iterable}`

```python
# item price in dollars

old_price = {'milk': 1.02, 'coffee': 2.5, 'bread': 2.5}

dollar_to_pound = 0.76
new_price = {item: value*dollar_to_pound for (item, value) in old_price.items()}
print(new_price)                   

{'milk': 0.7752, 'coffee': 1.9, 'bread': 1.9}

```        
####  Conditionals in Dictionary Comprehension
We can further customize dictionary comprehension by adding conditions to it. Let's look at an example.
```python
##  If Conditional Dictionary Comprehension
original_dict = {'jack': 38, 'michael': 48, 'guido': 57, 'john': 33}

even_dict = {k: v for (k, v) in original_dict.items() if v % 2 == 0}
print(even_dict)

{'jack': 38, 'michael': 48}

```
```python
## Multiple if Conditional Dictionary Comprehension
original_dict = {'jack': 38, 'michael': 48, 'guido': 57, 'john': 33}

new_dict = {k: v for (k, v) in original_dict.items() if v % 2 != 0 if v < 40}
print(new_dict)

{'john': 33}
```
```python
## if-else Conditional Dictionary Comprehension
original_dict = {'jack': 38, 'michael': 48, 'guido': 57, 'john': 33}

new_dict_1 = {k: ('old' if v > 40 else 'young')
    for (k, v) in original_dict.items()}
print(new_dict_1)

{'jack': 'young', 'michael': 'old', 'guido': 'old', 'john': 'young'}
```
####  Nested Dictionary Comprehension
We can add dictionary comprehensions to dictionary comprehensions themselves to create nested dictionaries. Let's look at an example.
```python
## Nested Dictionary with Two Dictionary Comprehensions
dictionary = {
    k1: {k2: k1 * k2 for k2 in range(1, 6)} for k1 in range(2, 5)
}
print(dictionary)

{2: {1: 2, 2: 4, 3: 6, 4: 8, 5: 10}, 
3: {1: 3, 2: 6, 3: 9, 4: 12, 5: 15},
4: {1: 4, 2: 8, 3: 12, 4: 16, 5: 20}}
```
Advantages of Using Dictionary Comprehension
* As we can see, dictionary comprehension shortens the process of dictionary initialization by a lot. It makes the code more pythonic.

* Using dictionary comprehension in our code can shorten the lines of code while keeping the logic intact.