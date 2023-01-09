[ch04 문자열과 함수] - [section13 문자와 문자열]

01. 문자열과 포인터
	1. 배열 기반의 문자열 선언
	char greet1[] = "hello";
	- 문자열의 끝은 NULL이 자동 추가된다.
	- 따라서 길이가 ???인 배열로 초기화 된다.
	
	2. 포인터 기반 문자열 선언
	char *greet2 = "hello";
	
	printf("%s %s", greet1, greet2);
	
02. 문자열 관련 함수
	1. 문자 단위 입출력 함수
		char ch = getchar();
		putchar(ch);
	
		- 키보드로부터 하나의 문자를 입력받는 함수이다. 
		- 입력받은 값은 내부 버퍼(임시 저장공간)에 저장된다.
		
	3. 문자열 단위 입출력 함수
		char ch[30];
		gets(ch);
		puts(ch);
		
		- 입력되는 문자열 끝에 자동으로 널 문자가 추가
		- puts("hello") : 자동줄바꿈되고, printf()기능 대체가능
	
	4. 문자열 처리 함수
		#include <string.h>
		- 문자열 처리 표준 함수를 사용 하려면 string.h 파일을 프로그램에 포함 시켜야 한다.
		
		문자열 관련 주요 함수
		srlen(str); 					// 
		strcpy(str1, str2);				// 
		strncpy(str1, str2, count);		// 
		strcat(str1, str2);				// 
		strncat(str1, str2, count);		// 
		strcmp(str1, str2);				// 
		strncmp(str1, str2, count);		// 
	
		라이브러리 참고 사이트
		https://en.wikipedia.org/wiki/C_standard_library
		http://www.cplusplus.com/reference/clibrary/
		
============================================================================================

[ch04 문자열과 함수] - [section13 문자와 문자열]

01. 문자열과 포인터
	1. 배열 기반의 문자열 선언
	char greet1[] = "hello";
	- 문자열의 끝은 NULL이 자동 추가된다.
	- 따라서 길이가 6인 배열로 초기화 된다.
	
	2. 포인터 기반 문자열 선언
	char *greet2 = "hello";
	
	printf("%s %s", greet1, greet2);
	
02. 문자열 관련 함수
	1. 문자 단위 입출력 함수
		char ch = getchar();
		putchar(ch);
	
		- 키보드로부터 하나의 문자를 입력받는 함수이다. 
		- 입력받은 값은 내부 버퍼(임시 저장공간)에 저장된다.
		
	3. 문자열 단위 입출력 함수
		char ch[30];
		gets(ch);
		puts(ch);
		
		- 입력되는 문자열 끝에 자동으로 널 문자가 추가
		- puts("hello") : 자동줄바꿈되고, printf()기능 대체가능
	
	4. 문자열 처리 함수
		#include <string.h>
		- 문자열 처리 표준 함수를 사용 하려면 string.h 파일을 프로그램에 포함 시켜야 한다.
		
		문자열 관련 주요 함수
		srlen(str); 					// null문자를 제외한 문자열 길이 반환
		strcpy(str1, str2);				// str2 문자열을 str1 주소에 복사
		strncpy(str1, str2, count);		// str2 문자열을 str1 주소에 count 갯수 만큼 복사
		strcat(str1, str2);				// str1에 str2를 이어 붙이기 
		strncat(str1, str2, count);		// str1에 str2를 count 갯수 만큼 이어 붙이기 
		strcmp(str1, str2);				// 문자열을 비교하여 내용이 같으면 0, 다르면 1을 반환
		strncmp(str1, str2, count);		// count 갯수 만큼 문자열을 비교한다.
	
		라이브러리 참고 사이트
		https://en.wikipedia.org/wiki/C_standard_library
		http://www.cplusplus.com/reference/clibrary/

	

	
	
	
