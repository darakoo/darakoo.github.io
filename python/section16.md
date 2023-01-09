# [section16 클래스와 객체2] 

01. 생성자와 소멸자
	- '__' 로 시작 하는 메소드들은 파이썬에 의해서 미리 기능과 역할이 부여된 메소드이다.
	1. 생성자 :  __init__()
		- 객체를 생성하고 값을 초기화 한다.
		- 리턴 값이 없다.
	2. 소멸자 : __del__()
	 	- 인스턴스가 소멸될 때 자동으로 호출되는메소드이다.
	```
	class Candy:
	    # 생성자
	    def __init__(self, shape, color) -> None:
		print('init called')
		self.shape = shape
		self.color = color
	    # 소멸자
	    def __del__(self):
		print('del called')

	candy = Candy('square', 'blue')
	print(candy.shape)
	print(candy.color)
	```

02. 클래스 메소드와 정적 메소드
	1. 클래스 변수
		- 클래스 이름으로 접근 가능한 변수
	2. 클래스 메소드
		- 클래스 변수를 멤버로 가지는 메소드
	```
	class Korean:
	    # 클래스 변수
	    country = 'korea'
	    
	    # 클래스 메소드
	    @classmethod
	    def trip(cls, country):
		if cls.country == country:
		    print('국내 여행입니다.')
		else:
		    print('해외 여행입니다.')
	
	# 클래스 변수, 메소드는 객체 생성없이 클래스 이름으로 접근이 가능하다.
	Korean.trip('korea')
	Korean.trip('japan')
	print("클래스 변수 : ", Korean.country)
	```
	3. 정적 메소드 : 
		- self, cls를 사용하지 않기 때문에 인스턴스변수, 클래스변수를 사용하지 않는다.
		- 인스턴스를 생성하지 않아도 사용할 수 있다.
	```
	class Korean:
	    country = 'korea'

	    @staticmethod
	    def slogan():
		print('Korea Fighting')

	Korean.slogan()
	```
	
03. 상속
	1. 상속이란?
		- 객체의 변수와 메소드를 다른 객체가 사용하도록 물려주는 기능이다.
		- 자식 클래스는 부모 클래스의 멤버를 재활용할 수 있다.
	2. 상속 관계 구현
	```
	# 부모 클래스
	class Person:
	    def __init__(self, name) -> None:
		self.name = name

	    def eat(self, food):
		print(self.name + '가 ' + food + '를 먹습니다.')

	    def sleep(self):
		print(self.name + '가 자고 있습니다.')
	
	# 자식 클래스
	class Student(Person):
	    def __init__(self, name, school) -> None:
		super().__init__(name)	# 부모의 생성자를 호출해야 한다.
		self.school = school

	    def study(self):
		print(self.name + '는 ' + self.school + '에서 공부를 합니다.')

	stu1 = Student('철수', 'sbs')
	stu1.eat('사과')   # 부모 기능
	stu1.sleep()       # 부모 기능	
	stu1.study()       # 자식 기능
	```

### MISSION ###
- 인스턴스를 생성할 때는 생성자가 자동으로 호출됩니다. 생성자 이름은 __init__입니다.
- 인스턴스가 소멸될 때는 소멸자가 자동으로 호출됩니다. 소멸자 이름은 __del__입니다.
- 클래스 변수는 해당 클래스를 기반으로 만든 모든 인스턴스가 공유할 수 있는 변수입니다. 
	인스턴스마다 생성되지 않고 클래스에 하나만 생성됩니다.
- 클래스 메소드는 인스턴스가 없어도 클래스를 이용해 호출할 수 있으며 cls를 이용해서 클래스 변수를 사용할 수 있습니다.
- 정적 메소드도 인스턴스 없이 클래스를 이용해서 호출할 수 있지만 cls를 사용할 수 없습니다.
- 상속을 이용하면 슈퍼 클래스의 기능을 사용하면서 추가 기능을 가지는 서브 클래스를 만들 수 있습니다.
