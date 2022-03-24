# python

## basic

1. print() 출력
2.
3. Exponentiation 제곱, 지수 표현

```py
print( 2**5 )

# 2^5의 결과가 나온다.

```

4. Floor division 나누고 소수점 내림(몫을 구한다.)

```py
print(20 // 6)

# 3이 결과값으로 나온다.

```

5. Remainder 나눗셈

```py
print (20 % 6)
print(1.25 % 0.5)
```

---

## string

1. print('')내부에서 어퍼스트로피를 쓰고싶은 경우 \'를 입력해주면 된다.

```

```

2. Newlines \n과 \t
   > \n는 다음 줄을 작성할 때 사용하고 \t는 문자열 사이에 탭 간격을 줄 때 사용한다.
   >
   > > '\\'는 문자 '\'를 그대로 사용할 때 사용한다 '\"', '\''는 작은따옴표와 큰따옴표를 그대로 사용할 경우 사용한다.

```py
print('one\ntwo\nthree');


# one
# two
# three


print('one\ttwo\tthree');


# one     two     three

```

3. Multiline

```py
print("""this
is a multiline
text""")


# this
# is a multiline
# text

```

4. String Operation

```py
print("spam" * 3);
print(4 * '2');


# spamspamspam
# 2222

```

5. Variables

   - 선언명으로 할 수 있는 것은 글자, 숫자, 언더스코어(\_)이며 숫자로 시작할 수 없다.
   - 숫자로 시작할 수 없다
   - 특수문자는 사용할 수 없다.
   - 변수 이름에 공백이 있으면 안된다.
   - 파이썬의 예약어 등은 사용할 수 없다.

6. Chaining Multiple Conditions

```py
x = 4
y = 2

if not 1 + 1 == y or x == 4 and 7 == 8:
    print("Yes")
elif x > y:
    print("no")
```

7. Lists

```py
words = ["Hello", "world", "!"]
print(words[0])
print(words[1])
print(words[2])
```

> Space("") is also a symbol and has an index

8. List Operations

```py
nums = [7, 7, 7, 7, 7]
nums[2] = 5
print(nums)

# [7, 7, 5, 7, 7]

```

9. List Operations
   > List can be added and multiplied in the smae way as strings

```py
nums = [1, 2, 3]
print(nums + [4, 5, 6])
print(nums * 3)

# [1, 2, 3, 4, 5, 6]
# [1, 2, 3, 1, 2, 3, 1, 2, 3]

```

10. List Operations

```py
words = ["spam", "egg", "spam", "sausage"]
print("spam" in words)
print("egg" in words)
print("tomato" in words)


# True
# True
# False

```

11. List Operations
    > To check if an item is not a list, you can use the not operator in one of the following ways

```py
nums = [1, 2, 3]
print(not 4 in nums)
print(4 not in nums)
print(not 3 in nums)
print(3 not in nums)


# True
# True
# False
# False

```

12. List Functions
    > The append method adds an item to the end of an existing list.

```py
nums = [1, 2, 3]
nums.append(4)
print(nums)


# [1, 2, 3, 4]

```

13. List Functions
    > To get the number of items in a list, you can use the len function

```py
nums = [1, 2, 5, 2, 4]

print(len(nums))


# 5

```

14. List Functions
    > The insert method is similar to append, except that it allows you to insert a new item at any position in the list, as opposed to just at the end

```py
words = ["python", "fun"]
index = 1
words.insert(index, "is")
print(words)


# ['python', 'is', 'fun']

```

15. List Functions
    > The index method finds the first occurrence of a list item and returns its index. if the item isn't in the list, it raises a ValueError

```py
letters = ['p', 'q', 'r', 's', 'p', 'u']
print(letters.index('r'))
print(letters.index('p'))
print(letters.index('z'))

    """
    2
    0
    ValueError : 'z' is not in list
    """
```

16. While Loops
    > A while loop is used to repeat a block of code multiple times. For Example, let's say we need to process multiple user inputs, so that each time the user inputs somethin, the same block of code needs to excute. Below is a while loop containing a variable that counts up for 1 to 5, at which point the loop terminates.

```py
i = 1
while i <= 5:
    print(i)
    i = i + 1

print("Finished")
    """
    1
    2
    3
    4
    5
    Finished
    """
```

17. While Loops
    > You can use multiple statements in the while loop.
    > For example, you can use an if statement to make decisions. This ca be useful, if you are making a game and need to loop through a number of player actions and add or remove points of the player.
    > The code below uses an if/else statement inside a while loop to seperrate the even and odd numbers in the range of 1 to 10

```py
x = 1
while x < 10:
    if x % 2 == 0:
        print(str(x) + "is even")
    else:
        print(str(x) + "is odd")
    x += 1

    """
    1is odd
    2is even
    3is odd
    4is even
    5is odd
    6is even
    7is odd
    8is even
    9is odd
    """
```

18. break

    > To end a while loop prematurely, the break statement can be used. For example, we can break an infinite loop if some condition is met

    > > While True is a short and easy way to make an infinite loop.

```py
i = 0
while True :
    print(i)
    i = i + 1
    if i >= 5:
        print("Breaking")
        break
print("Finished")
```

19. continue
    > Another statement that can be used within loop is continue. Unlike break, continue jumps back to the top of the loop, rather than stopping it. Basically, the continue statement stops the current iteration and continues with the next one.

```py
i = 0
while i < 5:
    i += 1
    if i == 3:
        print("Skipping 3")
        continue
    print(i)

    """
    1
    2
    Skipping 3
    4
    5
    """
```

20. for Loop
    > The for loop is used to iterate over a given sequence, such as lists or strings. The code below outputs each item in the list and adds and exclamation mark at the end

```py
words = ["hello", "world", "spam", "eggs"]
for word in words:
    print(word + "!")
    """
    hello!
    world!
    spam!
    eggs!
    """
```

21. for Loops(The for loop can be used to iterate over stirngs)

```py
str = "testing for loops"
count = 0

for x in str:
    if(x == 't'):
        count += 1
print(count)

 # 2

```

> The code above defines a count variable, iterates over the string and calculates the count of 't' letters in it. During each iteration, the x variable represents the current letter of the string. The count Variable is incremented each time the letter 't' is found, Thus, at the end of the loop it represents the number of 't' letters in the string.

22. Range

```py
numbers = list(range(10))

print(numbers)

    """
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    """
```

22. Range (second argument)
    > if range is called with one argument, it produces an object with values from 0 to that argument. if it is called with two arguments, it produces values from the first to the second.

```py
numbers = list(range(3, 8))
print(numbers)

print(range(20) == range(0, 20))
    """
    [3, 4, 5, 6, 7, 8]
    True
    """
```

22. Range (third argument)
    > range can have a third argument, which determines the interval of the sequence produced, also called the step.

```py
numbers = list(range(5, 20, 2))
print(numbers)
    """
    [5, 7, 9, 11, 13, 15, 17, 19]
    """
```

22. for Loops
    > The for loop is commonly used to repeat some code a certain number of times. This is done by combining for loops with range objects.

```py
for i in range(5):
print("hello!")

    """
    hellow!
    hellow!
    hellow!
    hellow!
    hellow!
    """
```

23. Resuing Code

    > Code reuse is a very inportant part of programming in any language. Incresing code size makes it harder to maintain. For a large programming project to be successful, it is essential to abide by the Don't Repeat Yourself, or Dry, principle. We've already looked at one way of doing this: by using loops. In this module, we will explore two ,ore: functions and modules.
    >
    > > Bad, repetitive code is said to abide by the WET principle, which stands for Write Everything Twice, or We Enjoy Typing.

24. Functions
    > in addition to using pre-defined functions, you can create your own functions by using the 'def' statement. Here is an example of a function named my_func. it takes no arguments, and prints "spam" three times. it is defined, and then called. The statements in the function are executed only when the function is called.

```py
def my_func():
    print("spam")
    print("spam")
    print("spam")
my_func()
# spam
# spam
# spam
```

25. Arguments
    > All the function definitions we've looked at so far have been functions of zero arguments, which are called with empty parentheses. However, most functions take arguemnts. The example velow defineds a function that takes one argument:

```py
def print_with_exclamation(word):
    print(word + '!')

print_with_exclamation('spam')
print_with_exclamation('eggs')
print_with_exclamation('python')

# spam!
# eggs!
# python!
```

26. Returning from functions
    > Certain functions, such as int or str, return a value that can be used later. To do this for your defined functions, you can use the return statement.

```py
def max(x, y):
    if x >= y:
        return x
    else:
        return y
print(max(4, 7))
z = max(8, 5)
print(z)

# 7
# 8
```

> The return statement cannot be used outside of a function definition.

26. Returning from functions

> Once you return a value from a function, it immediately stops being executed. Any code after the return statement will never happen.

```py
def add_numbers(x, y):
    total = x + y
    return total
    print("This won't be printed")
print(add_numbers(4, 5))
# 9
```

27. Comments
    > Comments are annotations to code used to make it easier to understand. They don't affect how code is run. In Python, a comment is create by inserting an 'octothorpe'(otherwise known as a number sign or hash symbol: #). All text after it on that line is ignored.

```py
x = 365
y = 7
# this is a comment

print(x % y) #find the remainder
#print(x // y)
# another comment
```

28. Docstrings
    > Docstrings(documentation strings) serve a similar purpose to comments, as they are designed to explain code. However, they are more specific and have a different syntax. They are created by putting a multiline string containing an explanation of the function below the function's first line

```py
    """
    Print a word with an
    exclamation mark following it.
    """
    print(word + "!")
shout("spam")
```

29. Functions
    > Functions can also be used as arguemnts of other functions.

```py
def add(x, y):
    return x + y
def do_twice(func, x, y)"
return func(func(x, y), func(x, y))

a = 5
b = 10

print(do_twice(add, a, b))

    """
    30
    """
```

29. Modules
    > Modules are pieces of code that other people have written to fulfill common tasks, such as generating random numbers, performing mathmatical operations, etc. The basic way to use a module is to add import moule_name at the top of your code, and then using module_name.var to access functions and values with the name var in the modules. For example, the following example uses the random module to generate random numbers

```py
import random

for i in range(5):
    value = random.randint(1, 6)
    print(value)

# 1
# 2
# 5
# 2
# 3
```

29. Modules
    > There is another kind of import that can be used if you only need certain functions from a module. These take the form from module_name import var, and then var can be used as if it were defined normally in your code. For example, to import only the pi constant from the math module:

```py
from math import pi
print(pi)

 # 3.14159265359
```

29. Modules
    > You can import a module or object under a different name using the as keyword. This is mainly used when a module or object has a long or confusing name.

```py
from math import sqrt as square_root
print(square_root(100))

# 10.0
```

29. Modules
    > There are three main types of modules in Python, those you write yourself, those you install from external sources,and those that are preinstalled with Python.
    > the last type is called the standard library, and contains many useful modules. Some of the standard library's useful modules include string, re, datetime, math, random, os, multiprocessing, subprocess, socket, email, json, doctest, unittest, pdb, argparse and sys.
    > Tasks that can be done by the standard library include string parsing, data serialization, testing, debugging and manipulating dates, emails, command line arguments, and much more

> > many third-party Python modules are stored on the Python Package Index(PyPI).

30. Exceptions

- ImportError: an import fails
- IndexError: a list is indexed with an out-of-range number
- NameError: an unkown variable is used
- SyntaxError: the code can't be parsed properly
- TypeError: a function is called on a value of an inappropriate type
- ValueError: a function is called on a value of the correct type, but with an inappropriate value.

30. Exception Handling

```py
try:
    num1 = 7
    num2 = 0
    print(num1 / num2)
    print("Done calculation")
except ZeroDivisionError:
    print("An error occured")
    print("due to zero division")

# An error occured
# due to zero division

try:
    num1 = 7
    num2 = 1
    print(num1 / num2)
    print("Done calculation")
except ZeroDivisionError:
    print("An error occured")
    print("due to zero division")

# 7
# Done calculation
```

30. Exception Handling
    > A try statement can have multiple different except blocks to handle different exceptions. Multiple exceptions can also be put into a single except block using parentheses, to have the except block handle all of them

```py
try:
    variable = 10
    print(variable + "hello")
    print(variable / 2)
except ZeroDivisionError:
    print("Divided by zero")
except (ValueError, TypeError):
    print("Error occurred")

# Error occurred
```

30. Exception Handling
    > An except statement without any exception specified will catch all errors. These should be used sparingly, as they can catch unexpected errors and hide programming mistake.

```py
try:
    word = "spam"
    print(word / 0)
except:
    print("An error occurred")
```

31. finally
    > To ensure some code runs no matter what errors occur, you can use a finally statement. The finally statement is placed at the bottom of a try/except statement. Code withis a finally statement always runs after execution of the code in the try, and possibly in the except, blocks.

```py
try:
    print("Hello")
    print(1 / 0)
except ZeroDivisionError:
    print("Divided by zero")
finally:
    print("This code will run no matter what")
```

31. finally
    > Code in a finally statement even runs if an uncaught exception occurs in one of the preceding blocks.

```py
try:
    print(1)
    print(10 / 0)
except ZeroDivisionError:
    print(unknown_var)
finally:
    print("This is excuted last")
```

32. Raising Exceptions
    > You can raise exceptions by using the raise statement.

```py
print(1)
raise ValueError
print(2)
```

32. Raising Exceptions
    > Exceptions can be raised with arguments that give detail about them.

```py
name = "123"
raise NameError("Invalid name!")

# Traceback (most recent call last):
#  File "hellow.py", line 2, in <module>
#    raise NameError("Invalid name!")
#NameError: Invalid name!
```

32. Raising Exceptions
    > In except blocks, the raise statement can be used without arguments to re-raise whatever exception ocurred.

```py
try:
    num = 5 / 0
except:
    print("An error occurred")
    raise
# An error occurred
#Traceback (most recent call last):
#  File "hellow.py", line 2, in <module>
#    num = 5 / 0
#ZeroDivisionError: integer division or modulo by zero
```

33. Assertions
    > An assertion is a sanity-check that you can turn on or trun off when you have finished testing the program. An expression is tested, and if the result comes up false, an exception is raise. Assertions are carried out through use of the assert statement.

```py
print(1)
assert 2 + 2 == 4
print(2)
assert 1 + 1 == 3
print(3)
# 1
# 2
# Traceback (most recent call last):
#  File "hellow.py", line 4, in <module>
#    assert 1 + 1 == 3
# AssertionError
```

33. Assertions
    > The assert can take a second argument that is passed to the AssertionError raised if the assertion fails.

```py
temp = -10
assert (temp >= 0), "Colder than absolute zero!"
#Traceback (most recent call last):
#  File "hellow.py", line 2, in <module>
#    assert (temp >= 0), "Colder than absolute zero!"
#AssertionError: Colder than absolute zero!
```

- plus) AssertionError exceptions can be caught and handled like any other exception using the try-except statement, but if not handled, this type of exception will terminate the program.

34. Opening files
    > You can use Python to read and write the contents of files. Text files are the easiest to manipulate. Before a file can be edited, it must be opened, using the open function.

```py
myfile = open("filename.txt")
```

- plus) The argument of the open function is the path to the file. if the file is in the current working directory of the program, you can specify only its name.

34. Opening Files
    > You can specify the mode used to open a file by applying a second argument to the open function.

- Sending "r" means open in read mode, which is the default.
- Sending "w" means write mode, for rewriting the contents of a file
- Sending "a" means append mode, for adding new content to the end of the file.
- Adding "b" to a mode opens it in binary mode, which is used for non-text files (such as image and sound files).

```py
# write mode
open("filename.txt", "w")
# read mode
open("filename.txt", "r")
open("filename.txt")
# binary write mode
open("filename.txt", "wb")
```

- plus) You can use the + sign with each of the modes above to give them extra access to files, For example, r+ opens the file for both reading and writing.

34. Opening Files
    > Once a file has been opened and used, you should close it. This is done with the close method of the file object.

```py
file = open("filename.txt", "w")
# do stuff to the file

file.close()
```

- plus) We will read/write content to files in the upcoming lesson.

35. Reading Files
    > The contents of a file that has been opend in text mode can be read using the read method.

```py
file = open("filename.txt", "r")
cont = file.read()
print(cont)
file.close()
```

- This will print all of the contents of the file "filename.txt"

35. Reading Files
    > To read only a certain abount of a file, you can provide a number as an argument to the read function. This determines the number of bytes that should be read. You can make more calls to read on the same file object to read more of the file byte by byre. With no argument, read returns the rest of the file.

```py
file = open("filename.txt", "r")
print(file.read(16))
print(file.read(4))
print(file.read(4))
print(file.read())
file.close()
```

- Just like passing no arguments, negative values will return the entrie contents.

35. Reading Files
    > After all contents in a file have been read, any attempts to read furthre from that file will return an empty string, because you are trying to read from the end of the file.

```py
file = open("filename.txt", "r")
file.read()
print("Re-reading")
print(file.read())
print("Finished")
file.close()
```

```py
>>>
Re-reading

Finished
>>>
```

- Just like passing no arguments, negative values will return the entire contents.

35. Reading Files

> To retrieve each line in a file, you can use the readlines method to return a list in which each element is a line in the file.

```py
file = open("filename.txt", "r")
print(file.readlines())
file.close()
```

```py
>>>
['Line 1 text \n', 'Line 2 text \n', 'Line 3 text']
>>>
```

- You can calso use a for loop to iterate through the lines in the file:

```py
file = open("filename.txt", "r")

for line in file:
    print(line)

file.close()
```

```py
>>>
Line 1 text

Line 2 text

Line 3 text
>>>
```

- plus) In the output, the lines are separated by blank lines, as the print function automatically adds a new line at the end of its output.

36. Writing Files
    > To write to files you use the write method, which writes a string to the file.

```py
file = open("newFile.txt", "w")
file.write("This has been written to a file")
file.close()

file = open("newfile.txt", "r")
print(file.read())
file.close()
```

- plus) The "W" mode will create a file, if it does not already exist.

36. Writing Files

```py
file = open("newfile.txt", "r")
print("Reading initial contents")
print(file.read())
print("Finished")
file.close()

file = open("newfile.txt", "w")
file.wrie("Some new text")
file.close()

file = open("newfile.txt", "r")
print("REading new contents")
print(file.read())
print("Finished")
file.close()

# As you can see, the content of the file has been overwritten
```

- plus) What happens if you open a file in write mode and then immediately close it? : The file contents are deleted

36. Writing Files
    > The write method returns the number of bytes written to a file, if successful

```py
msg = "Hello world!"
file = open("newfile.txt", "w")
print(amount_written)
file.close()

# None
```

- plus) To write something other than a string, it needs to be converted to a string first.
- plus) If a file write operation is successful, which one of these statements will be true? : file.write(msg) == len(msg)

37. Working with Files
    > It is good practice to aboid wasting resource by making sure that files are always closed after they have been used. One way of doing this is to use try and finally.

```py
try:
    f = open("newfile.txt")
    print(f.read())
finally:
    f.close()

```

37. Working with Files
    > An alterantive way of doing this is using with statements. This creates a temporary variable(often called f), which is only accessible in the indented block of the with statement.

```py
with open('newfile.txt') as f:
    print(f.read())

# Hello world!
```

- plus) The file is automatically closed at the end of the with statement, even if exceptions occur within it.

### Type

1. None

   > The None object is used to represent the absence of a value. It is simmilar to null in othe programming languages. Like other "empty" values, such as 0, [] and the empty string, it is False when converted to a Boolean variable. When entered at the Python console, it is displayed as the empty string.

2. None

   > The None object is returned by any function that doesn't explicitly return anything else.

3. Dictionaries
   > Dictionaries are data structures used to map arbitrary keys to values. Lists can be thought of as dictionaries with integer keys within a certain range. Dictionaries can ve indexed in the same way as lists, using square brackets containing keys.

```py
ages = {"Dave": 24, "Mary": 42, "John": 58}
print(ages["Dave"])
print(ages["Mary"])

# 24
# 42
```

> Each element in a dictionary is represented by a Key: Value pair

4. Dictionaries
   > Trying to index a key that isn't part of the dictionary returns a KeyError.

```py
primary = {
    "red": [255, 0, 0],
    "green": [0, 255, 0],
    "blue": [0, 0, 255],
}

print(primary["red"])
print(primary["yellow"])

# [255, 0, 0]
# Traceback (most recent call last):
#  File "hellow.py", line 8, in <module>
#    print(primary["yellow"])
# KeyError: 'yellow'
```

> As you can see, a dictionary can store any types of data as values. An empty dictionary is defined as {}

5. Dictionaries
   > Only immutable objects can be used as keys to dictionaries. Immutable objects are those that can't be changed. So far, the only mutable objects you've come across are lists and dictionaries. Trying to use a mutable object as a dictionary key causes a TypeError.

```py
bad_dict = {
    [1, 2, 3]: "one two three",
}

# Traceback (most recent call last):
#  File "hellow.py", line 2, in <module>
#    [1, 2, 3]: "one two three",
# TypeError: unhashable type: 'list'
```

6. Dictionaries
   > Just like lists, dictionary keys can be assigned to different values. However, unlike lists, a new dictionary key can also be assigned a value, not just ones that already exist.

```py
squares = {1: 1, 2: 4, 3: "error", 4: 16,}
squares[8] = 64
squares[3] = 9
print(squares)

# {8: 64, 1: 1, 2: 4, 3: 9, 4: 16}
```

7. Dictionaries
   > To determine whether a key is in a dictionary, you can use in and not in, just as you can for a list.

```py
nums = {
    1: "one",
    2: "two",
    3: "three",
}

print(1 in nums)
print("three" in nums)
print(4 not in nums)

# True
# False
# True
```

8. Dictionaries
   > A useful dictionary method is get. it does the same thing as indexing, but if the key is not found in the dictionary it return another specified value instead('None', by default)

```py
pairs = {
    1: "apple",
    "orange": [2, 3, 4],
    True: False,
    None: "True",
}

print(pairs.get("orange"))
print(pairs.get(7))
print(pairs.get(12345, "not in dictionary"))

# [2, 3, 4]
# None
# not in dictionary
```

9. Dictionaries
   > A useful dictionary method is get. it does the same thing as indexing, but if the key is not found in the dictionary it returns another specified value instead('None', by default)

```py
pairs = {
 1: "apple",
 "orange": [2, 3, 4],
 True: False,
 None: "True",
}

print(pairs.get("orange"))
print(pairs.get(7))
print(pairs.get(12345, "not in dictionary"))
# [2, 3, 4]
# None
# not in dictionary
```

> > Dictionary 객체의 get()메소드 => dic.get(key, default=None), get메소드의 두번째 인자는 만약 해당 key가 없을 때 반환하는 None을 바꾸고 싶을 때 지정한다.

10. Tuple
    > Tuples are very similar to lists, except that they are immutable(they cannot be changed). Also, they are created using parentheses, rather than square brackets.

```py
words = ("spam", "eggs", "sausages")
print(words[0])
words[1] = 'cheese'

# spam
# TypeError: 'tuple' object does not support item assignment
```

11. Tuple
    > Tuples can be created without the parentheses, by just separating the values with commas.

```py
my_tuple = "one", "two", "three"
print(my_tuple[0])

# one
```

> > An empty tuple is created using an empty parenthesis pair.

```py
tpl = ()
```

> > > Tuples are faster than lists, but they cannot be changed.

12. List Slices

    > List slices provide a more advanced way of retrieving values from a list. Basic list slicing involves indexing a list with two colon-separated integers. This returns a new list containing all the values in the old list between the indices.

    > > Slicing can also be done on tuples.

```py
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[2: 6])
print(squares[3: 8])
print(squares[0: 1])

# [4, 9, 16, 25]
# [9, 16, 25, 36, 49]
# [0]
```

13. List Slices
    > If the first number in a slice is omitted, it is taken to be the start of the list. If the second number is omitted, it is taken to be the end

```py
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[:7])
print(squares[7:])

# [0, 1, 4, 9, 16, 25, 36]
# [49, 64, 81]
```

14. List Slices
    > List slices can aslso have a third number, representing the step, to include only alternate values in the slice.

```py
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[::2])
print(squares[2:8:3])

# [0, 4, 16, 36, 64]
# [4, 25]
```

> > [2:8:3]will include elements starting from the 2nd index up to the 8th with a step of 3.

15. List Slices
    > Negative values can be used in list slicing(and normal list indexing). When negative values are used for the first and second value in a slice (or a normal index), they count from the end of the list.

```py
squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
print(squares[1:-1])


#[1, 4, 9, 16, 25, 36, 49, 64]
```

> > If a negative value is used for the step, the slice is done backwards. Using [::-1] as a slice is a common and idiomatic way to reverse a list.

16. List Comprehensions
    > List comprehensions are a useful way of quickly creating lists whose contents obey a simple rule. For example, we can do the following:

```py
# a list comprehension
nums = [i*2 for i in range(10)]

print(nums)

# [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

17. List Comprehensions
    > A list comprehension can also contain an if statement to enforce a condition on values in the list

```py
evens=[i**2 for i in range(10) if i**2 % 2 == 0]

print(evens)

# [0, 4, 16, 36, 64]
```

18. List Comprehensions
    > Trying to create a list in a very extensive range will result in a MemoryError. This code shows an example where the list comprehension runs out of memory.

```py
even = [2*i for i in range(10**100)]

print(even)

# OverflowError: range() result has too many items
```

> > This issue is solved by generators, which are covered in the next module.

19. String Formatting
    > So far, to combine strngs and non-strings, you've converted the non-strings to strings and added them. String formatting provides a more powerful way to embed non-strings within strings. String formatting uses a string's format method to substitute a number of arguments in the string.

```py
# string formatting

nums = [4, 5, 6]
msg = "Number: {0} {1} {2}". format(nums[0], nums[1],nums[2])

print(msg)

# Number: 4 5 6
```

> > Each argument of the format function is placed in the string at the corresponding position, which is determinded using the curly braces{}.

20. String Formatting
    > String formatting can also be done with named arguments.

```py
a = "{x}, {y}".format(x = 5, y = 12)

print(a)

# 5, 12
```

21. String Functions
    > Python contains many useful built-in functions and methods to accomplish common tasks. join - joins a list of strings with another string as a separator. replace - replaces one substring in a string with another. startswitch and endswitch - determine if there is a substring at the start and end of a string, repectively. To change the case of a string, you can use lower and upper. The method split is the opposite of join turning a string with a certain separator into a list.

```py
print(",".join(["spam", "eggs", "ham"]))
# prints "spam, eggs, ham"

print("Hello ME".replace("ME", "world"))
# prints "Hello world"

print("This is a sentence.".startswith("This"))
# prints "True"

print("This is a sentence.".endswith("sentence."))
#prints "True"

print("This is a sentence.".upper())
# prints "THIS IS A SENTENCE."

print("AN ALL CAPS SENTENCE".lower())
#prints "an all caps sentence"

print("spam, eggs, ham".split(","))
#prints "['spam', 'eggs', 'ham']"
```

22. Numeric Functions
    > To find the maximum or minimum of some numbers or a list, you can use max or min. To find the distance of a number from zero (its absolute value), use abs. To round a number to a certain number of decimal places, use round. To find the total of a list, use sum.

```py
print(min(1, 2, 3, 4, 0, 2, 1))
print(max([1, 4, 9, 2, 5, 6, 8]))
print(abs(-99))
print(abs(42))
print(sum([1, 2, 3, 4, 5]))

# 0
# 9
# 99
# 42
# 15
```

23. List Functions
    > Often used in conditional statements statements, all and any take a list as an argument, and return True if all or any(respectively) of their arguments evaluate to True(and False otherwise). The function enumerate can be used to iterate through the values and indices of a list simultaneously.

```py
nums = [55, 44, 33, 22, 11]

if all([i > 5 for i in nums]):
    print("All larger than 5")

if any([i % 2 == 0 for i in nums]):
    print("At least one is even")

for v in enumerate(nums):
    print(v)


# All larger than 5
# At least one is even
# (0, 55)
# (1, 44)
# (2, 33)
# (3, 22)
# (4, 11)
```

24. Text Analyzer
    > This is an example project, showing a program that analyzes a sample file to find what percentage of the text each character occupies. This section shows how a file could be open and read.

```py
filename = input("Enter a filename:")

with open(filename) as f:
    text = f.read()

print(text)

# Enter a filename: test.txt
# Traceback (most recent call last):
#  File "hellow.py", line 1, in <module>
#    filename = input("Enter a filename:")
#  File "<string>", line 1, in <module>
# NameError: name 'test' is not defined
```

25. Text Analyzer
    > This part of the program shows a function that counts how many times a character occurs in a string.

```py
def count_chr(text, char):
    count = 0
    for c in text:
        if c == char:
            count += 1
    return count
```

> This function takes as its arguments the text of the file and one character, returning the number of times that character appears in the text. Now we can call it for our file.

```py
filename = input("Enter a filename:")
with open(filename) as f:
    text = f.read()

print(count_char(text, "r"))

# Enter a filename: test.txt
# 83
```

> > The character "r" appears 83 times in the file.

26. Text Analyzer
