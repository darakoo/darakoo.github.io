# [section15 클래스와 객체1] 

01. 클래스 도입의 필요성
	- 절차지향언어(Procedural Programming) vs 객체지향언어(Object Oriented Programming)
	- 절차지향언어 : 대표적으로 c언어가 있다. 위에서 아래로 순차적으로 처리된다.
	- 객체지향언어 : 코드의 재사용성, 신뢰성 높은 프로그래밍, 코드 관리의 편리함

02. 클래스와 객체
	1. 클래스의 개념
		- 구현하고자 하는 객체의 속성과 기능들을 정의하는 설계도이다.
		- 속성은 변수, 기능은 메서드로 나타낸다.

	2. 객체의 개념
		- 클래스를 통해 만들어진 형태

	5. 클래스 정의와 객체 생성
	```
		# 클래스 정의
		class Person:
		    def who_am_i(self):
			print('클래스 실행구문')

		# 객체 생성
		boy = Person()
		boy.who_am_i()
	```

03. 클래스의 구성
	1. 클래의 기본 구성
		- 값 : 이름, 나이, 연락처, 주소            => 변수로 표현
		- 기능 : 잔다, 먹는다, 공부한다, 달린다.    => 메소드로 표현
	2. 인스턴스 변수와 인스턴스 메소드
	```
		# 클래스 정의
		class Person:
		    def who_am_i(self, name, age, tel, address):	# 인스턴스 메소드
			self.name = name	# 인스턴스 변수    
			self.age = age		# 인스턴스 변수
			self.tel = tel		# 인스턴스 변수
			self.address = address	# 인스턴스 변수
		    def sleep(self):					# 인스턴스 메소드
			print('I am sleeping')
		    def study(self):					# 인스턴스 메소드
			print('I am studying')       

		# 객체(인스턴스)생성
		person = Person()

		# 인스턴스 메소드 호출
		person.who_am_i('john', 15, '123-1234', 'toronto')
		person.sleep()
		person.study()
	```

### MISSION ###
- 객체란 현실 세계에 존재하는 모든 것들을 프로그래밍으로 표현한 것입니다. 사람, 자동차, 컴퓨터 등 눈에 보이는 모든 것들이 객체입니다.
- 클래스란 객체를 만들기 위해 객체가 가지는 값과 기능을 프로그래밍으로 구현한 것입니다.
- 사실 파이썬에는 변수가 없습니다. 변수는 모두 객체입니다.
