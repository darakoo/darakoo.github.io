# [section12 모듈과 import] 

01. 모듈과 import   
    1. 모듈이란? 
        - 변수, 함수, 클래스들을 작성한 파이썬 파일이다. 

    2. 모듈 사용하기
    ```
        방법1
        import 모듈 as 별명

        방법2
        from 모듈 import *
        from 모듈 import 함수 as 별명
        from 모듈 import 함수1, 함수2
    ```

    3. 모듈의 종류
        - 사용자 정의 모듈
        - 표준 모듈 : 파이썬에 기본적으로 설치되어 있는 모듈
        - 외부 모듈 : pip 명령어로 별도 설치를 하여 사용하는 모듈

02. 표준 모듈
    - 표준모듈이란 파이썬에 기본적으로 설치되어 있는 모듈이다.
    - 내장 함수나 메소드로 처리할 수 없는 많은 작업들을 표준 모듈로 해결할 수 있다.
    - 표준 모듈 종류 : math, random, time, datetime
    - <a href="https://docs.python.org/ko/3/library/index.html" target="_blank">모듈 참고 사이트</a>

03. 외부 모듈
    1. 패키지
        - 패키지란 비슷한 성격의 모듈을 모아 놓은 폴더이다.

    2. 패키지 관리자
        - pip 명령어

    3. 패키지 설치
        - pip install 패키지명
    
    4. 패키지 삭제
        - pip uninstall 패키지명

### MISSION ###
- 모듈이란 파이썬으로 작성한 파일을 의미한다.
- 표준 모듈은 파이썬 설치 시 함께 설치되기 때문에 곧바로 사용할 수 있다.
- 외부 모듈은 pip install 명령으로 설치한 후 사용할 수 있다.
- 모든 모듈은 import 후에 사용해야 한다.
