
#  Attributes

```python
import numpy as np
a = np.zeros([2,3])
a.ndim # 2 rows (axis=0) and columns (axis=1)
a.shape # (2, 3)
a.size # 6
a.dtype #  dtype('float64')
a.itemsize # 8  = size (in bytes) of each element
a.T # The transposed array.
a.flat # 1-D iterator over the array.
a.imag # The imaginary part of the array.
a.real # The real part of the array.
```


# Methods

```python
all([axis, out, keepdims])
any([axis, out, keepdims])
argmax([axis, out])
argmin([axis, out])
argpartition(kth[, axis, kind, order])
argsort([axis, kind, order])
astype(dtype[, order, casting, subok, copy])
byteswap([inplace])
choose(choices[, out, mode])
clip([min, max, out])
compress(condition[, axis, out])
conj()
conjugate()
copy([order])
cumprod([axis, dtype, out])
cumsum([axis, dtype, out])
diagonal([offset, axis1, axis2])
dot(b[, out])
dump(file)
dumps()
fill(value)
flatten([order])
getfield(dtype[, offset])
item(*args)
itemset(*args)
max([axis, out, keepdims, initial, where])
mean([axis, dtype, out, keepdims])
min([axis, out, keepdims, initial, where])
newbyteorder([new_order])
nonzero()
partition(kth[, axis, kind, order])
prod([axis, dtype, out, keepdims, initial, …])
ptp([axis, out, keepdims])
put(indices, values[, mode])
ravel([order])
repeat(repeats[, axis])
reshape(shape[, order])
resize(new_shape[, refcheck])
round([decimals, out])
searchsorted(v[, side, sorter])
setfield(val, dtype[, offset])
setflags([write, align, uic])
sort([axis, kind, order])
squeeze([axis])
std([axis, dtype, out, ddof, keepdims])
sum([axis, dtype, out, keepdims, initial, where])
swapaxes(axis1, axis2)
take(indices[, axis, out, mode])
tobytes([order])
tofile(fid[, sep, format])
tolist()
tostring([order])
trace([offset, axis1, axis2, dtype, out])
transpose(*axes)
var([axis, dtype, out, ddof, keepdims])
view([dtype][, type])
```
