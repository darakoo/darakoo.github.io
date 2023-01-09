[ch09 파이썬 예외 처리] - [section17 예외 처리] 

### 목차 ###
01. 예외 처리의 필요성
	1. 예외와 오류
		- 예외 : 개발자가 처리가능한 문제
		- 오류 : 개발자가 처리할 수 없는 문제

	2. 예외 처리의 필요성
		- 프로그램이 비정상적으로 종료되는 것을 막고 사용자에게 문제내용을 전달하기 위함이다.
		- ex) 웹사이트 오류 페이지

02. 예외 처리
	1. 고전적인 예외처리
		- 프로그램 로직에서 처리하는 방식
		- 프로그램이 복잡해지고 모든 예외를 처리하기에는 한계가 있다.
		```
		a = int(input('나누 어질 수를 입력하세요>>>'))
		b = int(input('나눌 수를 입력하세요>>>'))

		if b == 0:
		    print('0으로 나누는 것은 불가능 합니다.')
		else:
		    print(a/b)
		```

	2. 예외의 종류
		- 예외클래스 상속관계 : BaseException => Exception => 기타 예외클래스
		- 예외 발생 시키기
		```
		# ZeroDivisionError: division by zero
		print(2/0)

		# IndexError: list index out of range
		a = [1, 2, 3]
		print(a[3])

		# TypeError: unsupported operand type(s) for /: 'str' and 'int'
		a = '3'
		b = 2
		print(a / b)
		```
		
	3. 예외 처리 방식
		- 모든 예외를 처리하는 방식
		```
		a = int(input('나누 어질 수를 입력하세요>>>'))
		b = int(input('나눌 수를 입력하세요>>>'))

		try:
		    print(a/b)
		except:
		    print('예외가 발생했습니다.')
		```
		- 특정 예외만 처리하는 방식
		```
		a = int(input('나누 어질 수를 입력하세요>>>'))
		b = int(input('나눌 수를 입력하세요>>>'))

		try:
		    print(a/b)	
		except ZeroDivisionError:	# 0으로 나눌 경우
		    print('0으로 나눌 수 없습니다.')
		except ValueError:		# 문자 입력시
		    print('정수만 입력할 수 있습니다.')
		except Exception:		# 이외 예외 처리
		    print('알 수 없는 예외가 발생했습니다.')
		```
		- 예외 메시지 처리하기
		```
		a = [1, 2, 3, 4, 5]
		try:
		    a[10]
		except IndexError as e:
		    print(e)
		```
		- else문과 finally문
		```
		try:
		    a = int(input('나누어 질 수를 입력하세요>>>'))
		    b = int(input('나눌 수를 입력하세요>>>'))
		    result = a / b  # 예외가 발생할 수 있는 구문
		except ZeroDivisionError as e:  # 변수 b가 0일 경우
		    print(e)
		except TypeError as e:         # 변수 a, b가 정수가 아닐 경우 ???
		    print(e)   
		else:       # 예외가 발생하지 않으면 처리되는 구문
		    print(result)
		finally:
		    print('프로그램을 종료 합니다.')
		```
	4. 강제로 예외 발생시키기
	```
	try:
	    raise Exception('강제로 발생시킨 예외')
	except Exception as e:
	    print('발생한 예외 메시지는 다음과 같습니다.')
	    print(e)
	```
	5. 사용자 예외 클래스
	```
	class HourError(Exception):
	    def __init__(self, message='올바른 시간이 아닙니다.'):
		super().__init__(message)

	try:
	    hour = int(input('시간을 입력하세요>>>'))
	    if hour < 0 or hour > 23:
		# raise HourError()
		raise HourError('시간오류')
	except HourError as e:
	    print(e)
	```

### MISSION ###
- try except문으로 파이썬의 모든 예외를 처리할 수 있습니다.
- try문에서 예외가 발생한다면 except문이 발생한 예외를 처리합니다.
- try문에서 예외가 발생하지 않는다면 else문이 실행됩니다.
- try문의 예외 발생 여부와 생관없이 마지막에는 항상 finally문이 실행됩니다.
- 파이썬에 존재하지 않는 예외인 경우에는 직접 Exception클래스를 상속받는 예외 클래스를 생성할 수 있습니다.
