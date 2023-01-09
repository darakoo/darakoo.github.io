[ch05 메모리 관리와 구조체] - [section18 메모리 동적 할당]

01. 메모리의 동적 할당(dynamic memory allocation)
	- ???? 영역은 사용자에 의해 메모리 공간이 동적으로 할당되고 해제된다.
	- 데이타영역과 스택영역에 할당되는 메모리의 크기는 컴파일 타임에 결정되는 것에 반해 동적 할당은 프로그램 실행 시 메모리 크기를 결정하여 할당 받을 수도 있다.
	
02. 코드 설명
	- #include <stdlib.h> 헤더파일을 include 해야 한다.

	???(memory Allocation) : Heap 영역에 메모리 할당한다.
		자료형* 포인터명 = (자료형*)malloc(sizeof(자료형) * 길이);
		(int*)malloc(sizeof(int) * 5);
		
	???((clear Allocation) : 할당된 메모리에 기본값으로 초기화한다.
		자료형* 포인터명 = (자료형*)calloc(길이, sizeof(자료형));
		(int*)calloc(5, sizeof(int));	
		
	???((resize Allocation) : 동적 메모리 사이즈를 변경한다.
		포인터명 = (자료형*)realloc(포인터명, sizeof(자료형)*길이);
		(int*)realloc(dAr, sizeof(int) * 8);

	???( : 동적 메모리 해제
		free(포인터명);
		메모리를 해제하지 않으면 프로그램이 종료될때까지 사라지지 않고 남아있기 때문에
		꼭 반드시 free함수로 메모리 해제를 해줘야 한다.
	
================================
[ch05 메모리 관리와 구조체] - [section18 메모리 동적 할당]

01. 메모리의 동적 할당(dynamic memory allocation)
	- 힙 영역은 사용자에 의해 메모리 공간이 동적으로 할당되고 해제된다.
	- 데이타영역과 스택영역에 할당되는 메모리의 크기는 컴파일 타임에 결정되는 것에 반해 동적 할당은 프로그램 실행 시 메모리 크기를 결정하여 할당 받을 수도 있다.
	
02. 코드 설명
	
	- #include <stdlib.h> 헤더파일을 include 해야한다.

	malloc(memory Allocation) : Heap 영역에 메모리 할당한다.
		자료형* 포인터명 = (자료형*)malloc(sizeof(자료형) * 길이);
		(int*)malloc(sizeof(int) * 5);
		
	calloc(clear Allocation) : 할당된 메모리에 기본값으로 초기화한다.
		자료형* 포인터명 = (자료형*)calloc(길이, sizeof(자료형));
		(int*)calloc(5, sizeof(int));	
		
	realloc(resize Allocation) : 동적 메모리 사이즈를 변경한다.
		포인터명 = (자료형*)realloc(포인터명, sizeof(자료형)*길이);
		(int*)realloc(dAr, sizeof(int) * 8);

	free : 동적 메모리 해제
		free(포인터명);
		메모리를 해제하지 않으면 프로그램이 종료될때까지 사라지지 않고 남아있기 때문에
		꼭 반드시 free함수로 메모리 해제를 해줘야 한다.
	