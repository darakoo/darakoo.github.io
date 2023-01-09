# [section08 기타 제어문]

01. break문
    - 반복문을 강제로 종료할때 사용하는 제어문이다.
    - if문을 이용해서 반복문을 종료시킬 조건식을 만들고 break문을 사용해 반복문을 종료하면 된다.
    ```
    # n이 5인 경우 반복문을 빠져나온다.
    n = 1
    while n <= 10:
        if n == 5:
            break
        print(n)
        n += 1
    ```

02. continue문
    - continue문을 만나면 continue문 아래 명령은 수행되지 않는다.
    - 반복에서 제외하고 싶은 코드가 존재할 때 사용하기도 한다.
    ```
    # 3의 배수만 출력한다.
    for n in range(1, 10):
        if n % 3 != 0: 
            continue
        print(n)
    ```
    
### MISSION ###
- break문을 이용하면 break문이 포함된 반복문을 곧바로 종료할 수 있다.
- continue문을 이용하면 continue문이 포함된 반복문을 처음부터 다시 실행할 수 있다.
