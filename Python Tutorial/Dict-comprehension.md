# Dict comprehension

source: `{{ page.path }}`

`Dictionary comprehension` is a way to build a new dictionary by applying an expression to each item in an iterable.
Dictionaries are data types in Python which allows us to store data in key/value pair. For example:

D = {}
for x in range(5):
    D[x] = x**2

print(D)        # Prints {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

General syntax for a dictionary comprehension is:

![](./images/dict2.PNG)
![](./images/dict3.PNG)