# Python

# Index

1. [File extension](#file-extension-py)
2. [Suggested IDE](#suggested-ide-pycharm)
3. [Hello World](#hello-world-example)
4. [Creating variables](#creating-variables)
5. [Data types](#data-types)
6. [Comments in python](#comments)
7. [Boolean values](#boolean-values)
8. [Dynamically Typed Language](#dynamically-typed-language)
9. [Multiline strings](#multiline-strings)
10. [Indentation](#indentation)
11. [Arithmetic operators](#arithmetic-operators)
12. [Comparison operators](#comparison-operators)
13. [Logical operators](#logical-operators) 
14. [Assignment operators](#assignment-operators)
15. [If statements](#if-statements)
16. [Lists](#lists)
17. [Sets](#sets)
18. [Union, Intersection, Difference with Sets](#union-intersection-difference-with-sets)
19. [Dictionaries](#dictionaries)
20. [For loops](#for-loops)
21. [While loop](#while-loop)
22. [Functions](#functions)
23. [Built in functions and import statements](#built-in-functions-and-import-statements)
24. [Creating modules](#creating-modules)
25. [Classes and Objects](#classes-and-objects)
26. [Printing Objects](#printing-objects)
27. [Working with Dates](#working-with-dates)
28. [Creating Files](#creating-files)
29. [Reading Files](#reading-files)
30. [Fetching data from internet](#fetching-data-from-internet)
31. [Pip and modules](#pip-and-modules)
## File extension: **.py**

## Suggested IDE: **PyCharm**

## Hello World example
```python
print("Hello World")
```

## Creating variables:
Python is a **dinamically type lanaguage**.  
This means that a variable that contains an integer, can contain a string in further instructions.
```python
x = "Pippo"
x = [1, 2, 3, 4]
age = 30
pi = 3.14
name, age = "Giuseppe", 21 #Inline initialization of variables
```

## Basic Data types:
```python
brand = "Mirtino"
age = 2
pi = 3.14
numbers = [1, 2, 3, 4]
isBaby = True
print(type(brand)) # <class 'str'>
print(type(age)) # <class 'int'>
print(type(pi)) # <class 'float'>
print(type(numbers)) # <class 'list'>
print(type(isBaby)) # <class 'bool'>
```

## Comments:
Comments start with the symbol **#**
```python
# This is a comment
"""
I'm a multiline comment
""" 
```

## Boolean values:
The boolean values are written with capital letter in upperCase.
```python
True
False
```

## Dynamically Typed Language:
Python is a **Dynamically Typed Language** so i can declare variables without specifying the type.  
However we can also specify a type for our variables.
```python
name: str = "Giuseppe"
isAdult: bool = True 
def hello() -> str:
    return "hello"
```
N.B. It's not common to put the type for variables. 

## Multiline strings:
I use the same three quotes used for multiline comments
```python
multilineString = """
This is a multiline string.
Essentially a string on multiple lines.
"""
print(multilineString)
```
We can also do more complicated things like passing dynamic parameters:
```python
name = "Pippo"
email = f"""
Hi {name}
If you received this email, 
then you joined our community.
Congrats!!
"""
print(email)
```
N.B. The f before the quotes is not an error but it's mandatory.

## Indentation:
In python there are no parenthesis so the indentation is essential.  
Indentation is used when code has to be wrapped inside statements like  
functions, if, for loop, ect...  

## Arithmetic operators:
The arithmetic operators are:
1. +
2. -
3. *
4. ** (power operation)
5. /
6. %
7. **
```python
print(1 + 2)
print(2 * 2)
print(2 ** 5) # Power operation
print(10 / 5)
print(10 % 5)
```

## Comparison operators:
1. >
2. <
3. >=
4. <=
5. ==
6. !=
```python
print(10 > 5)
print(5 < 10)
print(10 >= 5)
print(10 <= 5)
print(10 == 10)
print(10 != 5)
```

## Logical operators: 
1. and
2. or
3. not
```python
print((10 > 5) and not (5 < 10))
```

## Assignment operators:
1. =
2. +=
3. -=
4. *=
5. /=
6. **= (power operation)

## If statements:
```python
number = 0
if number > 0:
    print("Number positive")
elif number == 0:
    print("Number is zero")
else:
    print("Number negative")
```

### Ternary if statement:
```python
number = 10
message = "number positive" if number > 0 else "number 0 or negative"
print(message)
```

## Lists:
The lists in python are collection of elements of different types.
```python
numbers = [1, 2, 3, 4, "Pippo", "Pluto", 3.4, True]
newList = [(1, 2), (3, 4), ("Pippo", "Pluto")]

print(numbers)
print(numbers[0])
```

## Sets:
Sets are **similar to lists** but duplicates are not allowed.  
This means that if there are duplicates, it will count only one of them whil the others will be ignored.
```python
numberSet = {1, 1, 1}
print(numberSet)
```
N.B. Order is not allowed inside sets

### Union, Intersection, Difference with Sets:
These are the operation same as in math studied at the college.
- **Union:**
```python
letterSetA = {"A", "B", "C", "D"}
letterSetB = {"E", "F"}
union = letterSetA | letterSetB
print(union)
```
- **Intersection:**
```python
letterSetA = {"A", "B", "C", "D"}
letterSetB = {"E", "F"}
intersection = letterSetA & letterSetB # in this case is empty set
print("Intersection: ", intersection)
```
- **Difference:**
```python
letterSetA = {"A", "B", "C", "D"}
letterSetB = {"E", "F", "C", "D"}
difference = letterSetA - letterSetB
print(f"Difference {difference}")
```

## Dictionaries: 
It's a data structure that allow us to store **<Key,Value> pairs**.  
It's essentially like a map or more easily it can be seen ad a JSON.  
To access to the values, it's used the square notation specifying the key. 
```python
person = {
    "name": "Pippo",
    "surname": "Pluto",
    "age": 20
}
print(person["name"]) #Square notation to specify the value of the key we want
person["age"] = 30
print(person)
```

## For loops:
```python
names = ["Pippo", "Pluto", "Paperino"]
for name in names:
    print(name)
```

## While loop:
While loop has a new statement which is else.  
The else is been executed once the condition is not true.
```python
number = 0
while number < 10:
    print(number)
    number +=1
else:
    print("While loop ended")
```

## Functions:
```python
def greet(name = "Pippo"):
    print(f"Hello {name}")

greet("Giuseppe")

def isAdult(age):
    if age >= 18:
        return True
    else:
        return False


adult = isAdult(10)
print(adult)

```

## Built in functions and import statements:
There are two ways to import modules:  
1. Import the whole module
```python
import math
actualPi = math.pi
print(actualPi)
```
2. Import only the things we need
```python
from math import isqrt
print(isqrt(25))
```

## Creating modules:
Just create a new .py file.  
Once written the code, we can import the file into another file

1. Module **calculator.py**
```python
def add(n1, n2):
    return n1 + n2


def subtract(n1, n2):
    return n1 - n2


def divide(n1, n2):
    return n1 / n2


def multiply(n1, n2):
    return n1 * n2

```
2. Module **main.py**
```python
import calculator

print(calculator.add(2,3))
print(calculator.subtract(2,3))
print(calculator.divide(6,3))
print(calculator.multiply(2,3))
```

## Classes and Objects:
```python
class Phone:
    # Constructor of the class
    def __init__(self, brand, price):
        # Attributes
        self.brand = brand
        self.price = price

    def call(self, phone_number):
        print(f"{self.brand} is calling {phone_number}")


# Create the object
iphone = Phone("Iphone 14", 1400)
samsung = Phone("S21", 1200)

print(iphone.brand)
print(iphone.price)
iphone.call("123456")
```
#### **N.B.**
- **Constructor:**  
Always starts with __init__ and the first parameter has to be **self**
- **Methods:**  
The first parameter is always self but when calling the method it's ignored 

## Printing Objects:
For printing objects it is used a toString method just like in Java programming.  
The method is called **__str__**  
```python
class Phone:
    # Constructor of the class
    def __init__(self, brand, price):
        # Attributes
        self.brand = brand
        self.price = price

    def call(self, phone_number):
        print(f"{self.brand} is calling {phone_number}")

    def __str__(self) -> str:
        return f"Brand: {self.brand} Price: {self.price}"


# Create the object
iphone = Phone("Iphone 14", 1400)
samsung = Phone("S21", 1200)
print(iphone)
print(samsung)
```
N.B. If we don't override the methods __str__ then will be printed the  
memory index of the object.

## Working with Dates:
We have to use and import the **datetime** module.  
```python
import datetime
print(datetime.date.today())
print(datetime.datetime.now().day)
print(datetime.datetime.now().now().month)
print(datetime.datetime.now().now().year)
```
### Formatting Dates:
Here's an example for formatting dates:
```python
import datetime
now = datetime.datetime.now()
print(now)

nowFormatted = now.strftime("%d/%m/%Y %H:%M:%S")
print(nowFormatted)
```

## Creating Files:
- r -> Read
- w -> Write (also create)
- r+ -> Read and Write
- a -> Append

```python
file = open("./data.csv", "r+")
file.write("id,name,email\n")
file.write("1,Pippo,pippo@gmail.com\n")
file.write("2,Pluto,pluto@gmail.com\n")
file.close()
```

## Reading Files:
```python
file = open("./data.csv", "r+")
print(file.read())
file.close()
```
Or we can do in this way:
```python
file = open("./data.csv", "r+")
for line in file:
    print(line)
file.close()
```

There is also a better way to work with files. Here's how:  
In this way we don't need to close the file explicitly
```python
import os.path

filename = "./data.csv"
if os.path.isfile(filename):
    with open("./data.csv", "r") as file:
        print(file.read())
else:
    print("File does not exist")
```

## Fetching data from internet:
We use the **urllib module** for fetching data on the internet.
```python
from urllib import request

r = request.urlopen("http://www.google.com")
# Get the status code from the request
print(r.getcode())
# Read the entire html of the website
print(r.read())
```

### Calling an API and read the JSON response:
```python
from urllib import request
import json

class Joke:

    def __init__(self, setup, punchline) -> None:
        self.setup = setup
        self.punchline = punchline

    def __str__(self) -> str:
        return f"setup: {self.setup} punchline: " \
               f"{self.punchline}"



tenJokesUrl = "http://official-joke-api.appspot.com/random_ten"

r = request.urlopen(tenJokesUrl)
data = r.read()
jokesRawData = json.loads(data)
print(jokesRawData)
print("One joke per time")

jokes = []

for j in jokesRawData:
    setup = j["setup"]
    punchline = j["punchline"]
    joke = Joke(setup, punchline)
    jokes.append(joke)

print(len(jokes))

for i in jokes:
    print(i)
```

## Pip and modules:
Pip is the package manager for installing python packages.  
It's useful because there are lots of library that helps programming and simplify the job.  

- Installing a new module:
```
pip3 install <module_name>
```