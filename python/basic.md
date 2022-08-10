# Python Basics

## Functions
How to make a function

Basic Function
```python
  def say_hi():
    print("Hi")
  
  say_hi()
<!--  prints "Hi"  -->
```

Having a parameter
```python
    def say_hi(name):
    print("Hi " + name)
  
  say_hi("James")
<!--  prints "Hi James"  -->
```

## If Statement

```python
is_male = True
  if is_male:
    print("You are a male")
  else:
    print("You are not a male")
```
```python
  if ~~ and ~~:
    return ~~
  elif ~~ and ~~:
    return ~~
   else:
    return ~~
```

## User input
```python
  name = input("Enter your name: ")
  age = int(input("Enter your name: "))
  number = float(input("Enter a number: "))
```

## While Loop
```python
  i = 1
  while i <= 10:
    print(i)
    i += 1
```

## For Loop
Basic For Loops
```python
  for letter in "James":
    print(letter) => prints J a m e s
```

Using Lists
```python
  friend = ["James", "Bob", "Peter"]
  for friend in friends:
    print(friend) => prints James Bob Peter
```
Using Range
```python
  for index in range(5):
    print(index) => prints 0 1 2 3 4
    
  for index in range(3,5):
    print(index) => prints 3 4
    
  friend = ["James", "Bob", "Peter"]
  for index range((len(friends))):
    print(friends[index]) => prints James Bob Peter
```

## Try Except
```python
try:
    number = int(input("Enter a number: "))
    print(number)
except:
    print("Invalid Input")
    
  # If the input is a letter of alphabets, except block will be executed because it needs to be a integer number
```

