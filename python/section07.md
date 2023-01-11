# [section07 반복문 for]

01. for문
	- 값의 범위나 반복 횟수가 정해져 있을 때 사용하면 편리한 반복문이다.
	- while문에 비해서 좀 더 자주 사용한다.
	- 문법
	for 변수 in 반복가능객체:
	     반복실행문

02. 시퀀서(문자열, list, tuple, range)와 for문
	1. 시퀀서와 for문
	```
	a = {'a', 'b', 'c'}
	a = ['a', 'b', 'c']
	a = 'hello'
	a = ('a', 'b', 'c')
	for ch in a:
	    print(ch)	
	```
	3. for문과 list
	```
	list = [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]
	list = [num*2 for num in list]
	list = [ num * 3 for num in list if num % 2 == 0 ]
	```
	6. for문과 range() 함수
	- range는 range(시작숫자, 종료숫자, step)의 형태로 리스트 슬라이싱과 유사합니다.
	- range의 결과는 시작숫자부터 종료숫자 바로 앞 숫자까지 컬렉션을 만듭니다.
	- 시작숫자와 step은 생략가능합니다.
	```
	for n in range(1, 11, 2):
	    print(n)
	```
	```
	for n in range(10):
	    print(n, 'hello')
	```

03. 비시퀀스(set, dict)와 for문
	1. for문과 set
	```
	for item in {'가위', '바위', '보'}:
	    print(item)
	```
	2. for문과 dict
	```
	person = {  'name':'홍길동', 'age':25 }
	for key in person:
	    print(key, person[key])
	```

### MISSION ###
- for문을 이용해 정해진 횟수만큼 반복해서 실행하는 코드를 작성할 수 있다.
- for문을 이용해서 list나 dict와 같은 반복 가능객체의 각 요소를 하나씩 꺼내서 사용할 수 있다.
