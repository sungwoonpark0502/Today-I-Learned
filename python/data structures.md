# Data Structures

## Tuples
* Immutable (Cannot change any of the element once initialized)

How to create a tuple:
```python
  coordinates = (4, 5)
  # coordinates[0] = 10 is not allowed
  print(coordinates[0]) # prints 4
```
List of Tuples:
```python
  coord = [(1,2), (3,4), (4,5)]
```

## Lists
* Mutable (can change the elements)
```python
  coordinates = [4, 5]
  coordinates[0] = 10
  print(coordinates[0]) # prints 10 
```
2D Lists
```python
  number_grid = [
    [1,2,3],
    [4,5,6],
    [7,8,9],
    [0]
  ]
  print(number_grid[2][1]) # prints 8
```
```python
a = ["a", "b", "c"]

a.append("d") # a, b, c, d
a.insert(2, "z") # a, b, z, c, d
a.remove("a") # b, z, c, d
# sort function sorts the list into alphabetical order or in increasing order
# only use sort when the data types are same in the list
a.sort() # b, c, d, z

print(a[2:4]) # d, z
print(a[:3]) # b, c, d
print(a[-1]) # z
print("b" in a) # true
print("f" in a) # false
print(len(a)) # prints the length of the list, 4

# .pop(), .clear(), .count("anything")

```

## Dictionaries
* Key and Value
* Keys cannot be a duplicate, should be unique
* Keys cannot be changed

Creating a dictionary
```python
  # Jan is the Key and January is a value
  month = { "Jan": "January", "Feb": "February"}
  print(month["Jan"]) # January
  print(month.get("Feb")) # February
  print(month.get("Mar")) # None
  print(month.get("Mar", "Not a valid Key")) # Not a valid Key
  
  print(month.keys()) # prints the keys
  print(month.values()) # prints the values
  
  # adding an item into dictionary
  month["Mar"] = March
  # removing an item from dictionary
  del month["Mar"]
  
  # tuple can be the Key but list cannot because lists can be modified
  month[(1,2,3)] = "Tuple"
  
```
