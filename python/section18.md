# [section18 웹 크롤링의 이해] 

01. 웹 크롤링의 이해
    1. 웹 크롤링이란
        - 웹 페이지에서 필요한 정보를 수집하고 선별하여 추출하는 과정이다.
    2. HTML의 개념과 구조 이해하기
        - html 문법 이해하기
        - class : 여러요소에서중복사용가능, id : 유일한 값 (https://bangu4.tistory.com/26 참고)
        - 웹 사이트 접속 => F12 개발자 도구에서 소스 확인하기
    
    3. URL(Uniform Resource Locator)이란
        - 웹 페이지 주소이다.
        - ex) https://www.naver.com/

02. 웹 크롤링의 준비
    - 크롬 브라우저 설치
    - requests, BeautifulSoup 명령 프롬프트에서 설치하기
        ```
        pip install requests
        pip install BeautifulSoup4        
        ```

03. 웹 크롤링 소스 분석
        ```
        # 1. 외부모듈 import
        import requests
        from bs4 import BeautifulSoup

        # 2. html 소스 추출
        url = 'https://movie.naver.com/movie/bi/mi/basic.nhn'
        param = {'code': 207921}
        response = requests.get(url, params=param)
        html = response.text

        # 3. BeautifulSoup 객체 생성
        soup = BeautifulSoup(html, 'html.parser')

        # 4. 데이터 분석
        review_list = soup.find_all('div', class_='score_reple')
        for review in review_list:
            print(review.find('p').text.strip())
        ```

### MISSION ###
- HTTP 요청을 수행하는 requests 라이브러리를 이용해서 웹 페이지 소스 코드를 가져올 수 있습니다.
- HTML 문서를 쉽게 분석할 수 있는 BeautifulSoup 라이브러리를 통해서 웹 크롤링을 수행할 수 있습니다.
