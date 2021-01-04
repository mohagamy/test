
# Basics

## Interactive shell

```python 
age = int(input("How old are you? "))   # explicit cast to int or float if needed.
```

## Value assignment

```python 
a = [1, 2, 3]
b = a
a.append(4)
print(b) 
#[1, 2, 3, 4], b = a does not make a copy of a but makes b reference to the object a references
```

## Multiple assignment

```python 
a1, a2, a3 = 2, 5, 6
a1 = a2 = a3 = 5
```

## Unpacking sequence
```python 
first,*remain = [2, 3, 4, 5]
s = "Jessica 31 647.28"
name, age, money = s.split()
```

## Conditional Assignment
```python 
b = 8
a = 3 if b>5 else 9
```

## Deletion
```python
del a1
```

## object id, type, and value
```python
a = 4
id(a)
type(a)
dir(a)
```

## Mutable and immutable variables
```python
b = []
id(b)
b.append(3)
id(b)
a = 4
id(a)
a = 5
id(a)
``` 


# Logical Operations

## Basic conditions
```python
a=2
b=3
print([a<b , a<=b ,  a>=b ,  a>b,   a==b ,  a!=b])
```

## Combined conditions

```python
a= True
b= False
print([ not a  ,  a and b ,   a or b])
```

## Simplified combined conditions
```python
x = 20
12 < x <= 34
```

# Mathematical Operations
```python
a=2
b=5
m =[-a,a+b,a-b,a*b,a**b]
print(m)
```

## Division
```python
m =[a/b,a//b,a%b]
print(m)
# a/b floating point division
# a//b floor division
# a%b remainder
```


## Basic math functions
```python
x = -3.6584726633
abs(x)
pow(2,3)
round(x,4)
```

## Advanced math functions
```python
import math
math.e
math.pi
x = 3.57855
math.ceil(x)
math.floor(x)
math.trunc(x)
math.exp(x)
math.log(x)
math.sqrt(x)
math.cos(x)
math.sin(x)
math.tan(x)
```

## Random library
```python
import random
random.seed(2)
x = [1,9,2,4,7,5,6]
random.random()
random.randint(3,12)
random.randrange(3,10,2)
random.uniform(2,40)
random.choice(x)
```


# Flow Control

## If statement
```python
if condition1:
    # block executed if condition1 is true
elif condition2:
    # block executed if condition2 is true
else:
    # block executed if all conditions are false
```

```python
grade = 75
if grade > 90:
    print('A')
elif grade > 80:
    print('B')
elif grade > 70:
    print('C')
else:
    print('D')
```

## Loop Over Sequence
```python
for var in iterable:
    # block executed with var being successively
    # each of the values in iterable
else:
    # executed after, except if exit for loop by break
```

## Loop with multiple variables
```python
for index,value in enumerate( )
```

```python
for number in [1, 2, 3, 4, 5, 6]:
    print(number)

for x in range(1, 6):
    print(x, "squared is", x * x)

for x in range(5, 0, -1):
    print(x)


animals = ["cat", "dog", "bird"]

for index, value in enumerate(animals):
    print(index, value)

sequence = [2, 5, 7, -3, 2, -7]
for item in sequence:
    # process until first negative
    if item < 0:
        break
    # process item
    print(item)


for item in sequence:
    if item < 0:
        continue
    # process all positive items
    print(item)


my_dict = {"name": "matt", "cash": 5.45}

for key in my_dict.keys():
    # process key
    print(key)

for value in my_dict.values():
    # process value
    print(value)

for key, value in my_dict.items():
    # process items
    print( str(key) + ': ' + str(value))

```

## Loop while
```python
while condition:
    # block executed while condition is true
else:
    # executed after, except if exit while loop by break
```

```python
number = 1
while number < 200:
    print(number)
    number = number * 2
```

## Loop Break
```python
break # Immediate exit of the loop, without going through else block.
```

## Loop skip
```python
continue # Immediate skip to the next iteration.
```

# Classes and Instances

```python
class Animal(object):
    def __init__(self, name):
        self.name = name

    def talk(self):
        print("Generic Animal Sound")
```

```python
animal = Animal("thing")
animal.name
animal.talk()
```

```python
class Cat(Animal):
    def talk(self):
        print('{} says, "Meow!"'.format(self.name))

cat1 = Cat("Groucho")
cat1.name
cat1.talk()  # invoke method
```

```python
class Cheetah(Cat):
    """classes can have docstrings"""

    def talk(self):
        print("Growl")
```

```python
Cheetah.__doc__
c = Cheetah("Tiger")
c.name
c.talk()  # invoke method
```

# Modules & Packages
```python
import package
import module
from math import sin
import longname as ln
```

```python
import os
help(os)
help(os.makedirs)
os.makedirs('aa/bb/cc/dd')
```

# Files
```python
fid = open("myfile.txt", 'w+')
fid.write('hello\n'*20)
print(file_text)
fid.close()
```

```python
count = 0
for line in open("myfile.txt").readlines():
    count = count + 1
print("The file contains {} lines.".format(count))
```

```python
count = 0
with open('myfile.txt') as fin:
    for line in fin:
        count = count + 1
print("The file contains {} lines.".format(count))
```

```python
name.read() #- file's entire contents as a string
name.readline() #- next line from file as a string
name.readlines() #- file's contents as a list of lines
```

# Functions and Procedures

## Function Definition
```python
def fname(x,y=4,*args,**kwargs):
    # function block or, if no code, pass
    return ret_expression

    # x: simple parameter
    # y: parameter with default value
    # args: variable parameters by order (tuple)
    # kwargs: named variable parameters (dict)
    # ret_expression: tuple return multiple values
```

## Function Call
```python
res = fname(expr,param=expr,*tuple,**dict)
```

```python
def add_2(num):
    return num + 2
five = add_2(3)
```

```python
def add_n(num, n=3):
    return num + n
five = add_n(2)
ten = add_n(15, -5)
```

# List Comprehensions
```python
[expr for var in iter if cond]
S = [x**2 for x in range(10)]
M = [x for x in S if x % 2 == 0]
```

# Generators
```python
variable = (yield expression)  #transmission of values to the generator.
```

```python
g = range(2,20,3)
r = ( 2*x+5 for x in g if x%2==0  )
r.__next__()
```

```python
x = iter([1, 2, 3])
x.__next__()
```

```python
t = enumerate('text')
t.__next__()
```

# Lambda, filter, reduce and map
```python
lambda x,y: expression
```

```python
sum = lambda x, y : x + y
sum(3,4)
```

```python
def fahrenheit(T):
    return ((float(9)/5)*T + 32)
def celsius(T):
    return (float(5)/9)*(T-32)

temp = (36.5, 37, 37.5,39)

F = list(map(fahrenheit, temp))
C = list(map(celsius, F))
```

```python
temp = (36.5, 37, 37.5,39)
F = list(map( lambda x: ((float(9)/5)*x + 32) , temp))
C = list(map( lambda x: (float(5)/9)*(x-32), F))
```

```python
fibonacci = [0,1,1,2,3,5,8,13,21,34,55]
odd_numbers = list(filter(lambda x: x % 2, fibonacci))
```

```python
import functools
functools.reduce(lambda x,y: x+y, [47,11,42,13])
```

```python
from functools import reduce
f = lambda a,b: a if (a > b) else b
reduce(f, [47,11,42,102,13])
```
