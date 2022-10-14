---
emoji: ☀️
title: 10월 2주차 스프린트 회고
date: '2022-10-14 16:00:00'
author: 백동재
tags: PS 회고
categories: PS
---

## 👀 간만의 회고록

9월 2주차 이후로 많은 일들이 있었고, 그 동안 블로그 작성이 멈췄었다.

불행은 한번에 몰려오다고 하던가

정말 쉽지 않은 나날들을 보내고 다시 커리어에 집중하고자 한다.

슬픔, 불안, 분노는 내 인생에 도움이 되지 않으니, 앞으로는 내 인생을 위해 열심히 살아보겠다고 다짐한다.

---

## 25628. 햄버거 만들기 (Bronze IV)

본 문제는 사칙연산과 수학이 접목된 문제로, 두 계산식 중 작은 결과를 출력시켜주면 되는 알고리즘이다.

```python
from sys import stdin

A, B = list(map(int, stdin.readline().strip().split()))

print(min([A // 2, B]))
```

각 A와 B 두 가지 수를 입력 받아 계산을 수행하며, 이들 중 작은 수를 출력하도록 작성한 코드로, A는 2로 나누고 B는 별도의 연산을 수행하지 않으며, 이를 min을 통하여 식별하고, 이를 출력한다.

난이도 자체는 어렵지 않아, 간단하게 풀기 좋은 문제였다고 생각한다.

---

## 25640. MBTI (Bronze IV)

본 문제는 target과 같은 문자열을 탐색하는 알고리즘이다.

target 문자열을 지정하고, 이를 반복문을 통해 비교하여 count 변수를 증가시킨다.

```python
from sys import stdin

target = stdin.readline().strip()
count = 0

for _ in range(int(stdin.readline().strip())):
  if stdin.readline().strip() == target:
    count += 1

print(count)
```

---

## 25641. 균형 잡힌 소떡소떡 (Bronze III)

본 문제는 두 대상(s와 t)를 동일한 갯수가 될 때 까지 왼쪽에서부터 제거하는 문제로, 왼쪽 요소 부터 제거해야 하는 조건 때문에 리스트가 아닌 Deque를 사용하여 해결하였다.

```python
from collections import deque
from sys import stdin

N = int(stdin.readline().strip())

dq = deque(list(stdin.readline().strip()))

while True:
  if dq.count('s') == dq.count('t'):
    break
  dq.popleft()

print(''.join(dq))
```

while 문을 통하여 요소들을 왼쪽에서 부터 제거하며, 비교 대상의 갯수가 같아질 경우 break를 통하여 loop 에서 탈출하도록 하며, 이후 join을 통해 문자로 변환하여 출력한다.

---

## 25642. 젓가락 게임 (Bronze III)

본 문제는 젓가락 게임의 우승자를 계산하여 출력하는 알고리즘으로, 각 더하기 연산의 결과가 5 이상이 되면 상대가 승리하게 되는 게임이다.

예를 들어 a = 2, b = 3 으로 시작하여 a가 선공을 진행 할 경우

(2, 3) => (5, 3) 으로 b가 승리하게 된다.

문제에서는 무조건 A의 선공이 진행되어지므로, isAttack 변수는 True 를 할당하여 A의 공격이 먼저 진행되도록 초기화 한다.

이후 각 턴을 교차시키도록 isAttack 변수를 변경한다.

```python
from sys import stdin

A, B = list(map(int, stdin.readline().strip().split()))

isAttack = True

while True:
  if isAttack:
    B += A
    isAttack = False

  else:
    A += B
    isAttack = True

  if A >= 5:
    print('yj')
    break
  elif B >= 5:
    print('yt')
    break
```

이후 A가 승리 할 경우 yt를 출력, B가 승리 할 경우 yj를 출력하도록 한다.

---

## 💻 후기

이번 스프린트는 알고리즘 문제풀이의 감을 돌리기 위해 간단한 문제를 위주로 풀어보았다.

다음 주가 시험인 만큼 이번 주를 잘 마무리하여 다음 주 시험을 잘 대비하도록 하여야겠다.

여전히 토익학원과 교내근로, 학점관리 및 팀 프로젝트, 그리고 알고리즘 공부까지 꽤나 바쁜 일상을 이어왔다.

꼭 내 노력이 헛되지 않도록 남은 학기도 열심히 살아야겠다.

슬픔을 음미하기엔 내 인생이 너무 바쁘니
