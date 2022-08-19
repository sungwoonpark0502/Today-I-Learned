# Pandas

* Python Library
* For data manipulation and analysis
* Made out of NumPy

## Series Data

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
Can generate Series using Dictionary
```python
pop_dict = {'china': 141500, 'japan': 12718, 'korea': 5180}
population = pd.Series(pop_dict)
"""
china 141500
japan 12718
korea 5180
dtype: int64
"""
```
## DataFrame
* Many Series are combined to make DataFrame with rows and columns

* Using many series to make a DataFrame
```python
# Dictionary for population
pop_dict = {'china': 141500, 'japan': 12718, 'korea': 5180}
population = pd.Series(pop_dict)
# Dictionary for GDP
gdp_dict = {'china': 1, 'japan': 2, 'korea': 3}
gdp = pd.Series(gdp_dict)

# DataFrame
country = pd.DataFrame({'gdp': gdp, 'population': population})
"""
      gdp     population
china   1       141500
japan   2       12718
korea   3       5180
"""
```
* Some methods
```python
print(country.shape) # (3,3)
print(country.size) # 8
print(country.ndim) # 2
print(country.values) """
                        [[1 141500]
                         [2 12718]
                         [3 5180]]
                      """
```
* Assigning name to index and column
```python
country.index.name = "Country"
country.columns.name = "Info"

print(country.index) # Index(['china','japan','korea'], dtype='object', name='Country')
print(country.columns) # Index(['gdp','population'], dtype='object', name='Info')
```
* Saving and Bring the DataFrame
```python
#saving
country.to_csv("./country.csv")
country.to_excel("country.xlsx")

# bringing
country = pd.read_csv("./country.csv")
country = pd.read_excel("country.xlsx")
```

* Using Dictionary to make DataFrame
```python
data = {'Name': ['A', 'B', 'C']}, 'age': [1, 2, 3], 'school': ['a', 'b', 'c']
person = pd.DataFrame(data)
person = person.set_index('person')
"""
person
---------------
A     1     a
B     2     b
C     3     c
"""
```
## Selecting/Chaning Data in DataFrame
Two ways to find data:
1. loc (often used)
2. iloc
```python
country.loc['china'] # indexing
country.loc['japan':'korea', 'population'] # slicing

```
Result of indexing from the code above
* The numbers on the right are the gdp, which has been substitued by 1,2,3 in my case
![Indexing](https://user-images.githubusercontent.com/93812258/185689316-ba95131c-f031-4cee-b289-214a3625ac2d.png)

Result of slicing from the code above
![Slicing](https://user-images.githubusercontent.com/93812258/185689516-8e679f25-c953-4743-93b3-8b501acc7985.png)
```python
country.iloc[0] # indexing
country.iloc[1:3, :2] # slicing

# result of the indexing and slicing is the same as the images above
```
Using the name of the COlumn to get Data
```python
country # Image A
country['gdp'] # Image B
country[['gdp']] # Image C
```
Image C
![Image C](https://user-images.githubusercontent.com/93812258/185690605-274a581f-e3c1-442b-9e81-907267bf2812.png)
Image B
![Image A](https://user-images.githubusercontent.com/93812258/185690418-b7d87fd2-ef2c-4288-85e9-fb3c57a0f9ea.png)
Image C
![Image B](https://user-images.githubusercontent.com/93812258/185690447-46ceaf0e-0cd2-4cfc-afff-d7fdafb341f7.png)

Using Masking and Query Function
```python
country[country['population'] < 10000] # using masking
country.query("population > 10000") # using query function
```
![Image](https://user-images.githubusercontent.com/93812258/185691069-a14ffd3b-f322-48dc-ac8e-8aecf9982398.png)

Can use Series like a operator like numpy array
```python
gdp_per_capita = country['gdp'] / country['population']
country['gdp_per_capita'] = gdp_per_capita
```
Result from the above code
![result](https://user-images.githubusercontent.com/93812258/185693821-8c02d185-4e42-49fc-abda-73249e9fcf50.png)

Adding new Data to DataFrame
![Image](https://user-images.githubusercontent.com/93812258/185694864-264cd45d-f336-46c5-bcba-84d90de40fef.png)
Adding New Column
![a](https://user-images.githubusercontent.com/93812258/185695165-7627ca33-1d8b-4fb9-a0ba-5452b2d536ae.png)
