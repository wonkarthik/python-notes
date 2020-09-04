Python Numbers
In Python, there are three distinct numeric types:

##### Integers
Floating-point numbers
Complex numbers
Python Numbers - Integers, Floats, Complex Numbers
Integers
An integer is a whole number that can be positive or negative.

# Following numbers are integers
```css
x = 10
y = -10
z = 123456789
```
In Python 3, there is no limit to how long an integer value can be. It can grow to have as many digits as your computer’s memory space allows.
```
# Integers have unlimited precision
x = 99999999999999999999999999999999999999999999999999999999999999999999999999999999
```
We normally write integers in base 10. However, Python allows us to write integers in Hexadecimal (base 16), Octal (base 8), and Binary (base 2) formats. You can do that by adding one of the following prefixes to the integer.
```sh
Prefix	Interpretation	Base
‘0b’ or ‘0B’	Binary	2
‘0o’ or ‘0O’	Octal	8
‘0x’ or ‘0X’	Hexadecimal	16
```
```
# Integers in binary, octal and hexadecimal formats

# binary
print(0b10111011)
# Prints 187

# octal
print(0o10)
# Prints 8

# hex
print(0xFF)
# Prints 255
In addition, Boolean is a sub-type of integers.

# Boolean in python
x = True
x = False
```
#### Floating-Point Numbers
Floating-point number or Float is a positive or negative number with a fractional part.
```
# Following numbers are floats
x = 10.1
y = -10.5
z = 1.123456
```
You can append the character e or E followed by a positive or negative integer to specify `scientific notation`.
```
# Scientific notation
print(42e3)
# Prints 42000.0

print(4.2e-3)
# Prints 0.0042
```
The maximum value a float can have is approximately 1.8×10308 . Any number greater than that is indicated by the string inf (infinity)
```
# Maximum value of a float
print(1.79e308)
# Prints 1.79e+308

print(1.8e308)
# Prints inf
```
However, the minimum value a float can have is approximately 5.0×10-324 . Any number, less than that is considered zero.
```
# Minimum value of a float
print(5e-324)
# Prints 4.94065645841e-324

print(5e-325)
# Prints 0.0
```
#### Complex Numbers
A complex number is specified as real_part + imaginary_part, where the imaginary_part is written with a j or J.
```
# Following numbers are complex numbers
x = 2j
y = 3+4j
```
To extract real and imaginary parts from a complex number x, use x.real and x.imag
```
x = 3+4j

# real part
print(x.real)
# Prints 3.0

# imaginary part
print(x.imag)
# Prints 4.0
```
Table Of Contents
Numeric Types in Python
Integers
Floating-Point Numbers
Complex Numbers
  
