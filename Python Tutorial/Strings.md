# Strings

source: `{{ page.path }}`

A string is a sequence of characters. You must have used strings in other languages as well. Python strings play the same role as character arrays in languages like C, but they are somewhat higher-level tools than arrays.

Unlike languages such as C, in Python, strings come with a powerful set of processing tools.

#### Create a String
A python string is zero or more characters written inside single quotes ' ' or double quotes " "
```python
S = 'Hello, World!'   # single quotes
S = "Hello, World!"   # double quotes
```

#### Multiline Strings
You can create a multiline string using triple-quotes: """  """ or '''  '''.
```python
S = """String literals can
span multiple lines."""
print(S)
# String literals can
# span multiple lines.
The str() Constructor
You can convert almost any object in Python to a string using a type constructor called str()

# an integer to a string
S = str(42)
print(S)
# Prints '42'

# a complex number to a string
S = str(3+4j)
print(S)
# Prints '(3+4j)

# a list to a string
S = str([1,1])
print(S)
# Prints '[1, 1]'
```