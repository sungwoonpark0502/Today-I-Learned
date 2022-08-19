## Pandas

* Python Library
* For data manipulation and analysis
* Made out of NumPy

### Series Data

```python
import  pandas as pd

data = pd.Series([1,2,3,4])
print(data)
"""
0 1
1 2
2 3
3 4
dtype: int64
"""

# Series has the values as ndarray
print(type(data)) # <class 'pandas.core.series.Series'>
print(data.values) # [1 2 3 4]
print(type(data.values)) # <class 'numpy.ndarray'>
```
Chaning the dtype
```python
data = pd.Series([1,2,3,4], dtype = "float")
print(data.type) # float64
```
Assigning Index and Accessing the values using Index
```python
data = pd.Series([1,2,3,4], index = ['a', 'b','c','d'])
data['c'] = 5
"""
a 1
b 2
c 5
d 4
dtype: int64
"""
```
