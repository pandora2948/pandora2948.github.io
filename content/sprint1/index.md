---
emoji: ☀️
title: 9월 1주차 스프린트 회고
date: '2022-09-11 22:00:00'
author: 백동재
tags: PS 회고
categories: PS
---

## ✒️ 첫 회고록 작성

개발자라고 하면 모름지기 개발 블로그를 작성해야한다는 말을 예전부터 꾸준히 들어왔었다.

그렇지만 작문 능력이 부족한 나는 항상 그런 얘기들을 무시해오다가 알고리즘 스터디에 참여한 후로부터 내가 배운것들을 오랫동안 보존하고자 회고록에 대해 관심을 갖게 되었다.

학과 공부와 토익 공부, 그리고 개인 알고리즘 공부까지 하루가 부족한 시간이지만 개발자로써 겪고 느낀게 무엇인지 기록해두려고 한다.

---

## 2309 일곱 난쟁이 (Bronze I)

본 문제는 수학적인 계산과 bruteforce알고리즘으로 해결 가능한 문제로, 파이썬에서 지원하는 라이브러리를 통해 조합을 사용하였다.

```python
from itertools import combinations
```

itertools 라이브러리에서 지원하는 조합과 순열을 사용하면 bruteforce 알고리즘을 쉽게 해결 할 수 있다.

```python
import itertools as  itool
list = [1, 2, 3]

for permutations in itool.permutations(list, 3) :
  print(permutations)
>> Result: [1, 2, 3], [1, 3, 2], [2, 1, 3], [2, 3, 1], [3, 1, 2], [3, 2, 1]
위와 같이 두번째 인자값만큼의 길이를 가진 리스트를 반환한다.

for combinations in itool.combinations(list, 3) :
  print(combinations)
>> Result: [1, 2, 3]
순서에 상관없이 각 요소들이 포함되도록 출력한다.
```

위와 같이 조합은 순열과 달리 각 요소들의 위치와 상관없이 포함 여부만 신경쓰므로 본 문제는 조합으로 해결하는것이 적합하다고 판단하였다.

9개의 입력 값 중 7개의 값의 합이 100이 되도록 작성하면 다음과 같다.

```python
...

list = [20, 7, 19...]

for combinations in itertools.combinations(list, 7) :
  if sum(combinations) == True :
    print(combinations)
    break
```

위와 같은 방법으로 문제를 해결할 수 있다.

---

## 2828 사과 담기 게임

본 문제는그리디 알고리즘으로 해결 가능한 문제로 바구니의 범위를 설정하여 좌측 끝 좌표와 우측 끝 좌표 사이에 사과가 떨어지도록 조정하는 문제이다.

좌측 끝 값은 1로 설정되어 있으며, 바구니의 너비 M이 주어지고 1 ~ (M + 1) 이라는 초기 범위를 가지게 되므로 좌측 초기값 을 1, 우측 초기값을 (M + 1) 로 설정하여 범위를 지정하였다.

```python
for position in applePos :
  while position < bucketStart or position > bucketEnd :
    if position > bucketEnd :
      bucketStart += 1
      bucketEnd += 1
      count += 1

    elif position < bucketStart :
      bucketStart -= 1
      bucketEnd -= 1
      count += 1
```

값의 범위를 지정하여 2중 반복문을 통하여 구현하였다.
