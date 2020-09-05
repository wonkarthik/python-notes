# operators
source: `{{ page.path }}`

Operators are used to perform operations on values and variables. The Python operators are classified into seven different categories:

* Arithmetic operators
* Assignment operators
* Comparison operators
* Logical operators
* Identity operators
* Membership operators
* Bitwise operators
* Arithmetic Operators

### Arithmetic operators
`Arithmetic operators` are used to perform simple mathematical operations on numeric values (except complex).

|Operator	|Meaning	      |Example    |
|-----------|-----------------|-----------|
|+	        |Addition	      |x + y      |
|–	        |Subtraction	  |x – y      |
|*	        |Multiplication	  |x * y      |
|/	        |Division	      |x / y      |
|%	        |Modulus	      |x % y      |
|**	        |Exponentiation	  |x ** y     |
|//	        |Floor division	  |x // y     |

```
Here are some examples:

x = 6
y = 2

# addition
print(x + y)		# 8

# subtraction
print(x - y)		# 4

# multiplication
print(x * y)		# 12

# division
print(x / y)		# 3

# modulus
print(x % y)		# 0

# exponentiation
print(x ** y)		# 36

# floor division
print(x // y)		# 3

```
For additional numeric operations see the [math module](https://docs.python.org/3/library/math.html)

### Assignment Operators
Assignment operators are used to assign new values to variables.

|Operator	    |Meaning	                    |Example	     |Equivatent to   |
|---------------|-------------------------------|----------------|----------------|
|=	            |Assignment	                    |  x = 3	     |   x = 3        |
|+=	            | Addition assignment	        |  x += 3	     |   x = x + 3    |
|-=	            | Subtraction assignment	    |  x -= 3	     |   x = x – 3    |
|*=	            | Multiplication assignment	    |  x *= 3	     |   x = x * 3    |
|/=	            | Division assignment	        |  x /= 3	     |   x = x / 3    |
|%=	            | Modulus assignment	        |  x %= 3	     |   x = x % 3    |
|//=	        | Floor division assignment	    |  x //= 3	     |   x = x // 3   |
|**=	        | Exponentiation assignment	    |  x **= 3	     |   x = x ** 3   |
|&=	            | Bitwise AND assignment	    |  x &= 3	     |   x = x & 3    |
|=	            | Bitwise OR assignment	        |  x |= 3	     |   x = x | 3    |
|^=	            | Bitwise XOR assignment	    |  x ^= 3	     |   x = x ^ 3    |
|>>=	        | Bitwise right shift assignment|  x >>= 3	     |   x = x >> 3   |
|<<=	        | Bitwise left shift assignment	|  x <<= 3	     |   x = x << 3   |


### Comparison Operators
Comparison operators are used to compare two values.

|Operator  |Meaning                   |Example   |
|----------|--------------------------|----------|
|==	       | Equal to	              |  x == y  |
|!=	       | Not equal to	          |  x != y  |
|>	       | Greater than	          |  x > y   |
|<	       | Less than	              |  x < y   |
|>=	       | Greater than or equal to |	 x >= y  |
|<=	       | Less than or equal to	  |  x <= y  |

Here are some examples:
```
x = 6
y = 2

# equal to
print(x == y)		# False

# not equal to
print(x != y)		# True

# greater than
print(x > y)		# True

# less than
print(x < y)		# False

# greater than or equal to
print(x >= y)		# True

# less than or equal to
print(x <= y)		# False
```
### Logical Operators
Logical operators are used to join two or more conditions.

|Operator	        |Description	                                            |Example              | 
|-------------------|-----------------------------------------------------------|---------------------|
|and	            |Returns True if both statements are true	                |x > 0 and y < 0      |
|or	                |Returns True if one of the statements is true	            |x > 0 or y < 0       |
|not	            |Reverse the result, returns False if the result is true	|not (x > 0 and y < 0)|

Here are some examples:
```
x = 2
y = -2

# and
print(x > 0 and y < 0)          # True

# or
print(x > 0 or y < 0)           # True

# not
print(not(x > 0 and y < 0))     # False
```
### Identity Operators
Identity operators are used to check if two objects point to the same object, with the same memory location.

|Operator	        |Description                                             |Example      |
|-------------------|--------------------------------------------------------|-------------|
|is	                |Returns true if both variables are the same object	     |   x is y    |
|is not	            |Returns true if both variables are not the same object	 |   x is not y|

Here are some examples:
```
x = [1, 2, 3]
y = [1, 2, 3]

# is
print(x is y)		# False

# is not
print(x is not y)	# True
```
### Membership Operators
Membership operators are used to check if a specific item is present in a sequence (such as a string, tuple, list, or range) or a collection (such as a dictionary, set, or frozen set).

|Operator	      |Description	                                         |Example          |
|-----------------|------------------------------------------------------|-----------------|
|in	              |Returns True if a value is present in the sequence	 |  x in y         |
|not in	          |Returns True if a value is not present in the sequence|	x not in y     |

Here are some examples:
```
L = ['red', 'green', 'blue']

# in
print('red' in L)           # True

# not in
print('yellow' not in L)    # True
```
### Bitwise Operators
Binary operators are used to perform bit-level operations on (binary) numbers.

|Operator	  |Meaning	     |Example  |
|-------------|--------------|---------|
|&	          |  AND	     |   x & y |
||	          |  OR	         |   x | y |
|^	          |  XOR	     |   x ^ y |
|~	          |  NOT	     |   ~x    |
|<<	          |  Left shift  |	 x << 2|
|>>	          |  Right shift |	 x >> 2|

Here are some examples:
```
x = 0b1100
y = 0b1010

# and
print(bin(x & y))	    # 0b1000

# or
print(bin(x | y))	    # 0b1110

# xor
print(bin(x ^ y))	    # 0b0110

# not
print(bin(~x))		    # -0b1101

# shift 2 bits left
print(bin(x << 2))	    # 0b1100

# shift 2 bits right
print(bin(x >> 2))	    # 0b0011
```
### Operator Precedence (Order of Operations)
In Python, every operator is assigned a precedence. Operator Precedence determines which operations are performed before which other operations.

Operators of highest precedence are performed first. Any operators of equal precedence are performed in left-to-right order.

|Precedence	           |Operator	            |     Description                                         |
|----------------------|------------------------|---------------------------------------------------------|
|lowest precedence	   |  or	                |        Boolean OR                                       | 
|                      |  and	                |        Boolean AND                                      |
|                      |  not	                |        Boolean NOT                                      |
|                      |  ==, ! =, <, <=, >, >=,|                                                         |
|                      |  is, is not	        |        comparisons, identity                            |
|                      |  |	                    |        bitwise OR                                       |
|                      |  ^	                    |        bitwise XOR                                      |
|                      |  &	                    |        bitwise AND                                      |
|                      |  <<, >>	            |        bitwise shis                                     |
|                      |  +, –	                |        addition, subtraction                            |
|                      |  *, /, //, %	        |        multiplication, division, floor division, modulo |
|                      |  +x, -x, ~x	        |        unary positive, unary negation, bitwise negation |
|highest precedence	   |  **	                |        exponentiation                                   |
