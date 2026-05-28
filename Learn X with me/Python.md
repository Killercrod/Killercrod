** Python
In this markdown we are going to talk about the basics of Python and how to use it to start building simple programs.

By the end of this guide you will be able to:
- Understand what Python is used for
- Read the basic structure of a Python program
- Practice the first things you should learn before moving on

This guide is for people who are new to Python, or for people who want a simple refresher without too much technical language.

First, we need to understand when we use Python. We use Python when we want to build scripts, automate small tasks, work with data, create simple apps, or learn programming in a simple way. It is a good idea to learn it step by step and keep things organized.

## Before You Start

You do not need to know everything before learning Python. It is enough to:

- Know how to read simple code
- Understand basic logic like "if this, then that"
- Be comfortable with practice and repetition
- Not be afraid of mistakes, because they are part of learning

## Basic Structure

This is the basic structure of a simple Python program. It is important to know why it is written like this.

```python
# Hello World
print("Hello, World!")

# Comments
# Single-line comment
"""Multi-line comment or docstring"""
```

I will explain why it is written like this and why it is important to know this.

** print("Hello, World!")
This prints text on the screen.
Why is it necessary? It is the simplest way to see output and test that your program works.

** Comments
Comments help you write notes inside your code.
Why are they useful? They make code easier to understand when you come back later.

## Variables, Data Types, and Operators in Simple Words

A variable is like a labeled box. You put something inside it so you can use it later.

The data type tells Python what kind of thing is inside the box. For example, a number, a decimal, text, or a true/false value.

Operators are the symbols that help you work with those values. Some operators do math, some compare values, and some help you change a variable.

## Variables and Data Types

```python
# Variables
name = "Ana"
age = 20
height = 1.68
is_student = True

# Strings
message = "Hello"

# Numbers
integer_number = 10
decimal_number = 3.14

# Booleans
is_active = False
```

If you want a simple way to remember them:

- Text values are strings
- Whole numbers are integers
- Decimal numbers are floats
- True or false values are booleans

## Operators

If you want a simpler way to remember them:

- Arithmetic operators help you calculate things
- Comparison operators help you ask questions about values
- Logical operators help you combine conditions
- Assignment operators help you update variables

```python
# Arithmetic
result = 10 + 5   # +, -, *, /, %, **

# Assignment
x = 10
x += 2

# Comparison
is_equal = (a == b)   # ==, !=, <, >, <=, >=

# Logical
logic_result = (a > b) and (c < d)   # and, or, not

# Ternary
max_value = a if a > b else b
```

## Basic Structure of a Python File

Python does not need classes or a main method for every small script. A file can start very simply and still work.

```python
print("First line")
print("Second line")
```

If you want to organize bigger programs, you can use functions.

```python
def greet(name):
	print(f"Hello, {name}!")

greet("Ana")
```

## Functions

A function is a reusable piece of code. Instead of writing the same logic many times, you put it in one place and call it when you need it.

```python
def add(a, b):
	return a + b

result = add(3, 5)
print(result)
```

Why functions are useful:

- They keep code cleaner
- They help you reuse logic
- They make programs easier to read

## Control Flow

### Conditional Statements

```python
if condition:
	# code
elif another_condition:
	# code
else:
	# code
```

### Loops

```python
# for loop
for i in range(5):
	print(i)

# for loop with a list
names = ["Ana", "Luis", "Maria"]
for name in names:
	print(name)

# while loop
count = 0
while count < 3:
	print(count)
	count += 1
```

## Data Collections

Python uses simple structures to store multiple values.

### Lists

```python
fruits = ["apple", "banana", "orange"]
fruits.append("grape")
print(fruits)
```

### Tuples

```python
point = (10, 20)
print(point)
```

### Sets

```python
unique_numbers = {1, 2, 3}
unique_numbers.add(4)
print(unique_numbers)
```

### Dictionaries

```python
person = {
	"name": "Ana",
	"age": 20
}

print(person["name"])
```

### Lists and Tuples Compared Simply

- A list can change
- A tuple is usually kept the same
- Use a list when you need to add or remove items
- Use a tuple when the values should stay fixed

## Packages and Imports

Packages in Python are usually modules or folders that help you organize code. Imports let you use code from somewhere else.

```python
import math

print(math.sqrt(25))
```

You can also import only what you need.

```python
from math import sqrt

print(sqrt(25))
```

Why this matters:

- Imports keep code organized
- They let you reuse tools that already exist
- You usually see them at the top of a file

## Classes and Objects

Python also uses classes, but you do not need to start there right away.

Think of it like this:

- A class is the blueprint
- An object is the real thing created from that blueprint
- A method is something the object can do

```python
class Car:
	def __init__(self, brand, year):
		self.brand = brand
		self.year = year

	def start(self):
		print("Car started")


my_car = Car("Toyota", 2020)
my_car.start()
```

## Exceptions

Sometimes things go wrong, and Python gives you a way to handle that without breaking the whole program.

```python
try:
	result = 10 / 0
except ZeroDivisionError:
	print("Cannot divide by zero!")
finally:
	print("This always runs")
```

## Basic File I/O

Python can also read and write files.

```python
with open("file.txt", "w") as file:
	file.write("Hello World!")

with open("file.txt", "r") as file:
	content = file.read()
	print(content)
```

## Useful Methods

### String Methods

```python
text = "Hello World"

len(text)
text.lower()
text.upper()
text.strip()
text.split(" ")
text.replace("World", "Python")
```

### List Methods

```python
numbers = [1, 2, 3, 4, 5]

numbers.append(6)
numbers.remove(3)
numbers.sort()
numbers.copy()
```

### Math Examples

```python
import math

math.sqrt(25)
math.pow(2, 3)
math.floor(3.8)
math.ceil(3.2)
```

## Basic Exercises

1. Print your name on the screen.
Expected result: You should see your name in the console.

2. Create two variables and add them.
Expected result: You should see the sum printed on the screen.

3. Use an if statement to check if a number is positive.
Expected result: The program should tell you if the number is positive or not.

4. Create a list and print all its values.
Expected result: You should see every item printed one by one.

5. Create a simple import and use it in your program.
Expected result: Your code should run without saying the module cannot be found.

## Common Beginner Mistakes

- My program does not run.
Check if your indentation is correct.

- My function does not work.
Check if you wrote the function name correctly and called it the right way.

- My import is failing.
Check if the module name is correct.

- My output does not appear.
Check if you used print() correctly.

- My code gives an indentation error.
Check if the spaces or tabs are consistent.

## What to Learn Next

- Python syntax basics (practice with small programs)
- Functions and parameters in more depth
- Lists, tuples, sets, and dictionaries
- Object-oriented programming in Python
- File handling and exceptions
- Working with modules and packages

## Key Points to Remember

- Python is easy to read and write
- Indentation matters in Python
- Variables do not need explicit type declarations in most cases
- Functions help you reuse code
- Lists are very common for storing multiple values
- Imports help you organize and reuse code
- Mistakes are normal when learning, so keep practicing

This guide covers the essential Python concepts. Keep practicing and referring to the official Python documentation for more detailed information.
