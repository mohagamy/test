- [Basics](#basics)
  * [Interactive shell](#interactive-shell)
  * [Value assignment](#value-assignment)
  * [Multiple assignment](#multiple-assignment)
  * [Unpacking sequence](#unpacking-sequence)
  * [Conditional Assignment](#conditional-assignment)
  * [Deletion](#deletion)
  * [object id, type, and value](#object-id--type--and-value)
  * [Mutable and immutable variables](#mutable-and-immutable-variables)
  * [Boolean](#boolean)
  * [Strings](#strings)
    + [String operations](#string-operations)
    + [Escape characters](#escape-characters)
    + [String formating](#string-formating)
    + [Padding and aligning](#padding-and-aligning)
    + [Truncating](#truncating)
    + [Padding numbers](#padding-numbers)
    + [String operations](#string-operations-1)
- [Logical Operations](#logical-operations)
  * [Basic conditions](#basic-conditions)
  * [Combined conditions](#combined-conditions)
  * [Simplified combined conditions](#simplified-combined-conditions)
- [Mathematical Operations](#mathematical-operations)
  * [Division](#division)
  * [Basic math functions](#basic-math-functions)
  * [Advanced math functions](#advanced-math-functions)
  * [Random library](#random-library)
- [Sequences (Containers):](#sequences--containers--)
  * [Lists](#lists)
    + [List operations](#list-operations)
  * [Dictionaries ( Hash tables, associative arrays)](#dictionaries---hash-tables--associative-arrays-)
    + [Read:](#read-)
    + [Delete](#delete)
    + [Insert](#insert)
    + [Update](#update)
    + [Keys, values, items:](#keys--values--items-)
  * [Tuples](#tuples)
  * [Sets](#sets)
- [Generic operations for containers](#generic-operations-for-containers)
  * [If statement](#if-statement)
  * [Loop Over Sequence](#loop-over-sequence)
  * [Loop with multiple variables](#loop-with-multiple-variables)
  * [Loop while](#loop-while)
  * [Loop Break](#loop-break)
  * [Loop skip](#loop-skip)
- [Classes and Instances](#classes-and-instances)
- [Modules & Packages](#modules---packages)
- [Files](#files)
- [Functions and Procedures](#functions-and-procedures)
  * [Function Definition](#function-definition)
  * [Function Call](#function-call)
- [List Comprehensions](#list-comprehensions)
- [Generators](#generators)
- [Lambda, filter, reduce and map](#lambda--filter--reduce-and-map)


# Basics

## Interactive shell
```python 
3+2
x = 12
print('hello world')
age = int(input("How old are you? "))   # explicit cast to int or float if needed.
```

## Value assignment
```python 
a = [1, 2, 3]
b = a
a.append(4)
print(b) #[1, 2, 3, 4], b = a does not make a copy of a but makes b reference to the object a references
```

## Multiple assignment
```python 
a1,a2,a3 = 2,5,6
a1 = a2 = a3 = 5
```

## Unpacking sequence
```python 
first,*remain = [2,3, 4,5]
s = "Jessica 31 647.28"
name, age, money = s.split()
```

## Conditional Assignment
```python 
b=8
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

#Variables 

##Numbers
```python
a = 4 # Integer
b = 5.6 # Float
```

## Boolean
```python
e = True
f = False
```


## Strings
```python
c = "hello" # String
d = "4" # rebound to String
with_quote = "I ain't gonna"
longer = """This string has
multiple lines
in it"""
```

### String operations 
```python
dir("a string")
help("a string".startswith)
"hello"+"world"			# concatenation
"hello"*3				# repetition
"hello"[0]				# indexing
"hello"[-1]				# (from end)
"hello"[1:4]			# slicing
len("hello")		    # size
"e" in "hello"			# search
for c in "booyah":		# loop 
    print(c)
s = ' <This is some text> '
s1 = ' <This is another text> '
n = 4
s*n #(repeat)
s+s1 #(concatenate)
s1 = ' <This is another text> '
s1.split()
s1.split('another')
' '.join(['we', 'add','more','text'])
'O'.join([' we ', ' add ',' more ',' text '])
s.replace('some','additional')
s.find('is')
s.count('is')
s.index('is')
s.lower()
s.upper()
s.strip(' ').strip('>').strip('<')
s.startswith(' ')
s.startswith('T')
s.endswith(' ')
```


### Escape characters
```python
print('Text\tText')
print('Text\nText')
print('Text\'Text')
print('Text\\Text')
```

### String formating
```python
"I am {} years old and I lived in {} countries".format(38,4)
s = "I am {} years old and I lived in {} countries"
s.format(38,4)
"{1} {0} {0}".format(3,9)
"{x} {y}".format(y=2,x=5)
"{0!r} {0!s}".format("text\n") # !s or !r renders the output of str() or repr()
"{0} in binary is {0:b} and in octal is {0:o} and in hexadecimal is {0:x}".format(100)
"Fixed point: {0:0.4f} General format: {0:0.8g} Exponent notation: {0:.1e}".format(1.44573463463745)
```

### Padding and aligning
```python
'{:>10}'.format('test') # Align right
'{:10}'.format('test') # Align left
'{:^10}'.format('test') # center align
'{:x<10}'.format('test')
```

### Truncating
```python
'{:.5}'.format('xylophone')
'{:10.5}'.format('xylophone')
```

### Padding numbers
```python
'{:04d}'.format(42)  # Integers
'{:06.2f}'.format(3.141592653589793) # Floats
```

### String operations
```python
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
print(math.e)
print(math.pi)
x = 3.57855
print([math.ceil(x) ,math.floor(x), math.trunc(x) ])
[ math.exp(x), math.log(x)]
[math.sqrt(x), math.cos(x), math.sin(x), math.tan(x)]
```

## Random library
```python
import random
random.seed(2)
x = [1,9,2,4,7,5,6]
[random.random() , random.randint(3,12) , random.randrange(3,10,2) , random.uniform(2,40) , random.choice(x)]
```

# Sequences (Containers):


## Lists
```python
a = [99, "bottles of beer", ["on", "the", "wall"]]
a*3, a[0], a[-1], a[1:], len(a)
a[0] = 98
a[1:2] = ["bottles", "of", "beer"]
del a[-1]
```

### List operations
```python
a =  [0,1,2,3,4]
a.append([5,6])		# [0,1,2,3,4,5,6]
a.extend([5,6])
a.pop()			# [0,1,2,3,4]
a.insert(0, 42)		# [42,0,1,2,3,4]
a.pop(0)			# [0,1,2,3,4]
a.reverse()		# [4,3,2,1,0]
a.sort()			# [0,1,2,3,4]
a.remove(2)
```

## Dictionaries ( Hash tables, associative arrays)
```python
d = {1: 'one', 2: 'two'}
d = dict(a=2, b=4)
age = {}
age['george'] = 10
age['fred'] = 12
age['henry'] = 10
```

### Read:
```python
age['george']
'matt' in age
'charles' not in age
```

### Delete
```python
del age['charles']
```

### Insert
```python
age.setdefault('max', 11)
age['Alice'] = 14
```

### Update
```python
age['matt'] = 15
```

### Keys, values, items:
```python
age.keys()
age.values()
age.items()
```

## Tuples
```python
a =(9,'x',[3,7,'new'])
key = ('lastname', 'firstname')
x,y,z = 2,5,7
point = x, y, z	 # parentheses optional
x, y, z = point   # unpack
lastname = key[0]
singleton = (1,)	 # trailing comma!!!
empty = ()		 # parentheses!
```

## Sets
```python
s = {1,'toto',42}
set([1,5,7,8,3])
a = set('Hello')
a.add('m')
a.remove('H')
```

# Generic operations for containers
```python
'h' in 'hello'
3 not in [3, 4 ,6, 9]
len((2,3,5))
max([3, 4 ,6, 9])
min([3, 4 ,6, 9])
sum([3, 4 ,6, 9])
reversed([3, 4 ,6, 9])
sorted([3, 4 ,6, 9])
```

#Flow Control

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
