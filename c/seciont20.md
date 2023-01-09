[ch05 메모리 관리와 구조체] - [section20 구조체의 응용]

01. 구조체와 ???
	보통 구조체는 멤버 변수가 여러 개 이므로 사이즈가 큰 편이다. 
	그래서 구조체 변수를 일일이 선언해서 사용하는 것보다는 포인터 변수로 사용하는 편이 효율적이다.

	Person boy;
    Person * ptr = &boy;
	
	(*ptr).name == ?????;
	
02. 구조체의 ??
	typedef struct{
		Book book; 			// 멤버 변수로 구조체 변수 선언
		char color[20];
	}Bag;
	
	구조체의 멤버로 ???를 사용할 수 있다.
	
03. 구조체와 ??
	
	1. call by ???
	Student s = {100, 21};
	printStudent(s);
	
	- 구조체 변수를 함수의 인자로 전달하고 반환할 수 있다.
	- 구조체 변수의 값이 매개 변수에 통째로 복사된다.
	
	2. call by ???
	Student s = {100, 21};
	printStudent(&s);
	
	- 구조체 변수가 저장된 주솟값을 인자로 전달한다.


================================================

[ch05 메모리 관리와 구조체] - [section20 구조체의 응용]

01. 구조체와 포인터
	보통 구조체는 멤버 변수가 여러 개 이므로 사이즈가 큰 편이다. 
	그래서 구조체 변수를 일일이 선언해서 사용하는 것보다는 포인터 변수로 사용하는 편이 효율적이다.

	Person boy;
    Person * ptr = &boy;
	
	(*ptr).name == ptr->name
	
02. 구조체의 중첩
	typedef struct{
		Book book; 			// 멤버 변수로 구조체 변수 선언
		char color[20];
	}Bag;
	
	구조체의 멤버로 구조체를 사용할 수 있다.
	
03. 구조체와 함수
	
	1. call by value
	Student s = {100, 21};
	printStudent(s);
	
	- 구조체 변수를 함수의 인자로 전달하고 반환할 수 있다.
	- 구조체 변수의 값이 매개 변수에 통째로 복사된다.
	
	2. call by ref
	Student s = {100, 21};
	printStudent(&s);
	
	- 구조체 변수가 저장된 주솟값을 인자로 전달한다.