1. 복잡도

- 시간복잡도: 알고리즘의 수행 시간 분석
- 공간복잡도: 알고리즘의 메모리 사용량 분석
- 빅오표기법: 가장 빠르게 증가하는 항만을 고려하는 표기법

2. 빅오 표기법

| 순위     | 명칭         |
| -------- | ------------ |
| O(1)     | 상수시간     |
| O(logN)  | 로그시간     |
| O(N)     | 선형시간     |
| O(NlogN) | 로그선형시간 |
| O(n^2)   | 이차시간     |
| O(n^3)   | tkacktlrks   |
| O(2^n)   | 지수시간     |

3. 시간복잡도 계산의 예시

> N개의 데이터의 합을 계산하는 프로그램 예제

```py
array = [3, 5, 1, 2, 4] # 5개의 데이터 (N = 5)
summary = 0 # 합계를 저장할 변수
#모든 데이터를 하나씩 확인하며 합계를 계산 <= 이것 때문에 수행의 갯수는 N에 비례한다는 것을 알 수 있다.
for x in array:
    summary += x

#결과를 출력
print(summary)
```

> 수행 시간은 데이터의 개수 N에 비례할 것임을 예측할 수 있습니다.

- 시간 복잡도: O(N)

---

> 2중 반복문을 이용하는 프로그램 예제

```py
array = [3, 5, 1, 2, 4] # 5개의 데이터(N = 5)

for i in array:
    for j in array:
        temp = i * j
        print(temp)
```

> 시간복잡도: O(N^2)
>
> > 참고로 모든 2중 반복문의 시간 복잡도가 O(N^2)인 것은 아니다. 소스코드가 내부적으로 다른 함수를 호출한다면 그 함수의 시간 복잡도까지 고려해야 한다.