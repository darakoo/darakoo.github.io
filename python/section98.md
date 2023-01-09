##  Naming Rule
1. 함수명
- 소문자 + 밑줄
- 처음에는 기능의 의미가 들어가면 좋다.
get_today_prices (Get_today_prices X)
insert_target_stock(O)

2. 변수명
- 소문자 + 밑줄
school_name (School_name X, SchoolName X)

3. 전역변수명
- g + 밑줄 + 변수명
g_school_name

4. 모듈명(파일명)
- 함수명규칙과 동일하나 최대한 짧은 소문자로 이름짓는다.
naver_stock_crawl.py (Naver_Stock_Crawl.py X)
stock_data_parser.py
- 기존 파일명과 중복될 수 있으니 너무 일반적인 단어는 지양
practice.py, tests.py 

5. 폴더명 : 모듈명규칙과 동일
ml_analyser (ML_analyser X)
bookmark, blog, myblog (단어 또는 합성단어)

6. 클래스명 & Exception명
- UpperCamelCase 적용, 단어는 모두 대문자로 시작
- 밑줄 사용하지 말것
NaverStockPrice (Naver_Stock_Price X)
NaverHistPrice (Naverhistprice X)
DataSplit (Datasplit X, dataSplit X, DATASPLIT X)
Predictors
PtBuilder (PTBUILDER X)

7. 상수
- 모두 대문자로 사용, 밑줄사용 가능
WINDOW_SIZE
TIME_LAGS
PATH
DATA_PATH
