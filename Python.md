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

33. Assertion
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
