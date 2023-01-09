[ch04 문자열과 함수] - [section16 함수 심화]

01. 함수 호출시 배열 전달
	void readArray(int ????){
		// 실행구문
	}
	void main(){
		int arr[] = {1, 2, 3};
		readArray(arr);
	}
	- 배열의 이름은 포인터 변수이므로 함수에서는 *arr 로 매개변수를 구현 해야 한다.
	
02. 인수 전달 방식
	1. Call-by-?????(값에 의한 전달)
	void addNum(int num) {
		num += 10;
		return num;
	}
	void main(){
		int num = 10;
		num = addNum(num);
		printf("%d", num);
	}
	- 전달되는 값이 함수 내의 매개변수에 복사되는 방식이다.
	- 따라서 함수 호출시 인자와 함수내의 매개변수는 별개로 서로 영향을 주지 않는다.

	2. Call-by-reference(?????에 의한 전달)
	void addNum(int* num) {
		*num += 10;
	}
	
	void main(){
		int num = 10;
		addNum(&num);
		printf("%d", num);
	}
	
	- 인수로 해당 변수의 주소값을 전달한다.
	- 인수로 전달된 변수의 값을 함수 내에서 변경할 수 있게 된다.
	
03. 재귀 호출 함수(recursive call)
	- 함수 내부에서 함수가 자기 자신을 또다시 호출하는 것이다.
	- 무한 반복이 될 수 있으므로 재귀호출이 중단되는 명령문이 있어야 한다.
	- 복잡한 문제를 매우 간단하게 논리적으로 해결 할 수 있다.
	
	[실행코드]
	// count 가 3이되면 종료
	void sayHello(int count) {
		// 실행구문
		printf("hello\n");
		
		// 종료조건(종료 조건이 없으면 무한 루프가 발생한다.)
		if (count != 3) {
			sayHello(count + 1);
		}
	}
	
	void main(){
		sayHello(3);
	}
	
==============================================================================

[ch04 문자열과 함수] - [section16 함수 심화]

01. 함수 호출시 배열 전달
	void readArray(int *arr){
		// 실행구문
	}
	void main(){
		int arr[] = {1, 2, 3};
		readArray(arr);
	}
	
	- 배열의 이름은 포인터 변수이므로 함수에서는 *arr 로 매개변수를 구현 해야 한다.
	
02. 인수 전달 방식
	1. Call-by-value(값에 의한 전달)
	void addNum(int num) {
		num += 10;
		return num;
	}
	void main(){
		int num = 10;
		num = addNum(num);
		printf("%d", num);
	}

	- 전달되는 값이 함수 내의 매개변수에 복사되는 방식이다.
	- 따라서 함수 호출시 인자와 함수내의 매개변수는 별개로 서로 영향을 주지 않는다.

	2. Call-by-reference(주솟값 참조에 의한 전달)
	void addNum(int* num) {
		*num += 10;
	}
	
	void main(){
		int num = 10;
		addNum(&num);
		printf("%d", num);
	}
	
	- 인수로 해당 변수의 주소값을 전달한다.
	- 인수로 전달된 변수의 값을 함수 내에서 변경할 수 있게 된다.
	
03. 재귀 호출 함수(recursive call)
	
	- 함수 내부에서 함수가 자기 자신을 또다시 호출하는 것이다.
	- 무한 반복이 될 수 있으므로 재귀호출이 중단되는 명령문이 있어야 한다.
	- 복잡한 문제를 매우 간단하게 논리적으로 해결 할 수 있다.
	
	[실행코드]
	// count 가 3이되면 종료
	void sayHello(int count) {
		// 실행구문
		printf("hello\n");
		
		// 종료조건(종료 조건이 없으면 무한 루프가 발생한다.)
		if (count != 3) {
			sayHello(count + 1);
		}
	}
	
	void main(){
		sayHello(3);
	}
		