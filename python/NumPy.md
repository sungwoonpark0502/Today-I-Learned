## NumPy

* Numerical Python
* a library for the Python programming language, adding support for large, __multi-dimensional arrays__ and matrices, along with a large collection of high-level mathematical functions to operate on these arrays
* Most of the datas could be seen as array of numbers
* Fast calculation and low memory compared to python lists

Using NumPy
```python
import numpy as np

npArr = np.array(range(5))
print(npArr) # [1 2 3 4 5] no commas
print(type(npArr)) # <class 'numpy.ndarray'> # ndarray: nth dimensional array
```
* Can store only one type of variables in the array
```python
arr = np.array([0, 1, 2, 3, 4], dtype=float)
print(arr) # [0. 1. 2. 3. 4.] # in float
print(arr.dtype) # float64, returns the dtype of arr
print(arr.astype(int)) # [0 1 2 3 4], changing the dtype
```

dytpe:
* int: i, int_, int32, int64, i8
* float: f, float_ float32, float64, f8
* str: str, U, U32
* bool: ?, bool_

__ndarray__

One Dimension
```python
list = [0,1,2,3]
arr = np.array(list)
print(arr.ndim) # 1
print(arr.shape) # (4,)
```

Two Dimension
```python
list = [[0,1,2],[3,4,5]]
arr = np.array(list)
print(arr.ndim) # 2
print(arr.shape) # (2,3) 2 row and 3 column
```

```python
arr = np.array([0,1,2,3,4,5])
print("arr.shape : {}".format(arr.shape)) # arr.shape : (6,)
print("Size : {}".format(arr.size)) # Size : 6
print("Length : {}".format(len(arr))) # Length : 6

```
