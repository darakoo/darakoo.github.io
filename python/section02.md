# [section02 변수와 자료형]


01. 주석
	- 한줄주석 : #
	- 여러줄주석 : ''' 내용추가 '''
	- Docstring, 여러줄주석 : """ 내용추가 """
	
	```
	'''
	파일명: circle.py
	개요: 반지름을 전달하면 원의 넓이를 반환하는 get_area() 함수
	'''
	import math

	# get_area() 함수 정의
	def get_area(radius):
	    """
	    반지름을 입력 받아서 원의 넓이를 반환하는 get_area() 함수
	    사용예) get_area(2)
	    """
	    area = math.pi * math.pow(radius, 2)
	    return area

	area = get_area(1.5)
	print(area)
	print(get_area.__doc__)
	```

02. 변수
	- 정의 : 데이터가 저장되는 메모리 공간
	- 변수명 생성규칙
		- 키워드*를 사용하면 안 됩니다.
		- 특수 문자는 언더 바(_ )만 허용됩니다.
		- 숫자로 시작하면 안 됩니다.
		- 공백을 포함할 수 없습니다.
		- 가급적 알파벳을 사용해주세요.
		- 유의미한 뜻으로 짓되 누구나 알 수 있어야 합니다.
		- <a href="https://wordic.loeaf.com/variable-name" target="_blank">공통표준용어참고</a>
	```
	name = 'Alice'      
	age = 25
	address = '''우편번호 12345
	서울시 영등포구 여의도동
	서울빌딩 501호'''
	boyfriend = None
	height = 168.5
	```

	- 동적타이핑은 자료형 검사가 런타임 동안 진행되며 PHP, python, Ruby 등의 인터프리터 언어가 이에 해당된다.
	- 정적타이핑은 자료형 검사가 컴파일타임 동안 진행되 C, C++, JAVA 등의 컴파일 언어가 이에 해당된다.
	```
	[python]
	a = 10 
	a = 3.14 
	a = 'hello' 
	```
	```
	[java]
	int a = 10;
	float b = 3.14;
	String c = "hello";
	```
 
03. 자료형 : 기본형
	- 정수, 실수, 문자열, 논리
	```
	a1 = 10     	# 정수(int)  
	a2 = 10.3	# 실수(float)
	a4 = "hello"	# 문자열(str)
	a5 = True	# 논리(bool)
	```
 	- 형변환
	```
	str(3.14)
	str(100)	
	int('100')	
	float(100)	
	```
	- 문자열 인덱싱
	```
	s[인덱스번호]
	s = 'hello'
	s[0] 	# h
	s[4]	# o
	```
	- 문자열 슬라이싱
	```
	s[start:stop:step] 
	s[0:3] 
	s[3:] 
	s[-4:-2]
	```
04. 자료형 : 컬렉션형
	- 여러 값을 하나의 이름으로 묶어서 관리하는 자료형이다
	
	1. list
	```
	a = [1,2,3] 
	```
	2. tuple : 값을 변경할 수 없는 리스트
	```
	a = (1,2,3)
	a = 1,2,3
	a = 1,
	```
	3. set
 	- 수학의 집합의 개념을 구현한 자료형이다.
	- 순서가 없기 때문에 인덱싱과 슬라이싱을 사용 할 수 없다.
	```
	a = {1,2,3}
	```		
	4. dict
	```
	a= {	'cat':'고양이',
		'mouse':'생쥐',
		'fish':'물고기' }
	a['cat']		 # 값 읽기
	a['dog'] = '개'		# 요소추가
	```

05. mutable과 immutable
	1. mutable
	- 생성된 후 할당된 메모리 주소에서 값 변경이 가능하다.
	- list, set, dict
	2. immutable
	- 생성된 후 값 변경시 다른 메모리 주소에서 새롭게 생성된다.
	- int, float, str, tuple

### MISSION ###
- 파이썬의 변수는 값을 저장하는 메모리 공간입니다.
- 기본 자료형으로 int, float, str, bool이 있습니다.
- int(), float(), str(), bool() 함수를 이용해 다른 자료형의 객체로 변환할 수 있습니다.
- list 자료형은 여러 객체를 저장하고 저장된 객체를 수정할 수 있습니다.
- tuple 자료형은 여러 객체를 저장하지만 저장된 객체를 수정할 수 없습니다.
- set 자료형은 값이 중복되지 않은 여러 객체를 저장할 수 있습니다.
- dict 자료형은 키와 값의 조합으로 구성된 여러 객체를 저장 할 수 있습니다.
