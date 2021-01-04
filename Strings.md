
```python
c = "hello" # String
d = "4" # rebound to String
with_quote = "I ain't gonna"
longer = """This string has
multiple lines
in it"""
```

## String operations 
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


## Escape characters
```python
print('Text\tText')
print('Text\nText')
print('Text\'Text')
print('Text\\Text')
```

## String formating
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

## Padding and aligning
```python
'{:>10}'.format('test') # Align right
'{:10}'.format('test') # Align left
'{:^10}'.format('test') # center align
'{:x<10}'.format('test')
```

## Truncating
```python
'{:.5}'.format('xylophone')
'{:10.5}'.format('xylophone')
```

## Padding numbers
```python
'{:04d}'.format(42)  # Integers
'{:06.2f}'.format(3.141592653589793) # Floats
```
