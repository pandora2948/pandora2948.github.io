---
emoji: ๐
title: 9์ 2์ฃผ์ฐจ ์คํ๋ฆฐํธ ํ๊ณ 
date: '2022-09-17 20:00:00'
author: ๋ฐฑ๋์ฌ
tags: PS ํ๊ณ 
categories: PS
---

## โ๏ธ 2์ฃผ์ฐจ ํ๊ณ ๋ก

์ถ์์ด ์ง๋๊ณ  ์ฌ๋ฆ์ด ๋๋๋์ค ์์์ง๋ง, ๋ค์ ๋ ์จ๊ฐ ๋จ๊ฑฐ์์ก๋ค.

์ฐํด๊ฐ ์ง๋ํ๋ผ ์ ์ ์๋ ์ผ์ฃผ์ผ์ ๋ณด๋ด์๋ค.

ํ๋ก์ ํธ ๊ธฐํ, ์๊ณ ๋ฆฌ์ฆ ๊ณต๋ถ ๋ฐ ํ์  ๊ด๋ฆฌ, ๊ทธ๋ฆฌ๊ณ  ์์ด ๊ณต๋ถ์ ๊ต๋ด ๊ทผ๋ก๊น์ง ์ ์ ์๋ ํ ์ฃผ๊ฐ ๋์๋ค.

๊ฐ์ฅ ๋ฐ์๊ณ  ์ ์ ์๋ ํ ํ๊ธฐ๊ฐ ๋๊ฒ ์ง๋ง, ํ  ์ ์๋ ๋งํผ ๋๊น์ง ์ต์ ์ ๋คํด๋ณด๊ณ ์ ํ๋ค.

---

## 1032. ๋ช๋ น ํ๋กฌํํธ (Bronze I)

๋ฌธ์ ๋น๊ต์ ๊ตฌํ์ด ์ฃผ๋ฅผ ์ด๋ฃจ๋ ๋ฌธ์ ๋ก, ์๋ ฅ๋ ๋ฌธ์์ด๋ค์ ๊ฐ ์์น์ ๋ชจ๋ ๋์ผํ ๋ฌธ์๊ฐ ์์นํ  ๊ฒฝ์ฐ ์ถ๋ ฅ์ ํด๋น ๋ฌธ์๋ก, ์๋๊ฒฝ์ฐ ? ๋ก ์ถ๋ ฅํ๋๋ก ๊ตฌํํ๋ ๋ฌธ์ ์ด๋ค.

> ์๋ ฅ
>
> <b>config</b>.sys
>
> <b>config</b>.inf
>
> <b>config</b>ures
>
> ---
>
> ์ถ๋ ฅ
>
> <b>config</b>????

์์ ๊ฐ์ด ๋ชจ๋  ๋ฌธ์์ด๋ค๊ฐ ์ค๋ณต๋์ด์ง๋ ๋ฌธ์๋ง ์ถ๋ ฅ๋๋๋ก ํด์ผํ๋ค.

๋ณธ ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด ๊ณ ๋ฏผํ๋ ๋ ๊ฐ์ง ๋ฐฉ๋ฒ์ ๋ฌธ์์ด์ ๋จผ์  ๋น๊ตํ ๊ฒ์ด๋, ๋ฌธ์์ ์์น๋ฅผ ๋จผ์  ๋น๊ตํ ๊ฒ์ด๋ ์๋ค.

์ดํ ๋ฌธ์์ ์์น๋ฅผ ๋จผ์  ๋น๊ตํ๋๊ฒ์ด ๊ตฌํ์ด ๊ฐ๋จํ๋ค๊ณ  ์๊ฐ๋์๊ณ , ํด๋น ๋ฐฉ๋ฒ์ ํตํด ๊ตฌํํ๊ธฐ๋ก ๊ฒฐ์ ํ์๋ค.

```python
result = list()

for i in range(charLength) :
  char = list(commands[0])[i]
  count = 1

  for j in range(1, len(commands)) :
    if char == list(commands[j])[i] :
      count += 1

  if count == N :
    result.append(char)

  else :
    result.append("?")

print("".join(result))
```

๊ฐ ๋ฌธ์ ์์น๋ฅผ ๋จผ์  ๊ฒฐ์ ํ๊ณ , ์ฒซ๋ฒ์งธ ๋ฌธ์์ด์ ๋ฌธ์๋ฅผ ๊ธฐ๋ณธ์ผ๋ก ์ค์ ํ์๋ค.

์ดํ ๋๋จธ์ง ๋ฌธ์์ด๋ค๊ฐ์ ๋น๊ต๋ฅผ ํตํด count ๋ณ์์ ์๋ฅผ ๋ณ๊ฒฝํด์ฃผ์๊ณ , ๊ทธ ๊ฐ์ด ๋ฌธ์์ด์ ๊ฐฏ์์ ๋ง์ผ๋ฉด ๊ฒฐ๊ณผ์ ํด๋น ๋ฌธ์๋ฅผ, ์๋๊ฒฝ์ฐ ?๋ฅผ ์ ์ฅํด์ฃผ์๋ค.

์ดํ join ์ ํตํด ๋ฌธ์์ด๋ก ๋ณํ ํ ์ถ๋ ฅํด์ฃผ์๋ค.

---

## 1299. Replace Elements with Greatest Element on Right Side

๋ฐฐ์ด์ ๋ค๋ฃจ๋ ๋ฌธ์ ๋ก, ๋ฐฐ์ด์ ์ฐ์ธก ๋๋ถํฐ ์ข์ธก์ผ๋ก ๊ฐ์๋ก ํฐ ๊ฐ์ด ๋๋๋ก ๊ตฌ์ฑํ๋ฉฐ, ๊ฐ์ฅ ์ฐ์ธก์ ๊ฐ์ -1 ๋ก ์ค์ ํ๋ฉฐ, ์ฐ์ธก์ ๊ฐ๋ณด๋ค ์์ ๊ฐ๋ค์ ์ฐ์ธก์ ์์นํ ๊ฐ์ฅ ํฐ ๊ฐ์ผ๋ก ๋์ฒด๋์ด์ง๋ค.

> ![](./img1.png)

์์ ๋ฐฐ์ด์ด ์ฃผ์ด์ง ๊ฒฝ์ฐ, ์๋์ ๋ฐฐ์ด๋ก ๋ณํ๋์ด์ผํ๋ค.

> ![](./img2.png)

๋ณธ ๋ฌธ์ ๋ฅผ ๋๊ฐ์ง ๋ฐฉ๋ฒ์ผ๋ก ํด๊ฒฐํด๋ณด์์ง๋ง, ํ๊ฐ์ง ๋ฐฉ๋ฒ์ ์๊ฐ ์ด๊ณผ๊ฐ ๋์๊ณ , ๋ค๋ฅธ ํ๋์ ๋ฐฉ๋ฒ์ ํต๊ณผํ์๋ค.

๋จผ์  ์๊ฐ ์ด๊ณผ์ ํ์ด๋ฅผ ์๊ฐํ๊ณ ์ ํ๋ค.

### 1๋ฒ์งธ ํ์ด

```python
for i in range(len(arr)) :
  maxNum = -1

  for j in range(i + 1, len(arr)) :
    if maxNum < arr[j] :
      maxNum = arr[j]
  arr[i] = maxNum
```

์ข์ธก์์๋ถํฐ, ์ฐ์ธก์ผ๋ก ์ ๊ทผํ์ฌ ํ์ฌ ์์น์ ์ฐ์ธก์ ์์นํ ๊ฐ์ ์ต๋๊ฐ์ผ๋ก ์ค์ ํ๊ณ , ์ดํ ๋ชจ๋  ์ฐ์ธก์ ๊ฐ๋ค์ ๋น๊ตํ์ฌ ์ต๋๊ฐ์ ์ค์ ํ๋ค.

์ดํ ํ์ฌ ์์น์ ๊ฐ์ ์ต๋ ๊ฐ์ผ๋ก ์ค์ ํ๋ค.

๋ณธ ํ์ด ๋ฐฉ๋ฒ์ 2์ค ๋ฐ๋ณต๋ฌธ์ ํตํด ์ธ๋ฑ์ฑ ํ๋ฏ๋ก, O(n<sup>2</sup>)์ ์คํ๋ณต์ก๋๋ฅผ ๊ฐ๋๋ค.

๋ฐ๋ผ์ ์๊ฐ ์ด๊ณผ๊ฐ ๋ฐ์ํ์๋ค.

### 2๋ฒ์งธ ํ์ด

```python
maxNum = -1

for i in range(len(arr) - 1, -1, -1) :
  cur = arr[i]
  arr[i] = maxNum
  if maxNum < cur :
      maxNum = cur
```

์ฒซ๋ฒ์งธ ํ์ด์ ๋ค๋ฅด๊ฒ ๋จ ํ๋์ ๋ฐ๋ณต๋ฌธ๋ง์ ์ฌ์ฉํ๊ธฐ ๋๋ฌธ์ O(n)์ ์คํ๋ณต์ก๋๋ฅผ ๊ฐ๊ฒ ๋์ด ์๊ฐ ์ด๊ณผ๊ฐ ๋ฐ์ํ์ง ์๋๋ค.

๋ณธ ํ์ด ๋ฐฉ๋ฒ์ ์ฐ์ธก ๋๋ถํฐ ์ข์ธก ๋๊น์ง ์ด๋ํ๋ฉฐ, ์ ์ ์์น์ ์ ๊ณต๋์ด์ง ์ต๋๊ฐ์ ํ์ฌ ์์น์ ๋ฃ๊ฒ๋๋ค.

์ดํ ํ์ฌ ๊ฐ์ด ๋ ํฐ ๊ฒฝ์ฐ, ๋ค์ ์์น์์ ์ฌ์ฉํ  ์ต๋๊ฐ์ ํ์ฌ ๊ฐ์ผ๋ก ์ง์ ํ๊ณ , ๋ค์ ์์น๋ก ์ด๋ํ๋ค.
