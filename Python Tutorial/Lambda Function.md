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

** lambda parameters: expression **

```
