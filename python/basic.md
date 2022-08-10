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
    print(letter) => "prints J a m e s"
```

Using Lists
```python
  friend = ["James", "Bob", "Peter"]
  for friend in friends:
    print(friend) => "prints James Bob Peter"
```
```python
  for index in range(5):
    print(index) => prints 0 1 2 3 4
```
