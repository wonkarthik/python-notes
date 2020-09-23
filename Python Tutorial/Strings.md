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

#### Access Characters by Index
You can access individual characters in a string using an index in square brackets. The string indexing starts from 0.

You can also access a string by negative indexing. A negative string index counts from the end of the string.

The indices for the elements in a string are illustrated as below:

![](./images/string.PNG)
```python
String Indexing
# Indexing
S = 'ABCDEFGHI'
print(S[0])    # Prints A
print(S[4])    # Prints E

# Negative Indexing
S = 'ABCDEFGHI'
print(S[-1])    # Prints I
print(S[-6])    # Prints D
```
#### Slicing a String
A segment of a string is called a slice and you can extract one by using a slice operator. A slice of a string is also a string.

The slice operator [n:m] returns the part of the string from the “n-th” item to the “m-th” item, including the first but excluding the last.
```python
S = 'ABCDEFGHI'
print(S[2:5])      # Prints CDE
print(S[5:-1])     # Prints FGH
print(S[1:6:2])    # Prints BDF
```
The string slicing capability provided by python is extensive and covered in full detail here.

#### Modify a String
It is tempting to use the [] operator on the left side of an assignment, in order to convert a character into a string. for example:
```python
S = 'Hello, World!'
S[0] = 'J'
# Triggers TypeError: 'str' object does not support item assignment
The reason for the error is that the strings are unchangeable (immutable) and because of which you cannot change the existing string. The best you can do is create a new string that is a variation of the original:

S = 'Hello, world!'
new_S = 'J' + S[1:]
print(new_S)
# Prints Jello, world!
```
#### String Concatenation
You can concatenate strings using the concatenation operator + or the augmented assignment operator +=
```python
# concatenation operator
S = 'Hello,' + ' World!'
print(S)
# Hello, World!

# augmented assignment operator
S = 'Hello,'
S += ' World!'
print(S)
# Prints Hello, World!

In Python, two or more strings next to each other are automatically concatenated, known as Implicit concatenation.

S = 'Hello,' " World!"
print(S)
# Prints Hello, World!
Implicit concatenation only works with two literals though, not with variables or expressions.

You can also put several strings within parentheses to join them together. This feature is useful when you want to break long strings.

S = ('Put strings within parentheses '
    'to join them together.')
print(S)
# Put strings within parentheses to join them together.
```
You can replicate substrings in a string using the replication operator *
```
# the hard way
S = '--------------------'

# the easy way
S = '-' * 20
```
#### Find String Length
To find the number of characters in a string, use len() built-in function.
```python
S = 'Supercalifragilisticexpialidocious'
print(len(S))
# Prints 34
```
#### Replace Text Within a String
Sometimes you want to replace a text inside a string, then you can use the replace() method.
```python
S = 'Hello, World!'
x = S.replace('World', 'Universe')
print(x)
# Prints Hello, Universe!
```
#### Split and Join a String
Use split() method to chop up a string into a list of substrings, around a specified delimiter.
```python
# Split the string on comma
S = 'red,green,blue,yellow'
x = S.split(',')
print(x)
# Prints ['red', 'green', 'blue', 'yellow']
print(x[0])
# Prints red

And use join() method to join the list back into a string, with a specified delimiter in between.

# Join the list of substrings
L = ['red', 'green', 'blue', 'yellow']
S = ','.join(L)
print(S)
# Prints red,green,blue,yellow
```
#### String Case Conversion
Python provides five methods to perform case conversion on the target string viz. lower(), upper(), capitalize(), swapcase() and title()
```python
S = 'Hello, World!'
print(S.lower())
# Prints hello, world!

S = 'Hello, World!'
print(S.upper())
# Prints HELLO, WORLD!

S = 'Hello, World!'
print(S.capitalize())
# Prints Hello, world!

S = 'Hello, World!'
print(S.swapcase())
# Prints hELLO, wORLD!

S = 'hello, world!'
print(S.title())
# Prints Hello, World!
```
#### Check if Substring Contains in a String
To check if a specific text is present in a string, use in operator. The in is a boolean operator, which takes two strings and returns True if the first appears as a substring in the second:

```python
S = 'Hello, World!'
print('Hello' in S)
# Prints True
```
To search for a specific text within a string, use find() method. It returns the lowest index in the string where substring is found.

```python
# Search for 'Foolish' within a string
S = 'Stay Hungry, Stay Foolish'
x = S.find('Foolish')
print(x)
# Prints 18

```
#### Iterate Through a String
To iterate over the characters of a string, use a simple for loop.
```python
# Print each character in a string
S = 'Hello, World!'
for letter in S:
    print(letter, end=' ')
# H e l l o ,   W o r l d !
``` 
#### Python Escape Sequence
You can use quotes inside a string, as long as they don’t match the quotes surrounding the string.
```python
S = "We're open"		# Escape single quote
S = "I said 'Wow!'"		# Escape single quotes
S = 'I said "Wow!"'		# Escape double quotes
```
This is fine for most of the time but what if you want to declare a string with both single and double quotes like:

`Bob told me, “Sam said, ‘This won’t work.'”`

Python will raise a `SyntaxError`, because both quotation marks are special characters. The solution to avoid this problem is to use the backslash escape character \.

Prefixing a special character with \ turns it into an ordinary character. This is called escaping.
```python
S = "Bob told me, \"Sam said, 'This won't work.'\""
print(S)
# Prints Bob told me, "Sam said, 'This won't work.'"
Backslash escape character is used in representing certain special characters like: \n is a newline, \t is a tab. These are known as escape sequences.

S = str('First line.\n\tSecond line.')
print(S)
# First line.
#     Second line.
```
#### String Methods

|Function	    |Description                                                                                                                    |
|---------------|-------------------------------------------------------------------------------------------------------------------------------|
|encode()	    |Python string encode() function is used to encode the string using the provided encoding.                                      |
|count()	    |Python String count() function returns the number of occurrences of a substring in the given string.                           |
|startswith()	|Python string startswith() function returns True if the string starts with the given prefix, otherwise it returns False.       |
|endswith()	    |Python string endswith() function returns True if the string ends with the given suffix, otherwise it returns False.           |
|capitalize()	|Python String capitalize() function returns the capitalized version of the string.                                             |
|center()	    |Python string center() function returns a centered string of specified size.                                                   |
|casefold()	    |Python string casefold() function returns a casefolded copy of the string. This function is used to perform case-insensitive   | |               |string comparison.                                                                                                             |
|expandtabs()	|Python string expandtabs() function returns a new string with tab characters (\t) replaced with one or more whitespaces.       |
|index()	    |Python String index() function returns the lowest index where the specified substring is found.                                |
| __contains__()|Python String class has __contains__() function that we can use to check if it contains another string or not. We can also use | |               | “in” operator to perform this check.                                                                                          |


##### Built-in String Functions in Python

`Conversion Functions`

1. capitalize() – Returns the string with the first character capitalized and rest of the characters in lower case.
```python
var = 'PYTHON'
print (var.capitalize())
# Python
```
2. lower() – Converts all the characters of the String to lowercase
```python
var = 'FootBall'
print (var.lower())
# football
```l
3. upper() – Converts all the characters of the String to uppercase
```python
var = 'FootBall'
print (var.upper())
# FOOTBALL
```
4. swapcase() – Swaps the case of every character in the String means that lowercase characters got converted to uppercase and vice-versa.
```python
var = 'FootBall'
print (var.swapcase())
# fOOTbALL
```
5. title() – Returns the ‘titlecased’ version of String, which means that all words start with uppercase and the rest of the characters in words are in lowercase.
```python
var = 'welcome to Python programming'
print (var.title())
# Welcome To Python Programming
```
6. `count( str[, beg [, end]])` – Returns the number of times substring ‘str’ occurs in the range [beg, end] if beg and end index are given else the search continues in full String Search is case-sensitive.
```python
var='Television'
str='e'
print (var.count(str))
# 2
var1='Eagle Eyes'
print (var1.count('e'))
# 2
var2='Eagle Eyes'
print (var2.count('E',0,5))
# 1
```
`Comparison Functions – Part1`
1. islower() – Returns ‘True’ if all the characters in the String are in lowercase. If any of the char is in uppercase, it will return False.
```python
var='Python'
print (var.islower())
# False

var='python'
print (var.islower())
# True
```
2. isupper() – Returns ‘True’ if all the characters in the String are in uppercase. If any of the char is in lowercase, it will return False.
```python
var='Python'
print (var.isupper())
# False

var='PYTHON'
print (var.isupper())
# True
```
3. isdecimal() – Returns ‘True’ if all the characters in String are decimal. If any character in the String is of other data-type, it will return False.Decimal characters are those from the Unicode category Nd.
```python
num=u'2016'
print (num.isdecimal())
# True
```
4. isdigit() – Returns ‘True’ for any char for which isdecimal() would return ‘True and some characters in the ‘No’ category. If there are any characters other than these, it will return False’.

Precisely, digits are the characters for which Unicode property includes: Numeric_Type=Digit or Numeric_Type=Decimal.

For example, superscripts are digits, but fractions not.
```python
print ('2'.isdigit())
# True

print ('²'.isdigit())
# True
```
`Comparison Functions – II`
1. isnumeric() – Returns ‘True’ if all the characters of the Unicode String lie in any one of the categories Nd, No, and NI.

If there are any characters other than these, it will return False.

Precisely, Numeric characters are those for which Unicode property includes: Numeric_Type=Digit, Numeric_Type=Decimal or Numeric_Type=Numeric.
```python
num=u'2016'
print (num.isnumeric())
# True

num=u'year2016'
print (num.isnumeric())
# False
```
2. isalpha() – Returns ‘True’ if String contains at least one character (non-empty String), and all the characters are alphabetic, ‘False’ otherwise.
```python
print ('python'.isalpha())
# True

print ('python3'.isalpha())
# False
```
3. isalnum() – Returns ‘True’ if String contains at least one character (non-empty String), and all the characters are either alphabetic or decimal digits, ‘False’ otherwise.
```python
print ('python'.isalnum())
# True
print ('python3'.isalnum())
# True
```
`Padding Functions`
1. rjust(width[,fillchar]) – Returns string filled with input char while pushing the original content on the right side.

By default, the padding uses a space. Otherwise, ‘fillchar’ specifies the filler character.
```python
var='Python'
print (var.rjust(10))
# Python

print (var.rjust(10,'-'))
# ----Python
```
2. ljust(width[,fillchar]) – Returns a padded version of String with the original String left-justified to a total of width columns

By default, the padding uses a space. Otherwise, ‘fillchar’ specifies the filler character.
```python
var='Python'
print (var.ljust(10))
# Python

print (var.ljust(10,'-'))
# Python----
```
3. center(width[,fillchar]) – Returns string filled with the input char while pushing the original content into the center.

By default, the padding uses a space. Otherwise, ‘fillchar’ specifies the filler character.
```python
var='Python'
print (var.center(20))
# Python

print (var.center(20,'*'))
# *******Python*******
```
4. zfill(width) – Returns string filled with the original content padded on the left with zeros so that the total length of String becomes equal to the input size.

If there is a leading sign (+/-) present in the String, then with this function, padding starts after the symbol, not before it.
```python
var='Python'
print (var.zfill(10))
# 0000Python

var='+Python'
print (var.zfill(10))
# +000Python
```
`Search Functions`
1. find(str [,i [,j]]) – Searches for ‘str’ in complete String (if i and j not defined) or in a sub-string of String (if i and j are defined).This function returns the index if ‘str’ is found else returns ‘-1’.

Here, i=search starts from this index, j=search ends at this index.
See more details – Python String Find()
```python
var="High sky"
str="sky"
print (var.find(str))
# 5

var="High sky"
str="sky"
print (var.find(str,4))
# 5

var="High sky"
str="sky"
print (var.find(str,7))
# -1
```
2. index(str[,i [,j]]) – This is same as ‘find’ method. The only difference is that it raises the ‘ValueError’ exception if ‘str’ doesn’t exist.
```python
var='High Sky'
str='sky'
print (var.index(str))
# 5

var='High Sky'
str='sky'
print (var.index(str,4))
# 5

var='High Sky'
str='sky'
print (var.index(str,7))
# ValueError: substring not found
```
3. rfind(str[,i [,j]]) – This is same as find() just that this function returns the last index where ‘str’ is found. If ‘str’ is not found, it returns ‘-1’.
```python
var='This is a good example'
str='is'
print (var.rfind(str,0,10))
# 5

print (var.rfind(str,10))
# -1
```
4. count(str[,i [,j]]) – Returns the number of occurrences of substring ‘str’ in the String. Searches for ‘str’ in the complete String (if i and j not defined) or in a sub-string of String (if i and j are defined).

Where: i=search starts from this index, j=search ends at this index.
```python
var='This is a good example'
str='is'
print (var.count(str))
# 2

print (var.count(str,4,10))
# 1
```

`String Substitution Functions`
1. replace(old,new[,count]) – Replaces all the occurrences of substring ‘old’ with ‘new’ in the String.

If the count is available, then only ‘count’ number of occurrences of ‘old’ will be replaced with the ‘new’ var.

Where old =substring to replace, new =substring
```python
var='This is a good example'
str='was'
print (var.replace('is',str))
# Thwas was a good exampleprint (var.replace('is',str,1))
# Thwas is a good example
```
2. split([sep[,maxsplit]]) – Returns a list of substring obtained after splitting the String with ‘sep’ as a delimiter.

Where, sep= delimiter, the default is space, maxsplit= number of splits to be done
```python
var = "This is a good example"
print (var.split())
# ['This', 'is', 'a', 'good', 'example']print (var.split(' ', 3))
# ['This', 'is', 'a', 'good example']
```
3. splitlines(num) – Splits the String at line breaks and returns the list after removing the line breaks.

Where num = if this is a positive value. It indicates that line breaks will appear in the returned list.
```python
var='Print new line\nNextline\n\nMove again to new line'
print (var.splitlines())
# ['Print new line', 'Nextline', '', 'Move again to new line']print (var.splitlines(1))
# ['Print new line\n', 'Nextline\n', '\n', 'Move again to new line']
```
4. join(seq) – Returns a String obtained after concatenating the sequence ‘seq’ with a delimiter string.

Where: the seq= sequence of elements to join
```python
seq=('ab','bc','cd')
str='='
print (str.join(seq))
# ab=bc=cd
```

`Misc String Functions`
1. lstrip([chars]) – Returns a string after removing the characters from the beginning of the String.

Where: Chars=this is the character to be trimmed from the String.

The default is whitespace character.
```python
var=' This is a good example '
print (var.lstrip())
# This is a good example
var='*****This is a good example*****'
print (var.lstrip('*'))
# This is a good example**********
```
2. rstrip() – Returns a string after removing the characters from the End of the String.

Where: Chars=this is the character to be trimmed from the String. The default is whitespace character.
```python
var=' This is a good example '
print (var.rstrip())
# This is a good example
var='*****This is a good example*****'
print (var.lstrip('*'))
# *****This is a good example
```
3. rindex(str[,i [,j]]) – Searches for ‘str’ in the complete String (if i and j not defined) or in a sub-string of String (if i and j are defined). This function returns the last index where ‘str’ is available.

If ‘str’ is not there, then it raises a ValueError exception.

Where: i=search starts from this index, j=search ends at this index.
```python
var='This is a good example'
str='is'
print (var.rindex(str,0,10))
# 5
print (var.rindex(str,10))
# ValueError: substring not found
```
4. len(string) – Returns the length of given String
```python
var='This is a good example'
print (len(var))
# 22
```
