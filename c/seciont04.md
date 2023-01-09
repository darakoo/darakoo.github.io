[ch01 C언어의 기본] - [section04 기본 입출력 함수]

01. printf 함수(형식화된 출력, f(formatted))
	1. 표현가능한 문자
	- 일반적인 문자 : 알파벳, 숫자 등
	- 제어문자 : \n, \t, \" 등
	- 서식문자 : 
	%d : 정수형
	%x : 16진수 정수(양수만표현)
	%o : 8진수 정수(양수만표현)
	%f : 실수 타입	
	%c : 문자
	%s : 문자열
	%u : 부호없는 정수들
	%% : % 출력
	ex) printf("number is %d\n", number);
	
	2. print formatting
	- 음수를 붙이면 왼쪽정렬
	정수 : %10d, %-10d 
	실수 : %10.3f, %-10.3f

02. scanf 함수(입력)
	1. 서식문자
	%d : 정수형
	%c : 문자
	%s : 문자열
	%lf : double 타입 실수
	%f : float 타입 실수

	2. 입력예시 : 
	scanf_s("%d", &num);							// 정수를 입력 받아 num에 저장한다.
	scanf_s("%d %f", &num1, &num2);
	
	3. 형변환 : 
	scanf_s("%o %x %d", &num1, &num2, &num3);		// 8진수 16진수 10진수
	printf("입력된 정수들 : %d %d %d \n", num1, num2, num3);
	
	* 주의
	2010년 이후 scanf를 보완한 scanf_s 함수가 등장, 최근 컴파일러 중에는 scanf 함수를 사용 못하는 경우가 종종 있다.
	개념적인 접근 미 호환성을 고려하여 scanf() 함수를 사용하겠다.
	코드 가장 첫 번째 줄에 아래와 같이 선언 해야 한다.
	#define _CRT_SECURE_NO_WARNINGS

	

	