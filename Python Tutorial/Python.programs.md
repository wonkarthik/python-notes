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
