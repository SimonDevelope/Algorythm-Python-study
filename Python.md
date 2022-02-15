#python

##basic

1. print() 출력
2.
3. Exponentiation 제곱, 지수 표현

```py
print( 2**5 )
"""
 2^5의 결과가 나온다.
"""
```

4. Floor division 나누고 소수점 내림(몫을 구한다.)

```py
print(20 // 6)
"""
 3이 결과값으로 나온다.
"""
```

5. Remainder 나눗셈

```py
print (20 % 6)
print(1.25 % 0.5)
```

---

##string

1. print('')내부에서 어퍼스트로피를 쓰고싶은 경우 \'를 입력해주면 된다.

```

```

2. Newlines \n과 \t
   > \n는 다음 줄을 작성할 때 사용하고 \t는 문자열 사이에 탭 간격을 줄 때 사용한다.
   >
   > > '\\'는 문자 '\'를 그대로 사용할 때 사용한다 '\"', '\''는 작은따옴표와 큰따옴표를 그대로 사용할 경우 사용한다.

```py
print('one\ntwo\nthree');

"""
 one
 two
 three
"""

print('one\ttwo\tthree');

"""
 one     two     three
"""
```

3. Multiline

```py
print("""this
is a multiline
text""")

"""
 this
 is a multiline
 text
"""
```

4. String Operation

```py
print("spam" * 3);
print(4 * '2');

"""
 spamspamspam
 2222
"""
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
"""
 [7, 7, 5, 7, 7]
"""
```

9. List Operations
   > List can be added and multiplied in the smae way as strings

```py
nums = [1, 2, 3]
print(nums + [4, 5, 6])
print(nums * 3)
"""
 [1, 2, 3, 4, 5, 6]
 [1, 2, 3, 1, 2, 3, 1, 2, 3]
"""
```

10. List Operations

```py
words = ["spam", "egg", "spam", "sausage"]
print("spam" in words)
print("egg" in words)
print("tomato" in words)

"""
 True
 True
 False
"""
```

11. List Operations
    > To check if an item is not a list, you can use the not operator in one of the following ways

```py
nums = [1, 2, 3]
print(not 4 in nums)
print(4 not in nums)
print(not 3 in nums)
print(3 not in nums)

"""
 True
 True
 False
 False
"""
```

12. List Functions
    > The append method adds an item to the end of an existing list.

```py
nums = [1, 2, 3]
nums.append(4)
print(nums)

"""
 [1, 2, 3, 4]
"""
```

13. List Functions
    > To get the number of items in a list, you can use the len function

```py
nums = [1, 2, 5, 2, 4]

print(len(nums))

"""
 5
"""
```

14. List Functions
    > The insert method is similar to append, except that it allows you to insert a new item at any position in the list, as opposed to just at the end

```py
words = ["python", "fun"]
index = 1
words.insert(index, "is")
print(words)

"""
 ['python', 'is', 'fun']
"""
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
