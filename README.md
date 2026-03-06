# learn-python
Here is a **complete Python roadmap from beginner to advanced**, with **clear code**, **core concepts**, and **real project ideas**.

I will teach it in a practical order, like this:

1. Python basics
2. Control flow
3. Functions
4. Data structures
5. OOP
6. Files
7. Error handling
8. Modules and packages
9. Advanced Python
10. Real projects
11. Best practices
12. Full learning roadmap

---

# 1. What is Python?

Python is a **high-level, easy-to-read, general-purpose programming language**.

You can use Python for:

* web development
* automation
* scripting
* data analysis
* AI / machine learning
* cybersecurity tools
* desktop apps
* APIs
* web scraping

Example:

```python
print("Hello, World!")
```

Output:

```python
Hello, World!
```

---

# 2. Installing Python

You need:

* Python 3
* a code editor like VS Code
* terminal / command prompt

Check installation:

```bash
python --version
```

or

```bash
python3 --version
```

Run a file:

```bash
python app.py
```

---

# 3. Python Syntax Basics

Python uses **indentation** instead of `{}`.

Example:

```python
age = 18

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

---

# 4. Variables and Data Types

Python is dynamically typed.

```python
name = "Seyam"
age = 18
height = 5.8
is_student = True
```

## Main data types

```python
text = "Hello"      # str
num = 10            # int
price = 99.99       # float
ok = True           # bool
nothing = None      # NoneType
```

Check type:

```python
print(type(text))
print(type(num))
```

---

# 5. Input and Output

```python
name = input("Enter your name: ")
print("Hello,", name)
```

Numeric input:

```python
age = int(input("Enter age: "))
print(age + 5)
```

Why `int()`?

Because `input()` always returns a string.

---

# 6. Operators

## Arithmetic

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

## Comparison

```python
print(10 > 5)    # True
print(10 == 10)  # True
print(10 != 5)   # True
```

## Logical

```python
x = True
y = False

print(x and y)
print(x or y)
print(not x)
```

## Assignment

```python
x = 5
x += 2
x *= 3
print(x)
```

---

# 7. Strings in Python

```python
text = "Python"
```

## Access characters

```python
print(text[0])   # P
print(text[-1])  # n
```

## Slicing

```python
print(text[0:3])   # Pyt
print(text[2:])    # thon
print(text[:4])    # Pyth
```

## Common string methods

```python
msg = " hello world "

print(msg.upper())        # HELLO WORLD
print(msg.lower())        # hello world
print(msg.strip())        # remove spaces
print(msg.replace("world", "Python"))
print(msg.split())
```

## f-string

Best way to format:

```python
name = "Seyam"
age = 18

print(f"My name is {name} and I am {age} years old.")
```

---

# 8. Type Conversion

```python
x = "100"
y = int(x)
print(y + 50)
```

More:

```python
print(float("3.14"))
print(str(123))
print(bool(1))
print(bool(0))
```

---

# 9. Conditional Statements

## if

```python
age = 20

if age >= 18:
    print("Adult")
```

## if-else

```python
num = 7

if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

## if-elif-else

```python
marks = 85

if marks >= 80:
    print("A+")
elif marks >= 70:
    print("A")
elif marks >= 60:
    print("A-")
else:
    print("Below A-")
```

---

# 10. Loops

## for loop

```python
for i in range(5):
    print(i)
```

Output:

```python
0
1
2
3
4
```

## while loop

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

## break

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

## continue

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

---

# 11. Functions

Functions help reuse code.

## Basic function

```python
def greet():
    print("Hello!")
    
greet()
```

## Function with parameters

```python
def greet(name):
    print(f"Hello, {name}")

greet("Seyam")
```

## Return value

```python
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

## Default parameter

```python
def welcome(name="Guest"):
    print(f"Welcome, {name}")

welcome()
welcome("Seyam")
```

## Keyword arguments

```python
def student(name, age):
    print(name, age)

student(age=18, name="Seyam")
```

## Variable number of arguments

```python
def total(*numbers):
    return sum(numbers)

print(total(1, 2, 3, 4))
```

## `**kwargs`

```python
def show_info(**info):
    for key, value in info.items():
        print(key, value)

show_info(name="Seyam", age=18)
```

---

# 12. Scope

```python
x = 100  # global

def test():
    y = 50   # local
    print(x)
    print(y)

test()
```

---

# 13. Lists

A list stores multiple values.

```python
fruits = ["apple", "banana", "mango"]
```

## Access

```python
print(fruits[0])
print(fruits[-1])
```

## Modify

```python
fruits[1] = "orange"
print(fruits)
```

## Methods

```python
nums = [1, 2, 3]
nums.append(4)
nums.insert(1, 100)
nums.remove(2)
nums.pop()
nums.sort()
nums.reverse()

print(nums)
```

## Loop through list

```python
for item in fruits:
    print(item)
```

## List comprehension

```python
squares = [x * x for x in range(1, 6)]
print(squares)
```

---

# 14. Tuples

Tuple is ordered but immutable.

```python
point = (10, 20)
print(point[0])
```

Why use tuple?

* fixed data
* safer than list
* faster in some cases

---

# 15. Sets

Set stores unique values.

```python
nums = {1, 2, 3, 3, 4}
print(nums)
```

## Methods

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a.union(b))
print(a.intersection(b))
print(a.difference(b))
```

Useful for removing duplicates:

```python
data = [1, 2, 2, 3, 4, 4]
unique = list(set(data))
print(unique)
```

---

# 16. Dictionaries

Dictionary stores key-value pairs.

```python
student = {
    "name": "Seyam",
    "age": 18,
    "dept": "CSE"
}
```

## Access

```python
print(student["name"])
print(student.get("age"))
```

## Add / update

```python
student["age"] = 19
student["email"] = "abc@gmail.com"
```

## Loop

```python
for key, value in student.items():
    print(key, value)
```

---

# 17. Nested Data Structures

```python
students = [
    {"name": "A", "marks": 80},
    {"name": "B", "marks": 90}
]

for s in students:
    print(s["name"], s["marks"])
```

This is very common in real projects.

---

# 18. Object-Oriented Programming (OOP)

OOP is used to model real-world things.

## Class and object

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def show(self):
        print(f"Name: {self.name}, Age: {self.age}")

s1 = Student("Seyam", 18)
s1.show()
```

## Meaning of `self`

`self` refers to the current object.

---

## Inheritance

```python
class Person:
    def __init__(self, name):
        self.name = name

    def show_name(self):
        print(self.name)

class Student(Person):
    def study(self):
        print("Studying...")

s = Student("Seyam")
s.show_name()
s.study()
```

## Polymorphism

```python
class Bird:
    def sound(self):
        print("Some sound")

class Duck(Bird):
    def sound(self):
        print("Quack")

class Cat(Bird):
    def sound(self):
        print("Meow")

animals = [Duck(), Cat()]
for a in animals:
    a.sound()
```

## Encapsulation

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

acc = BankAccount(1000)
acc.deposit(500)
print(acc.get_balance())
```

---

# 19. File Handling

## Write file

```python
with open("data.txt", "w") as file:
    file.write("Hello Python")
```

## Read file

```python
with open("data.txt", "r") as file:
    content = file.read()
    print(content)
```

## Append file

```python
with open("data.txt", "a") as file:
    file.write("\nNew line")
```

Why `with open()`?

Because it automatically closes the file.

---

# 20. Exception Handling

Errors happen. Handle them safely.

```python
try:
    num = int(input("Enter a number: "))
    print(10 / num)
except ValueError:
    print("Invalid number")
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Done")
```

---

# 21. Modules

A module is a Python file.

## Example: `math_utils.py`

```python
def add(a, b):
    return a + b
```

## Another file

```python
import math_utils

print(math_utils.add(2, 3))
```

## Import specific function

```python
from math import sqrt
print(sqrt(25))
```

## Alias

```python
import math as m
print(m.pi)
```

---

# 22. Useful Built-in Functions

```python
nums = [1, 2, 3, 4]

print(len(nums))
print(sum(nums))
print(max(nums))
print(min(nums))
print(sorted(nums, reverse=True))
```

More:

```python
for i, value in enumerate(["a", "b", "c"]):
    print(i, value)

names = ["A", "B", "C"]
marks = [80, 90, 85]

for n, m in zip(names, marks):
    print(n, m)
```

---

# 23. Lambda, map, filter

## lambda

```python
square = lambda x: x * x
print(square(5))
```

## map

```python
nums = [1, 2, 3]
result = list(map(lambda x: x * 2, nums))
print(result)
```

## filter

```python
nums = [1, 2, 3, 4, 5, 6]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)
```

In real code, list comprehensions are often cleaner.

---

# 24. Python Packages

A package is a folder of modules.

Example:

```python
myapp/
    main.py
    utils/
        __init__.py
        helper.py
```

Import:

```python
from utils.helper import some_function
```

---

# 25. Virtual Environment

Used to isolate project dependencies.

Create:

```bash
python -m venv venv
```

Activate on Linux/macOS:

```bash
source venv/bin/activate
```

Activate on Windows:

```bash
venv\Scripts\activate
```

Install package:

```bash
pip install requests
```

Save dependencies:

```bash
pip freeze > requirements.txt
```

Install from file:

```bash
pip install -r requirements.txt
```

---

# 26. Working with External Libraries

Example: `requests`

```python
import requests

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
print(response.status_code)
print(response.json())
```

---

# 27. JSON in Python

Very important for APIs.

```python
import json

data = {
    "name": "Seyam",
    "age": 18
}

json_string = json.dumps(data)
print(json_string)
```

Parse JSON:

```python
text = '{"name": "Seyam", "age": 18}'
obj = json.loads(text)
print(obj["name"])
```

---

# 28. Date and Time

```python
from datetime import datetime

now = datetime.now()
print(now)
print(now.year)
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

---

# 29. Python Advanced Concepts

## 1. List, set, dict comprehensions

```python
nums = [1, 2, 3, 4]

squares = [x*x for x in nums]
evens = {x for x in nums if x % 2 == 0}
mapping = {x: x*x for x in nums}

print(squares)
print(evens)
print(mapping)
```

## 2. Iterators

```python
nums = [1, 2, 3]
it = iter(nums)

print(next(it))
print(next(it))
```

## 3. Generators

Generators save memory.

```python
def count_up_to(n):
    i = 1
    while i <= n:
        yield i
        i += 1

for num in count_up_to(5):
    print(num)
```

## 4. Decorators

A decorator modifies a function.

```python
def logger(func):
    def wrapper():
        print("Function started")
        func()
        print("Function ended")
    return wrapper

@logger
def say_hello():
    print("Hello")

say_hello()
```

## 5. `*args` and `**kwargs`

Already discussed, but used heavily in advanced code.

## 6. `__name__ == "__main__"`

```python
def main():
    print("Program running")

if __name__ == "__main__":
    main()
```

Why?

It ensures code runs only when the file is executed directly.

---

# 30. Important Python Style Rules

Use:

* meaningful variable names
* small functions
* comments only where needed
* `snake_case` for variables and functions
* `PascalCase` for classes
* constants in uppercase

Example:

```python
MAX_USERS = 100

def calculate_total(price, quantity):
    return price * quantity

class UserProfile:
    pass
```

---

# 31. Real Project 1 — Calculator

A beginner console project.

```python
def add(a, b):
    return a + b

def sub(a, b):
    return a - b

def mul(a, b):
    return a * b

def div(a, b):
    if b == 0:
        return "Cannot divide by zero"
    return a / b

print("1. Add")
print("2. Subtract")
print("3. Multiply")
print("4. Divide")

choice = input("Choose (1/2/3/4): ")
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

if choice == "1":
    print("Result:", add(a, b))
elif choice == "2":
    print("Result:", sub(a, b))
elif choice == "3":
    print("Result:", mul(a, b))
elif choice == "4":
    print("Result:", div(a, b))
else:
    print("Invalid choice")
```

## Concepts used

* functions
* input/output
* conditionals
* error thinking

---

# 32. Real Project 2 — To-Do List App (Console)

```python
tasks = []

while True:
    print("\n1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        task = input("Enter task: ")
        tasks.append(task)
        print("Task added.")

    elif choice == "2":
        if not tasks:
            print("No tasks available.")
        else:
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")

    elif choice == "3":
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")
        index = int(input("Enter task number to delete: ")) - 1
        if 0 <= index < len(tasks):
            removed = tasks.pop(index)
            print(f"Deleted: {removed}")
        else:
            print("Invalid task number.")

    elif choice == "4":
        print("Goodbye!")
        break

    else:
        print("Invalid choice.")
```

## Better version with file storage

```python
import json
import os

FILE_NAME = "tasks.json"

def load_tasks():
    if os.path.exists(FILE_NAME):
        with open(FILE_NAME, "r") as f:
            return json.load(f)
    return []

def save_tasks(tasks):
    with open(FILE_NAME, "w") as f:
        json.dump(tasks, f)

tasks = load_tasks()

while True:
    print("\n1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        task = input("Enter task: ")
        tasks.append(task)
        save_tasks(tasks)
        print("Task saved.")

    elif choice == "2":
        if not tasks:
            print("No tasks.")
        else:
            for i, task in enumerate(tasks, start=1):
                print(f"{i}. {task}")

    elif choice == "3":
        for i, task in enumerate(tasks, start=1):
            print(f"{i}. {task}")
        try:
            index = int(input("Enter task number: ")) - 1
            removed = tasks.pop(index)
            save_tasks(tasks)
            print(f"Deleted: {removed}")
        except (ValueError, IndexError):
            print("Invalid input.")

    elif choice == "4":
        break

    else:
        print("Invalid choice.")
```

## Concepts used

* lists
* file handling
* JSON
* exceptions
* modular thinking

---

# 33. Real Project 3 — Student Management System

```python
students = []

def add_student():
    name = input("Enter name: ")
    roll = input("Enter roll: ")
    dept = input("Enter dept: ")

    student = {
        "name": name,
        "roll": roll,
        "dept": dept
    }

    students.append(student)
    print("Student added.")

def show_students():
    if not students:
        print("No students found.")
        return

    for s in students:
        print(f"Name: {s['name']}, Roll: {s['roll']}, Dept: {s['dept']}")

def search_student():
    roll = input("Enter roll to search: ")
    for s in students:
        if s["roll"] == roll:
            print("Found:", s)
            return
    print("Not found.")

while True:
    print("\n1. Add Student")
    print("2. Show Students")
    print("3. Search Student")
    print("4. Exit")

    choice = input("Choice: ")

    if choice == "1":
        add_student()
    elif choice == "2":
        show_students()
    elif choice == "3":
        search_student()
    elif choice == "4":
        break
    else:
        print("Invalid choice")
```

---

# 34. Real Project 4 — Password Generator

```python
import random
import string

length = int(input("Enter password length: "))

characters = string.ascii_letters + string.digits + string.punctuation
password = "".join(random.choice(characters) for _ in range(length))

print("Generated password:", password)
```

## Concepts used

* modules
* strings
* loops
* random generation

---

# 35. Real Project 5 — File Organizer

This is closer to real automation.

```python
import os
import shutil

source_folder = "my_files"

file_types = {
    "Images": [".jpg", ".png", ".jpeg", ".gif"],
    "Documents": [".pdf", ".docx", ".txt"],
    "Videos": [".mp4", ".mkv"],
    "Archives": [".zip", ".rar"]
}

for filename in os.listdir(source_folder):
    file_path = os.path.join(source_folder, filename)

    if os.path.isfile(file_path):
        ext = os.path.splitext(filename)[1].lower()

        moved = False
        for folder, extensions in file_types.items():
            if ext in extensions:
                dest_folder = os.path.join(source_folder, folder)
                os.makedirs(dest_folder, exist_ok=True)
                shutil.move(file_path, os.path.join(dest_folder, filename))
                moved = True
                break

        if not moved:
            other_folder = os.path.join(source_folder, "Others")
            os.makedirs(other_folder, exist_ok=True)
            shutil.move(file_path, os.path.join(other_folder, filename))

print("Files organized successfully.")
```

## Concepts used

* OS operations
* files
* automation
* dictionaries
* real-world scripting

---

# 36. Real Project 6 — Expense Tracker

```python
expenses = []

def add_expense():
    title = input("Expense title: ")
    amount = float(input("Amount: "))
    expenses.append({"title": title, "amount": amount})
    print("Expense added.")

def show_expenses():
    total = 0
    for e in expenses:
        print(f"{e['title']} - {e['amount']}")
        total += e["amount"]
    print("Total:", total)

while True:
    print("\n1. Add Expense")
    print("2. Show Expenses")
    print("3. Exit")

    choice = input("Choice: ")

    if choice == "1":
        add_expense()
    elif choice == "2":
        show_expenses()
    elif choice == "3":
        break
    else:
        print("Invalid choice")
```

---

# 37. Real Project 7 — API Data Fetcher

```python
import requests

url = "https://jsonplaceholder.typicode.com/users"
response = requests.get(url)

if response.status_code == 200:
    users = response.json()
    for user in users:
        print(user["name"], "-", user["email"])
else:
    print("Failed to fetch data")
```

## Concepts used

* HTTP requests
* JSON
* external APIs
* loops through structured data

---

# 38. Real Project 8 — Simple OOP Bank System

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print("Deposited:", amount)
        else:
            print("Invalid amount")

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            print("Withdrawn:", amount)
        else:
            print("Insufficient balance")

    def show_balance(self):
        print(f"{self.owner}'s balance: {self.balance}")

acc = BankAccount("Seyam", 1000)
acc.deposit(500)
acc.withdraw(300)
acc.show_balance()
```

---

# 39. Real Project 9 — Quiz Game

```python
questions = [
    {
        "question": "What is the capital of Bangladesh?",
        "options": ["A. Dhaka", "B. Chittagong", "C. Khulna", "D. Rajshahi"],
        "answer": "A"
    },
    {
        "question": "Which language is this course about?",
        "options": ["A. Java", "B. C++", "C. Python", "D. PHP"],
        "answer": "C"
    }
]

score = 0

for q in questions:
    print("\n" + q["question"])
    for opt in q["options"]:
        print(opt)

    user_answer = input("Your answer: ").upper()

    if user_answer == q["answer"]:
        print("Correct!")
        score += 1
    else:
        print("Wrong!")

print(f"\nFinal score: {score}/{len(questions)}")
```

---

# 40. Real Project 10 — Number Guessing Game

```python
import random

secret = random.randint(1, 100)

while True:
    guess = int(input("Guess a number (1-100): "))

    if guess < secret:
        print("Too low")
    elif guess > secret:
        print("Too high")
    else:
        print("Correct!")
        break
```

---

# 41. How Python is Used in Real Industry

## Web Development

Frameworks:

* Django
* Flask
* FastAPI

## Automation

Examples:

* file renaming
* report generation
* web scraping
* email automation

## Data Science

Libraries:

* NumPy
* pandas
* matplotlib

## AI / ML

Libraries:

* scikit-learn
* TensorFlow
* PyTorch

## Cybersecurity

Examples:

* network scanners
* automation scripts
* log analysis
* packet parsing

---

# 42. Example Real-World Folder Structure

For a medium Python project:

```bash
my_project/
│
├── app.py
├── requirements.txt
├── README.md
├── data/
├── utils/
│   ├── __init__.py
│   └── helpers.py
├── services/
│   ├── __init__.py
│   └── api_service.py
└── tests/
    └── test_app.py
```

---

# 43. Writing Better Python Code

Bad:

```python
x = 10
y = 20
z = x + y
print(z)
```

Better:

```python
first_number = 10
second_number = 20
total = first_number + second_number
print(total)
```

Bad:

```python
def do(a, b, c):
    return a * b - c
```

Better:

```python
def calculate_discounted_total(price, quantity, discount):
    return price * quantity - discount
```

---

# 44. Debugging in Python

## Print debugging

```python
name = "Seyam"
print("DEBUG:", name)
```

## Use `type()`

```python
x = input("Enter number: ")
print(type(x))
```

## Handle exceptions

```python
try:
    value = int("abc")
except ValueError as e:
    print("Error:", e)
```

---

# 45. Common Beginner Mistakes

## 1. Forgetting indentation

Wrong:

```python
if True:
print("Hello")
```

Correct:

```python
if True:
    print("Hello")
```

## 2. Mixing string and int

Wrong:

```python
age = input("Age: ")
print(age + 5)
```

Correct:

```python
age = int(input("Age: "))
print(age + 5)
```

## 3. Using `=` instead of `==`

Wrong:

```python
if x = 5:
    print("Yes")
```

Correct:

```python
if x == 5:
    print("Yes")
```

## 4. Index out of range

```python
nums = [1, 2, 3]
print(nums[5])  # error
```

---

# 46. Python Interview-Level Topics

You should know these well:

* difference between list and tuple
* difference between `is` and `==`
* mutable vs immutable
* shallow copy vs deep copy
* decorators
* generators
* iterators
* list comprehension
* exception handling
* OOP concepts
* `*args` and `**kwargs`
* module vs package
* `self`
* `__init__`
* `__name__ == "__main__"`

Example:

```python
a = [1, 2]
b = a
c = a.copy()

print(a == b)  # True
print(a is b)  # True

print(a == c)  # True
print(a is c)  # False
```

---

# 47. Full Learning Path for Python

## Stage 1: Beginner

Learn:

* syntax
* variables
* input/output
* operators
* if/else
* loops
* functions
* lists, tuples, sets, dictionaries

Practice:

* calculator
* odd/even checker
* marks grader
* multiplication table
* simple to-do list

## Stage 2: Intermediate

Learn:

* file handling
* exception handling
* modules
* OOP
* JSON
* working with libraries
* virtual environment

Practice:

* student management system
* expense tracker
* quiz app
* password generator
* file organizer

## Stage 3: Advanced

Learn:

* decorators
* generators
* iterators
* package structure
* APIs
* testing
* clean code

Practice:

* REST API client
* web scraper
* automation bot
* Flask/FastAPI app
* database project

---

# 48. Mini Project Ideas by Level

## Beginner

* calculator
* number guessing game
* temperature converter
* simple login checker
* unit converter

## Intermediate

* contact book
* expense tracker
* weather app using API
* file organizer
* quiz system

## Advanced

* blog backend with Flask/FastAPI
* chat app backend
* portfolio automation tool
* web scraper dashboard
* student result management system with database

---

# 49. One Complete Example Project — Contact Book

This project combines functions, lists, dictionaries, loops, and files.

```python
import json
import os

FILE_NAME = "contacts.json"

def load_contacts():
    if os.path.exists(FILE_NAME):
        with open(FILE_NAME, "r") as file:
            return json.load(file)
    return []

def save_contacts(contacts):
    with open(FILE_NAME, "w") as file:
        json.dump(contacts, file, indent=4)

def add_contact(contacts):
    name = input("Enter name: ")
    phone = input("Enter phone: ")
    email = input("Enter email: ")

    contacts.append({
        "name": name,
        "phone": phone,
        "email": email
    })

    save_contacts(contacts)
    print("Contact added successfully.")

def show_contacts(contacts):
    if not contacts:
        print("No contacts found.")
        return

    for i, contact in enumerate(contacts, start=1):
        print(f"{i}. {contact['name']} | {contact['phone']} | {contact['email']}")

def search_contact(contacts):
    keyword = input("Enter name to search: ").lower()

    found = False
    for contact in contacts:
        if keyword in contact["name"].lower():
            print(contact)
            found = True

    if not found:
        print("No matching contact found.")

def delete_contact(contacts):
    show_contacts(contacts)
    try:
        index = int(input("Enter contact number to delete: ")) - 1
        removed = contacts.pop(index)
        save_contacts(contacts)
        print(f"Deleted {removed['name']}")
    except (ValueError, IndexError):
        print("Invalid choice.")

def main():
    contacts = load_contacts()

    while True:
        print("\n--- Contact Book ---")
        print("1. Add Contact")
        print("2. Show Contacts")
        print("3. Search Contact")
        print("4. Delete Contact")
        print("5. Exit")

        choice = input("Enter choice: ")

        if choice == "1":
            add_contact(contacts)
        elif choice == "2":
            show_contacts(contacts)
        elif choice == "3":
            search_contact(contacts)
        elif choice == "4":
            delete_contact(contacts)
        elif choice == "5":
            print("Goodbye!")
            break
        else:
            print("Invalid choice.")

if __name__ == "__main__":
    main()
```

## What this project teaches

* file handling
* JSON persistence
* modular function design
* list of dictionaries
* user input validation
* real program structure

---

# 50. Final Advice

To master Python well, do this:

* learn one concept
* write code immediately
* modify the code yourself
* break the code and fix it
* build small projects
* then build bigger projects

Best learning formula:

**Concept → Example → Practice → Project**

---

# 51. Best Project Order for You

Since you like programming and practical learning, follow this order:

1. calculator
2. number guessing game
3. to-do list
4. student management system
5. contact book
6. file organizer
7. API data fetcher
8. Flask or FastAPI backend
9. database project
10. automation/security-related scripts

---

# 52. What to Learn After This

After core Python, the next best directions are:

* **Python for automation**
* **Python with SQL**
* **Flask / FastAPI**
* **Python for DSA**
* **Python for cybersecurity scripting**
* **Python with web scraping**
* **Python with OOP + real architecture**

If you want, I can make the **next part** as a **full Python notes + exercises + interview questions + 10 real projects** in one structured guide.
