# [section03 기본 입출력]

01. 표준출력
    - 이스케이프 문자
        - 확장문자이다.
        - 종류 : \', '", \n, \r, \t
    - print() 함수
    ```
    print('hello', 'hello')                         # hello hello
    print('hello', 'hello', sep=':', end='!')       # hello:hello!
    ```

02. 형식을 갖춘 문자열
    - % 연산자
    ```
    a = 10
    b =20
    print('%d' %100)                # 100
    print('%d, %d' %(a, b))         # 10, 20
    ```
    - format() 메소드
    ```
    print('Breakfast is {} and {}'.format('spam', 'eggs'))
    ```
    - f-strings
        - 파이썬 3.6이후 버전부터 사용 가능한 문법이다.
    ```
    age = 25
    print(f'내년에는 {age+1}살이 됩니다.')
    ```
    
03. 표준입력 : input() 함수
    - input 함수는 모든 입력을 문자열(str)로 저장한다.
    ```
    name = input('이름을 입력하세요 >>>')
    age = input('나이를 입력하세요 >>>')

    print(f'입력된 이름은 {name}입니다.')
    print(f'입력된 나이는 {age}살입니다.')
    ```

### MISSION ###
- 파이썬의 표준 출력 함수는 print()이다.
- 파이썬의 표준 입력 함수는 input()이다.
- 파이썬의 표준 입력 함수 input()은 모든 입력을 문자열로 처리하기 때문에 문자열이 아닌 입력은 변환 작업이 필요하다.
- 리스트에 요소를 추가할 때는 append() 메소드나 insert()메소드를 사용하고, 제거할 때는 pop()메소드를 사용합니다.
