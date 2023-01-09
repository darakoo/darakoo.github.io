[ch01 C언어의 기본] - [section03 데이터 표현 방식]

01. 컴퓨터의 데이터 표현 방식
	* 참고 : Appendix 339페이지(정수의 표현과 처리)

	1. 2진수의 이해
	- 컴퓨터는 2진수를 기반으로 데이터를 표현한다.
	- 2진수란 두가지 기호(0, 1)만을 이용해 값을 표현한다.
	
	2. 2진수를 이용한 비트의 표현
	
	3. 10진수를 2진수, 8진수, 16진수 로 표현하기
	- 실습
	
	
02. 정수와 실수
	1. 정수의 표현
	- 비트구성 : 부호비트(Most Signaificant Bit) + 정수
	- 2진수 음의 값 : 2의 보수(모든 비트의 값을 반전 + 1)를 취해야 한다.

	2. 실수의 표현
	- 비트구성 : 부호비트 + 지수부 + 가수부
	- float : 1bit + 8bit + 23bit = 32bit = 4byte
	- double : 1bit + 11bit + 52bit = 64bit = 8byte 
	
03. unsigned 자료형
	- 부호비트를 데이터 표현에 사용하게 되어 값의 표현 범위가 커진다.
	
	1. unsigned 데이터
	[signed 데이터]
	char ch;				// -2의7제곱 ~ 2의7제곱-1
	short sh;				// -2의15제곱 ~ 2의15제곱-1
	int in;					// -2의31제곱 ~ 2의31제곱-1
	
	[unsigned 데이터]
	unsigned char ch;		// 0 ~ 2의8제곱-1(255)
	unsigned short sh;		// 0 ~ 2의16제곱-1(65,535)
	unsigned int in;		// 0 ~ 2의32제곱-1(4,294,967,295)
	
	2. unsigned 자료형의 접미사
	1000U	=> unsigned int
	1000UL	=> unsigned long
	1000ULL	=> unsigned long long
	