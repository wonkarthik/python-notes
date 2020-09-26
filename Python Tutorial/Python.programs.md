# Python Programs
source: `{{ page.path }}`
## Basic Programs
#### All Arithmetic operations of 2 no
```python
# Store input numbers:  
num1 = input('Enter first number: ')  
num2 = input('Enter second number: ')  
  
# Add two numbers  
add = float(num1) + float(num2)  
# Subtract two numbers  
sub = float(num1) - float(num2)  
# Multiply two numbers  
mul = float(num1) * float(num2)  
#Divide two numbers  
div = float(num1) / float(num2)  

# Display the sum  
print(f"The sum of {num1} and {num2} is {add}") 
# Display the subtraction  
print(f"The sub of {num1} and {num2} is {sub}") 
# Display the multiplication  
print(f"The mul of {num1} and {num2} is {mul}") 
# Display the division  
print(f"The div of {num1} and {num2} is {div}")
```
#### python program to swap 2 numbers
```python
# method 1
x = 1  
y = 0  
temp = x
x = y
y = temp
print(f"values of x={x} and y={y}")
# method 2
x = 1  
y = 0  
x,y = y,x
print(f"values of x={x} and y={y}")
# method 3
x = 10
y = 50
  
# Swapping of two variables 
# using arithmetic operations 
x = x + y    
y = x - y   
x = x - y 
print(f"values of x={x} and y={y}")
```
#### python program convert km to miles

```python
# converting Kilometer in to miles 
# 1 kilometer is equal to 0.62137 miles
x = float(input("enter the no of kilometers : "))
miles = x * 0.62137
print(f" Total no of {x} kilometers in to miles is {miles}")
```

#### python program convert celsius to Fahrenheit

```python

## T(℉) = T(℃) x 1.8 + 32
C = float(input("enter the celsius value : "))
F = ( C * 1.8 ) + 32
print(f"The celsius of {C} in Fahrenheit temp is {F}")
```

#### Python program to display calender

```python
import calendar  
# Enter the month and year  
yy = int(input("Enter year: "))  
mm = int(input("Enter month: "))  
  
# display the calendar  
print(calendar.month(yy,mm))
```

#### python program of multiplication table

```python
mul = int(input("Enter the no for multiplication : "))
for i in range(1,11):
    print(mul, "*" ,i, "=" ,mul * i)
```    

#### Pythom program for Leap Year

```python
year = int(input("Enter a year: "))  
if (year % 4) == 0:  
   if (year % 100) == 0:  
       if (year % 400) == 0:  
           print(f"{year} is a leap year")  
       else:  
           print(f"{year} is not a leap year")  
   else:  
       print(f"{year} is a leap year")  
else:  
   print(f"{year} is not a leap year") 
```   

#### Prime number

```python
for num in range(15):  
   if num > 1:  
       for i in range(2,num):
           if (num % i) == 0: 
               break  
       else:  
           print(f"{num} is prime number") 
```
#### Factorial number

```python
num = int(input("Enter a number: "))  
factorial = 1  
if num < 0:  
   print(" factorial does not exist for negative numbers")  
elif num == 0:  
   print("The factorial of 0 is 1")  
else:  
   for i in range(1,num + 1):  
       factorial = factorial*i  
   print("The factorial of",num,"is",factorial)
```
#### MAX and Min numbers

```python
# Given list of numbers
list = [ 3,2,19,10]

# sorting the given list "list"
# sort() function sorts the list in ascending order
list.sort()
# Displaying the first element of the list
# which is the smallest number in the sorted list
print("list of small number : ",list[0])
print("list of Big number : ",list[-1])

## method 2
list = [ 87,64,78,99,96 ]
print("Maximum number in list : ", max(list))
print("Minimum number in list : ", min(list))
```

#### sum of cubes 
An efficient solution is to use direct mathematical formula which is (n ( n + 1 ) / 2) ^ 2

```python
## method 1
def sumofcubes(n):
       sum = 0
       for i in range (1,n+1):
          sum += i*i*i
       return sum
n = int(input("enter the value of n: "))
print(sumofcubes(n))           

## method 2
# Returns the sum of series  with mathematical formula is  (n ( n + 1 ) / 2) ^ 2
def sumofcubes(n): 
	x = (n * (n + 1) / 2) 
	return (int)(x * x) 

# Driver Function 
n = int(input("Enter the value of number: "))
print(sumofcubes(n)) 

```
#### Sum of squares of natural numbers

```python
# Method 1
# Return the sum of  square of first n  natural numbers 
def squaresum(n) : 
	# Iterate i from 1  and n finding  square of i and  add to sum. 
	sum = 0
	for i in range(1, n+1) : 
		sum = sum + (i * i) 
	return sum 
n = int(input("enter the value of n : "))
print(squaresum(n)) 


# method 2

## n * (n + 1) * (2 * n + 1)/6 
def sumofsquares(n):
       sum = n * (n + 1) * (2 * n + 1) // 6
       return sum

n = int(input("enter the value of n : "))
print(sumofsquares(n))
```

#### Remove punctuation from string
```python
# Removing punctuations in string 
# Using regex 
import re 

# initializing string 
test_str = "python, is best  program: to learn !!!;"

# printing original string 
print("The original string is : " + test_str) 

# Removing punctuations in string Using regex 
res = re.sub(r'[^\w\s]', '', test_str) 

# printing result 
print("The string after punctuation filter : " + res) 

# output :
The original string is : python, is best  program: to learn !!!;
The string after punctuation filter : python is best  program to learn

```
