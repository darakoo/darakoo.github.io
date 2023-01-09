# [section11 사용자 함수]

01. 사용자 함수
    - 사용자 함수란 사용자가 직접 만드는  함수

02. 사용자 함수 용어
    1. 함수 용어 정리
        - 인수, 매개변수, 반환값

    2. 함수 정의
    ```
        def 함수이름(매개변수):
            기능구현
            return 반환값
    ```
    
    3. 함수 호출
    ```
        함수이름(인수)
        변수 = 함수이름(인수)
    ```
    
    4. 문법
    ```
        # 함수정의
        # num1, num2 => 매개변수
        # sum => 반환값
        def add(num1, num2):
            sum = num1 + num2
            return sum

        # 함수호출
        # 1, 2 => 인수
        add(1, 2)   
    ```
    
03. 인수(argument)와 매개변수(parameter)
    1. 매개변수
    2. 가변 매개변수
    ```
        def add(*args):
            print(f'{args}의 합은 {sum(args)}입니다.')

        add(1,2)    
        add(1,2,3)
        add(1,2,3,4)
    ```
    
    3. 디폴트 매개변수(기본 매개변수)
    ```
        def greet(message='안녕하세요'):
            print(message)

        greet('반갑습니다')     # 반갑습니다
        greet()                # 안녕하세요
    ```

04. 반환값
    - 반환값이란 함수 호출 결과값 또는 return 값을 말한다.
    <br/>
    
    1. 반환값이 있는 함수
    ```
        def bigger(n1, n2):
            if n1 > n2:
                return n1
            else:
                return n2

        print(bigger(1, 3))
    ```
    
    2. 다중 반환
    ```
        def calculator(*args):
            return sum(args), sum(args)/len(args), max(args), min(args)

        a, b, c, d = calculator(1, 2, 3, 4, 5)
        print('합계', a)
        print('평균', b)
        print('최댓값', c)
        print('최솟값', d)

        result = calculator(1, 2, 3, 4, 5)
        print('합계', result[0])
        print('평균', result[1])
        print('최댓값', result[2])
        print('최솟값', result[3])
    ```
    
    3. 함수의 종료를 위한 return
    ```
        def charge(energy):
        if energy < 0:
            print('0보다 작은 에너지는 충전할 수 없습니다.')
            return  # charge( ) 함수의 종료, 아래 코드가 실행되지 않는 것을 확인한다.
        print('에너지가 충전되었습니다.')
    ```

05. 지역변수와 전역변수
    1. 지역변수(local variable)
        - 함수 내부에서 선언한 변수이며 함수 내부에서만 사용할 수 있다.
    2. 전역변수(global variable)
        - 함수 외부에서 선언한 변수이며 함수 내부, 외부에서 모두 사용할 수 있다.

    ```
        # 지역변수
        def f():
            a = 10
            print(a)

        # print(a) # 구문오류

        # 전역변수(반드시 필요한 경우가 아니면 사용하지 않는 것을 추천한다.)
        b = 10
        def f():
            global b    # 전역변수를 변경할 경우
            b = 20
            print(b)

        print(b)  
    ```


### MISSION ###
- def 키워드를 통해서 새로운 함수를 정의할 수 있다.
- 함수에 전달하는 값을 인수라고 한다.
- 인수를 저장하는 변수를 매개변수라고 한다.
- 함수의 변환값이 존재하는 경우 return문을 통해 반환할 수 있다.
- 반환값이 없는 함수에서 return문을 사용하면 함수를 종료할 수 있다.

