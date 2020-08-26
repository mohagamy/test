
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
np.all([axis, out, keepdims])
np.any([axis, out, keepdims])
np.argmax([axis, out])
np.argmin([axis, out])
np.argpartition(kth[, axis, kind, order])
np.argsort([axis, kind, order])
np.astype(dtype[, order, casting, subok, copy])
np.byteswap([inplace])
np.choose(choices[, out, mode])
np.clip([min, max, out])
np.compress(condition[, axis, out])
np.conj()
np.conjugate()
np.copy([order])
np.cumprod([axis, dtype, out])
np.cumsum([axis, dtype, out])
np.diagonal([offset, axis1, axis2])
np.dot(b[, out])
np.dump(file)
np.dumps()
np.fill(value)
np.flatten([order])
np.getfield(dtype[, offset])
np.item(*args)
np.itemset(*args)
np.max([axis, out, keepdims, initial, where])
np.mean([axis, dtype, out, keepdims])
np.min([axis, out, keepdims, initial, where])
np.newbyteorder([new_order])
np.nonzero()
np.partition(kth[, axis, kind, order])
np.prod([axis, dtype, out, keepdims, initial, …])
np.ptp([axis, out, keepdims])
np.put(indices, values[, mode])
np.ravel([order])
np.repeat(repeats[, axis])
np.reshape(shape[, order])
np.resize(new_shape[, refcheck])
np.round([decimals, out])
np.searchsorted(v[, side, sorter])
np.setfield(val, dtype[, offset])
np.setflags([write, align, uic])
np.sort([axis, kind, order])
np.squeeze([axis])
np.std([axis, dtype, out, ddof, keepdims])
np.sum([axis, dtype, out, keepdims, initial, where])
np.swapaxes(axis1, axis2)
np.take(indices[, axis, out, mode])
np.tobytes([order])
np.tofile(fid[, sep, format])
np.tolist()
np.tostring([order])
np.trace([offset, axis1, axis2, dtype, out])
np.transpose(*axes)
np.var([axis, dtype, out, ddof, keepdims])
np.view([dtype][, type])
```

```python
np.zeros((3,4))
np.ones((2,3,4),dtype=np.int16)
d = np.arange(10,25,5)       
np.linspace(0,2,9)  
e = np.full((2,2),7)   
f = np.eye(2)
np.random.random((2,2))  
np.empty((3,2))   
```
