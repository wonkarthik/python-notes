# Lambda Function

source: `{{ page.path }}`

`Lambda` is one of the most useful, important and interesting features in Python. Unfortunately, they are easy to misunderstand and get wrong.

What is a Lambda Function?
A lambda is simply a way to define a function in Python. They are sometimes known as lambda operators or lambda functions.

By now you probably have defined your functions using the def keyword, and it has worked well for you so far. So why is there another way to do the same thing?

The difference is that lambda functions are anonymous. Meaning, they are functions that do not need to be named. They are used to create small one-line functions in cases where a normal function would be an overkill.

#### Basic Example
Before looking at a lambda function, let’s look at a super basic function defined the “traditional” way: Here is a simple function that doubles the passed value.
```python
def doubler(x):
    return x*2

print(doubler(2))
# Prints 4

print(doubler(5))
# Prints 10

## Here’s how it looks as a lambda function:

doubler = lambda x: x*2

print(doubler(2))
# Prints 4

print(doubler(5))
# Prints 10
```
In the above example, the lambda is constructed as:

```javascript 

lambda parameters: expression 

```

#### Important Characteristics
##### Single Expression Only
Unlike a normal function, a lambda function contains only a single expression.

Although, you can spread the expression over multiple lines using parentheses or a multiline string, but it should only remain as a single expression.
```python
evenOdd = (lambda x:
           'odd' if x%2 else 'even')

print(evenOdd(2))
# Prints even

print(evenOdd(3))
# Prints odd
```

##### Immediately Invoked Function Expression (IIFE)
A lambda function can be immediately invoked. For this reason it is often referred to as an Immediately Invoked Function Expression (IIFE).

Here’s the same previously seen ‘doubler’ lambda function that is defined and then called immediately with 3 as an argument.

```python
print((lambda x: x*2)(3))
# Prints 6
```
#### Multiple Arguments

You can send as many arguments as you like to a lambda function; just separate them with a comma ,.

Here’s how you’d create a lambda function with multiple arguments:
```python
# A lambda function that multiplies two values
mul = lambda x, y: x*y
print(mul(2, 5))
# Prints 10
# A lambda function that adds three values
add = lambda x, y, z: x+y+z
print(add(2, 5, 10))
# Prints 17
```




























