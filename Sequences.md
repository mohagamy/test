
Sequences (Containers):


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

## Dictionaries (Hash tables, associative arrays)
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
