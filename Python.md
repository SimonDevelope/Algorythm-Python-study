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
"""py

"""
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
