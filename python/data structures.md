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

## Dictionaries
* Key and Value
* Keys cannot be a duplicate, should be unique

Creating a dictionary
```python
  monthConversions = {
    "Jan": "January",
    "Feb": "February"
   # Jan is the Key and January is a value
  }
  print(monthConversions["Jan"]) # January
  print(monthConversions.get("Feb")) # February
  print(monthConversions.get("Mar")) # None
  print(monthConversions.get("Mar", "Not a valid Key")) # Not a valid Key

```
