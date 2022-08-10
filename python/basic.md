# Python Basics

## Functions
How to make a function

Basic Function
```python
  def say_hi():
    print("Hi")
  
  say_hi() # prints "Hi"
```

Having a parameter
```python
    def say_hi(name):
    print("Hi " + name)
  
  say_hi("James") # prints "Hi James"
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
    print(letter) # prints J a m e s
```

Using Lists
```python
  friend = ["James", "Bob", "Peter"]
  for friend in friends:
    print(friend) # prints James Bob Peter
```
Using Range
```python
  for index in range(5):
    print(index) # prints 0 1 2 3 4
    
  for index in range(3,5):
    print(index) # prints 3 4
    
  friend = ["James", "Bob", "Peter"]
  for index range((len(friends))):
    print(friends[index]) # prints James Bob Peter
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

## Reading Files
```python
open("nameOfTheFile.txt", "r") # r means to read
open("nameOfTheFile.txt", "w") # w means write and can change
open("nameOfTheFile.txt", "a") # a means append, cannot change but can add
open("nameOfTheFile.txt", "r+") # r+ means read and write
```
```python
employee_file = open("employees.txt", "r")
  print(employee_file.readable()) # will print True b/c is on "r"
  print(employee_file.readline()) # reads the first line
  print(employee_file.readline()) # reads the second line
  
  print(employee_file.readlines()) # takes all the line and put them in an array
  print(employee_file.readlines()[1]) # prints the second line/element
  
  print(employee_file.read()) # prints all the texts
  
employee_file.close()
```
```python
employee_file = open("employees.txt", "r")
for employee in employee_file.readlines():
  print(employee)
employee_file.close()
```
## Writing to Files
```python
  employee_file = open("employees.txt", "a") // use "a" to append
  employee_file.write("James - Developer") // appends to the file
   employee_file.write("\nJames - Software Engineer") // appends to the file with a new line
  employee_file.close()
```

## Modules & Pip
```python
import name_of_pythonfile
# now I can use the functions from the imported python file
```
How to use Modules made by 3rd party
```python
# pip install nameofthepymodule
# now use import ~~
```
## Classes & Objects
profile.py
```python
class Student:
  
  def __init__(self, name, major, gpa, is_on_probation):
    self.name = name
    self.major = major
    self.gpa = gpa
    self.is_on_probation = is_on_probation 
```
Using Student Class
```python
from profile import Student

student1 = Student("James", "Computer Science", 4.0, False) // Creating a student object

print(student1.name) # prints James
print(student1.gpa) # prints 4.0
```
## Inheritance
```python
# chef.py
from Chef import Chef
class Chef(nameofclass): # inherits the class nameofclass, which means class Chef can use all the functions in nameofclass

# now we can override the function to change its role
```
## Python Interpreter
On the Terminal
```terminal
asdas
```
