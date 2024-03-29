# [section19 데이터 분석 개요] 

# 1. 데이터 분석
1. 정의
	- 데이터 분석은 원시 데이터를 실행 가능한 인사이트로 변환하는 것이다.
	- 데이터 분석을 통해 비즈니스 프로세스를 구성하고, 의사 결정을 개선하며, 비즈니스 성장을 증진할 수 있다.

2. 데이터 분석 프로세스
	- 데이터 분석을 수행하는 이유
	- 데이터 수집
	- 데이터 정제
	- 데이터 분석 및 결과 공유

# 2. 자주사용하는 모듈
1. Pandas(판다스)
	1. 공식사이트 : [https://pandas.pydata.org/](https://pandas.pydata.org/)
	2. 개요
		- 표 형태의 데이터를 다루는데 특화된 파이썬 모듈이다.
		- 엑셀의 기능을 제공하는 파이썬 모듈이라고 생각하면 이해가 쉽다.
		- 표 형태의 데이터를 다루기 위한 시리즈(Series)와 데이터프레임(DataFrame) 클래스를 제공한다.
		- Series : 1차원 자료구조를 표현(벡터)
		- DataFrame : 행렬의 표를 표현
		
			<img src="/img/python/pandas.jpg" width="60%" height="60%">

2. Numpy(넘파이)
	1. 공식사이트 : [https://numpy.org/](https://numpy.org/)
	2. 개요
		- Numerical Python으로 수치 계산을 위해 만들어진 파이썬 라이브러리다.
		- 행렬이나 일반적으로 대규모 다차원 배열을 쉽게 처리할 수 있다.
		- 데이터 구조 외에도 수치 계산을 위해 효율적으로 구현된 기능을 제공한다.
		- 행렬, 백터 등의 수치 연산에 활용되기에 "선형대수" 라이브러리이며, 내부적으로 c로 짜여있어 연산속도가 빠르다.

	3. 코드비교(numpy vs python)
	- 파이썬과 비교하여 간결한 코드를 만들 수 있다.

		```
			# y = 2x + 8 (단, 0<=x<20)에서 y의 값에 해당하는 list
			import numpy as np

			# python
			result_py = []
			for n in range(0,20):
			    result_py.append((2*n) + 8)
			print(result_py)

			# numpy
			result_np = 2 * np.arange(0,20) + 8
			print(result_np)
		```

		```
			# [1,2,3]과 [4,5,6]에서 같은 index끼리를 합한 list
			
			import numpy as np
			
			# python
			a_py = [1,2,3]
			b_py = [4,5,6]
			result_py = []
			for idx in range(len(a_py)):
			    result_py.append(a_py[idx] + b_py[idx])
			print(result_py)

			# numpy
			a_np = np.array([1,2,3]) # a_np = np.random.randint(1, 4, size=3) 
			b_np = np.array([4,5,6])
			result_np = a_np + b_np
			print(result_np)
		```

# 3. 데이타 시각화
1. Matplot
	- 공식사이트 : [https://matplotlib.org/](https://matplotlib.org/)
	- MATLAB-인터페이스 기반의 Python 라이브러리이다.
	- 그래프의 디테일한 설정이 가능하다.
2. Seaborn
	- 공식사이트 : [https://matplotlib.org/](https://matplotlib.org/)
	- Matplot 라이브러리를 기반으로 한 통계 전용 시각화툴이다.
	- Pandas 라이브러리와 연계가 잘 된다.
	- 사용법이 비교적 쉽다.


#### 참고
- https://www.youtube.com/@user-xt4sh7kh3n/playlists
- https://yozm.wishket.com/magazine/detail/1567/
- https://laboputer.github.io/
