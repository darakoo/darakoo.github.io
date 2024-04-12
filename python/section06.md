# [section06 반복문 while]

01. while문
```
n = 1
while n <= 10:
  print(n, end=' ')
  n += 1
```
```
print()
n = 10
while n >= 1:
  print(n, end=' ')
  n -= 1
```
```
while True:
  pwd = input('비밀번호를 입력하세요 >>> ')
  if pwd == "0000":
   print('비밀번호를 맞혔습니다.')
   break
```
### MISSION ###
- while문을 이용하면 특정 조건을 만족하는 동안 계속해서 실행되는 코드를 작성할 수 있다.
- while문에서 반복 실행되는 코드는 반드시 들여쓰기 후 작성해야 한다.
