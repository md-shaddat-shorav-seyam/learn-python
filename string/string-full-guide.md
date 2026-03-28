Here is a detailed **A to Z guide of Python strings and string methods**.

---

# Python String: Full Detailed Guide

## 1. What is a string in Python?

A **string** is a sequence of characters.

Examples:

```python
name = "Shorav"
city = 'Dhaka'
message = """This is
multiple lines"""
```

A string can contain:

* letters
* numbers
* symbols
* spaces
* Unicode characters

Example:

```python
s1 = "Hello"
s2 = "123"
s3 = "Hello 123 !"
s4 = "বাংলা"
```

---

# 2. How to create strings

## Using single quotes

```python
a = 'Python'
```

## Using double quotes

```python
b = "Python"
```

## Using triple quotes

Used for multi-line strings.

```python
c = """Python
is
awesome"""
```

---

# 3. String is immutable

In Python, strings are **immutable**.

That means once created, you cannot change individual characters directly.

```python
text = "hello"
# text[0] = "H"   # Error
```

Correct way:

```python
text = "H" + text[1:]
print(text)
```

Output:

```python
Hello
```

---

# 4. Accessing characters

## Indexing

```python
word = "Python"
print(word[0])   # P
print(word[1])   # y
print(word[5])   # n
```

## Negative indexing

```python
print(word[-1])  # n
print(word[-2])  # o
```

---

# 5. String slicing

Syntax:

```python
string[start:stop:step]
```

Example:

```python
text = "PythonProgramming"

print(text[0:6])    # Python
print(text[6:])     # Programming
print(text[:6])     # Python
print(text[::2])    # Pto rgamn
print(text[::-1])   # reverse
```

---

# 6. Looping through a string

```python
text = "Python"

for ch in text:
    print(ch)
```

Using index:

```python
for i in range(len(text)):
    print(i, text[i])
```

---

# 7. Checking length of a string

```python
text = "Python"
print(len(text))
```

Output:

```python
6
```

---

# 8. String operators

## Concatenation `+`

```python
a = "Hello"
b = "World"
print(a + " " + b)
```

## Repetition `*`

```python
print("Hi" * 3)
```

Output:

```python
HiHiHi
```

## Membership `in`, `not in`

```python
text = "Python Programming"
print("Python" in text)      # True
print("Java" not in text)    # True
```

---

# 9. Comparing strings

```python
print("abc" == "abc")   # True
print("abc" < "abd")    # True
print("A" < "a")        # True
```

Python compares strings **lexicographically** based on Unicode values.

---

# 10. Escape characters

| Escape | Meaning         |
| ------ | --------------- |
| `\'`   | single quote    |
| `\"`   | double quote    |
| `\\`   | backslash       |
| `\n`   | new line        |
| `\t`   | tab             |
| `\r`   | carriage return |
| `\b`   | backspace       |

Example:

```python
print("Hello\nWorld")
print("Hello\tWorld")
print("He said \"Python is great\"")
```

---

# 11. Raw string

A raw string ignores escape sequences.

```python
path = r"C:\Users\Name\Docs"
print(path)
```

---

# 12. Important built-in functions for strings

## `len()`

```python
print(len("Python"))
```

## `str()`

Converts something to string.

```python
num = 100
print(str(num))
```

## `ord()`

Returns Unicode of a character.

```python
print(ord("A"))   # 65
```

## `chr()`

Returns character from Unicode.

```python
print(chr(65))    # A
```

---

# 13. Common string methods in Python

Now the main part: **all important string methods**.

---

## 13.1 `lower()`

Converts all characters to lowercase.

```python
text = "PYTHON"
print(text.lower())
```

Output:

```python
python
```

---

## 13.2 `upper()`

Converts all characters to uppercase.

```python
text = "python"
print(text.upper())
```

---

## 13.3 `title()`

Converts first letter of each word to uppercase.

```python
text = "python programming language"
print(text.title())
```

Output:

```python
Python Programming Language
```

---

## 13.4 `capitalize()`

Makes first character uppercase and rest lowercase.

```python
text = "python is FUN"
print(text.capitalize())
```

Output:

```python
Python is fun
```

---

## 13.5 `swapcase()`

Uppercase becomes lowercase and lowercase becomes uppercase.

```python
text = "PyThOn"
print(text.swapcase())
```

---

## 13.6 `casefold()`

More aggressive lowercase, useful for case-insensitive comparisons.

```python
a = "HELLO"
b = "hello"

print(a.casefold() == b.casefold())
```

---

## 13.7 `strip()`

Removes spaces from both ends.

```python
text = "   hello   "
print(text.strip())
```

---

## 13.8 `lstrip()`

Removes spaces from left side.

```python
text = "   hello"
print(text.lstrip())
```

---

## 13.9 `rstrip()`

Removes spaces from right side.

```python
text = "hello   "
print(text.rstrip())
```

---

## 13.10 `replace(old, new)`

Replaces substring.

```python
text = "I like Java"
print(text.replace("Java", "Python"))
```

---

## 13.11 `find()`

Returns first index of substring, or `-1` if not found.

```python
text = "Python Programming"
print(text.find("Pro"))
print(text.find("Java"))
```

---

## 13.12 `rfind()`

Returns last occurrence index.

```python
text = "one two one"
print(text.rfind("one"))
```

---

## 13.13 `index()`

Like `find()`, but gives error if not found.

```python
text = "Python"
print(text.index("t"))
```

---

## 13.14 `rindex()`

Like `rfind()` but raises error if substring not found.

```python
text = "abc abc"
print(text.rindex("abc"))
```

---

## 13.15 `count()`

Counts how many times substring appears.

```python
text = "banana"
print(text.count("a"))
```

Output:

```python
3
```

---

## 13.16 `startswith()`

Checks if string starts with given value.

```python
text = "Python Programming"
print(text.startswith("Python"))
```

---

## 13.17 `endswith()`

Checks if string ends with given value.

```python
text = "report.pdf"
print(text.endswith(".pdf"))
```

---

## 13.18 `split()`

Splits string into a list.

```python
text = "apple,banana,mango"
print(text.split(","))
```

Output:

```python
['apple', 'banana', 'mango']
```

---

## 13.19 `rsplit()`

Splits from the right side.

```python
text = "one-two-three-four"
print(text.rsplit("-", 2))
```

---

## 13.20 `splitlines()`

Splits lines into a list.

```python
text = "Hello\nWorld\nPython"
print(text.splitlines())
```

---

## 13.21 `join()`

Joins elements of iterable into a string.

```python
words = ["Python", "is", "great"]
print(" ".join(words))
```

Output:

```python
Python is great
```

---

## 13.22 `center(width)`

Centers string.

```python
text = "Python"
print(text.center(20))
```

---

## 13.23 `ljust(width)`

Left-justifies string.

```python
text = "Python"
print(text.ljust(10, "-"))
```

---

## 13.24 `rjust(width)`

Right-justifies string.

```python
text = "Python"
print(text.rjust(10, "-"))
```

---

## 13.25 `zfill(width)`

Pads with zeros from left.

```python
num = "42"
print(num.zfill(5))
```

Output:

```python
00042
```

---

## 13.26 `partition(sep)`

Splits into 3 parts: before, separator, after.

```python
text = "name=Shorav"
print(text.partition("="))
```

Output:

```python
('name', '=', 'Shorav')
```

---

## 13.27 `rpartition(sep)`

Same as partition, but from the right side.

```python
text = "a-b-c"
print(text.rpartition("-"))
```

---

## 13.28 `format()`

Formats strings.

```python
name = "Shorav"
age = 18
print("My name is {} and I am {} years old".format(name, age))
```

---

## 13.29 `format_map()`

Like `format()`, but uses dictionary.

```python
data = {"name": "Shorav", "age": 18}
print("My name is {name} and I am {age}".format_map(data))
```

---

## 13.30 `encode()`

Converts string to bytes.

```python
text = "Python"
print(text.encode())
```

---

# 14. Checking methods (returns True/False)

These are very important.

---

## 14.1 `isalnum()`

Checks if all characters are letters or digits.

```python
print("abc123".isalnum())   # True
print("abc 123".isalnum())  # False
```

---

## 14.2 `isalpha()`

Checks if all characters are letters only.

```python
print("Python".isalpha())   # True
print("Python3".isalpha())  # False
```

---

## 14.3 `isdigit()`

Checks if all characters are digits.

```python
print("12345".isdigit())    # True
print("12.5".isdigit())     # False
```

---

## 14.4 `isdecimal()`

Checks if all are decimal characters.

```python
print("123".isdecimal())    # True
```

---

## 14.5 `isnumeric()`

Checks if all are numeric characters.

```python
print("123".isnumeric())    # True
```

---

## 14.6 `islower()`

Checks if all alphabetic characters are lowercase.

```python
print("python".islower())   # True
```

---

## 14.7 `isupper()`

Checks if all alphabetic characters are uppercase.

```python
print("PYTHON".isupper())   # True
```

---

## 14.8 `istitle()`

Checks if string is title-cased.

```python
print("Python Programming".istitle())   # True
```

---

## 14.9 `isspace()`

Checks if all characters are whitespace.

```python
print("   \t\n".isspace())   # True
```

---

## 14.10 `isidentifier()`

Checks if string is a valid Python identifier.

```python
print("my_var".isidentifier())   # True
print("2var".isidentifier())     # False
```

---

## 14.11 `isprintable()`

Checks if all characters are printable.

```python
print("Hello".isprintable())     # True
print("Hello\n".isprintable())   # False
```

---

## 14.12 `isascii()`

Checks if all characters are ASCII.

```python
print("Hello".isascii())   # True
print("বাংলা".isascii())   # False
```

---

# 15. String formatting methods

Python has 3 main ways.

---

## 15.1 Old style `%` formatting

```python
name = "Shorav"
age = 18
print("My name is %s and I am %d years old" % (name, age))
```

---

## 15.2 `format()`

```python
name = "Shorav"
age = 18
print("My name is {} and I am {}".format(name, age))
```

With positions:

```python
print("My name is {0} and I am {1}".format("Shorav", 18))
```

With names:

```python
print("My name is {name} and I am {age}".format(name="Shorav", age=18))
```

---

## 15.3 f-string

Best and most modern way.

```python
name = "Shorav"
age = 18
print(f"My name is {name} and I am {age} years old")
```

Expression inside:

```python
a = 5
b = 10
print(f"Sum = {a+b}")
```

---

# 16. Useful real-life string examples

## Reverse a string

```python
text = "Python"
print(text[::-1])
```

---

## Check palindrome

```python
text = "madam"
if text == text[::-1]:
    print("Palindrome")
else:
    print("Not palindrome")
```

---

## Count vowels

```python
text = "programming"
count = 0

for ch in text.lower():
    if ch in "aeiou":
        count += 1

print(count)
```

---

## Remove spaces

```python
text = "Python is fun"
print(text.replace(" ", ""))
```

---

## Count words

```python
text = "Python is very easy to learn"
words = text.split()
print(len(words))
```

---

## Convert first letter of each word capital

```python
text = "i love python programming"
print(text.title())
```

---

# 17. Important difference between some methods

## `find()` vs `index()`

`find()`:

* returns `-1` if not found

`index()`:

* gives error if not found

Example:

```python
text = "hello"
print(text.find("x"))   # -1
# print(text.index("x"))  # ValueError
```

---

## `split()` vs `partition()`

`split()` returns a list.

```python
print("a=b=c".split("="))
```

Output:

```python
['a', 'b', 'c']
```

`partition()` returns 3 parts.

```python
print("a=b=c".partition("="))
```

Output:

```python
('a', '=', 'b=c')
```

---

## `lower()` vs `casefold()`

`casefold()` is stronger for text comparison.

```python
a = "HELLO"
b = "hello"

print(a.lower() == b.lower())
print(a.casefold() == b.casefold())
```

---

# 18. Mini table of important string methods

| Method         | Work                     |
| -------------- | ------------------------ |
| `lower()`      | lowercase                |
| `upper()`      | uppercase                |
| `title()`      | title case               |
| `capitalize()` | first letter capital     |
| `swapcase()`   | reverse case             |
| `strip()`      | remove spaces both sides |
| `replace()`    | replace text             |
| `find()`       | find substring           |
| `count()`      | count substring          |
| `startswith()` | starts check             |
| `endswith()`   | ends check               |
| `split()`      | string to list           |
| `join()`       | list to string           |
| `isalnum()`    | letters+digits check     |
| `isalpha()`    | letters only             |
| `isdigit()`    | digits only              |
| `islower()`    | lowercase check          |
| `isupper()`    | uppercase check          |

---

# 19. Practice code with many methods

```python
text = "  python programming  "

print("Original:", text)
print("Lower:", text.lower())
print("Upper:", text.upper())
print("Title:", text.title())
print("Capitalize:", text.capitalize())
print("Strip:", text.strip())
print("Replace:", text.replace("python", "java"))
print("Find:", text.find("pro"))
print("Count:", text.count("m"))
print("Startswith:", text.strip().startswith("python"))
print("Endswith:", text.strip().endswith("ing"))

words = text.strip().split()
print("Split:", words)
print("Join:", "-".join(words))
```

---

# 20. Interview/common exam points

Very important things to remember:

* Python string is **immutable**
* Indexing starts from **0**
* Negative indexing works from the end
* Slicing does not change original string
* `split()` gives list
* `join()` combines list into string
* `find()` returns `-1` if not found
* `replace()` creates a new string
* `strip()` removes spaces at ends, not middle
* `f-string` is modern and powerful

---

# 21. Most used string methods in competitive programming and real coding

These are used most often:

```python
s.lower()
s.upper()
s.strip()
s.split()
" ".join(list_data)
s.replace()
s.find()
s.count()
s.startswith()
s.endswith()
len(s)
```

---

# 22. Full example program

```python
name = input("Enter your full name: ")

print("Original:", name)
print("Upper:", name.upper())
print("Lower:", name.lower())
print("Title:", name.title())
print("Length:", len(name))
print("Without spaces:", name.replace(" ", ""))
print("Words:", name.split())

if name.isalpha():
    print("Only letters")
else:
    print("Contains spaces or other characters")
```

---

# 23. Complete method list you should know

Main string methods:

```python
capitalize()
casefold()
center()
count()
encode()
endswith()
expandtabs()
find()
format()
format_map()
index()
isalnum()
isalpha()
isascii()
isdecimal()
isdigit()
isidentifier()
islower()
isnumeric()
isprintable()
isspace()
istitle()
isupper()
join()
ljust()
lower()
lstrip()
maketrans()
partition()
removeprefix()
removesuffix()
replace()
rfind()
rindex()
rjust()
rpartition()
rsplit()
rstrip()
split()
splitlines()
startswith()
strip()
swapcase()
title()
translate()
upper()
zfill()
```

---

# 24. Some newer useful methods

## `removeprefix()`

```python
text = "unhappy"
print(text.removeprefix("un"))
```

Output:

```python
happy
```

---

## `removesuffix()`

```python
text = "filename.txt"
print(text.removesuffix(".txt"))
```

---

## `maketrans()` and `translate()`

Useful for multiple replacements.

```python
table = str.maketrans("aeiou", "12345")
text = "education"
print(text.translate(table))
```

---

## `expandtabs()`

Converts tabs into spaces.

```python
text = "Hello\tWorld"
print(text.expandtabs(4))
```

---

# 25. Best way to learn strings

Learn in this order:

1. create string
2. indexing
3. slicing
4. loop through string
5. basic methods like `lower`, `upper`, `strip`, `split`, `join`
6. searching methods like `find`, `count`
7. checking methods like `isalpha`, `isdigit`
8. formatting using f-strings
9. practice problems

---

# 26. Simple practice questions

Practice these:

1. Reverse a string
2. Count vowels in a string
3. Check palindrome
4. Convert sentence to uppercase
5. Replace spaces with `-`
6. Count words in a sentence
7. Check whether a string contains only digits
8. Remove prefix and suffix
9. Find first and last occurrence of a character
10. Join a list of words into a sentence

---

# 27. Final summary

A Python string is:

* ordered
* iterable
* immutable
* supports indexing and slicing
* has many built-in methods for searching, formatting, checking, and transforming text

The most important methods are:

* `lower()`
* `upper()`
* `strip()`
* `split()`
* `join()`
* `replace()`
* `find()`
* `count()`
* `startswith()`
* `endswith()`
* `isalpha()`
* `isdigit()`

---

I can also make this into a **clean exam-style note**, a **mind map**, or a **50+ practice problems set with answers**.
