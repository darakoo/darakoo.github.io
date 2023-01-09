# [section13 파일 입출력의 이해] 

01. 파일 입출력의 개요
    1. 지금까지는 터미널 입출력을 다뤘는데 지금부터는 파일을 읽고 파일을 수정, 생성하는 파일 입출력을 다룹니다.

    2. 모드
	    - [파일을 여는 목적]
		    - r(read) : 읽기 => default
		    - w(write) : 기존내용삭제 후 쓰기
		    - a(append) : 기존내용유지 후 추가

	    - [파일 종류]
		    - t : 텍스트 파일 => default
		    - b : 바이너리(텍스트 외의 모든 파일) 파일

	    - [모드종합]
		- rt, rb, wt, wb, at, ab

02. 파일 생성
    1. 텍스트 파일생성
    ```
	    file = open('hello.txt', 'wt')
	    print('file.txt 파일이 생성되었습니다.')
	    file.close()
    ```

    2. 텍스트 파일생성 -with문 사용
	    - 파일 입출력에 문제가 있을 경우 예외처리 문법이다.
	    - with 구문을 사용하면 close() 메소드를 생략할 수 있다.
    ```
	    with open('hello.txt', 'wt') as file:
		print('파일이 생성되었습니다.')
    ```    
    3. 텍스트 파일에 내용 추가하기
	```
		file = open('hello.txt', 'at', encoding='utf-8')
		file.write('내용을 추가합니다.')
		file.close()
	```

03. 파일 읽기
    1) read
	    - 파일 전체를 한 번에 읽어 들인다.
	    - 한번에 읽어 들일 양이 많을 경우 많은 메모리 공간이 필요 할 수 있다. 
	```
		file = open('hello.txt', 'rt', encoding='utf-8')
		str = file.read()
		print(str)
		file.close()
	```
	    
    2) readline
	    - 한줄씩만 읽는다.
	    - 더 이상 읽어 들일 데이터가 없으면 빈문자열('')을 반환 한다.
	```
		# 방법1
		while str != '':
		    str = file.readline()
		    print(str, end='')

		# 방법2
		while True:
		    str = file.readline()
		    if str == '':
			break
		    print(str, end='')
		file.close()
	```
	
    3) readlines
	    - 전체 라인을 모두 읽어 각 라인 단위로 리스트에 저장한다.
	```
		file = open('hello.txt', 'rt', encoding='utf-8')
		line_list = file.readlines()
		for line in line_list:
		    print(line.strip('\n'))     # 문자열 끝에 개행을 없앤다.
		file.close()
	```
	
### MISSION ###
- 파일 입출력은 open() 함수로 파일객체를 생성한 뒤 처리 할 수 있다.
- r 모드는 파일 입력 모드이다. 파일의 내용을 읽어 들일 수 있다.
- w 모드는 파일 출력 모드이다. 파일에 새로운 내용을 기록할 수 있다.
- a 모드는 파일 추가 모드이다. 파일의 기존 내용을 유지하고 새로운 내용을 추가할 수 있다.

