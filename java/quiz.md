# 퀴즈 ch01 ~ ch03

1. 2010년 썬마이크로시스템즈로부터 자바를 인수한 회사는?

2. 환경변수 설정을 하는 이유는 컴퓨터의 어떤 경로에서든 운영체제가 자바를 ??하도록 하는 것이다.

3. 자바의 변수명명 규칙 주로 ?? 표기법(예시:userName)을 따른다.

4. 자바의 기본 데이터 타입은 정수형, ??형, 논리형, 문자형 이다.

5. byte 데이터 타입의 저장 가능한 값의 범위는 -128 ~ ??? 이다.

6. 증감연산자에서 마지막 sum의 값은 얼마인가?
```java
int sum = 10;
int a = 10;
sum += a++;
```

7. 콘솔에 어떤 문자가 출력 되나요?
if( false && true) {
	System.out.println("true");
} else {
	System.out.println("false");
}

8. 십진수 5를 이진수로 나타내 보세요.
 

# 퀴즈 ch06 ~ ch08 객체지향

1. 객체 지향 언어의 장점이 아닌 것은?
	- 코드의 재사용성
	- 코드의 실행 속도 향상
	- 신뢰성 높은 프로그래밍
	- 코드 관리의 편리함
 
2. 메서드의 리턴값이 없을 경우 리턴타입은 무엇인가요?

3.  getArea(int a){} 메소드를 OverLoading 한 메소드를 하나만 만들어 보세요.

4. class A{} 클래스의 기본 생성자를 만드세요.

5. 접근제어자의 접근 범위가 큰 것 부터 나열 하세요.

6. 클래스 A는 추상 클래스 입니다. 클래스 A를 완성 하세요. 단, 클래스 A의 메소드와 변수 이름은 임의로 정해도 됩니다.

7. 인터페이스 A 를 구현하는 B 클래스를 완성하세요. 단, 인터페이스 A는 go() 라는 추상 메소드를 포함하고 있습니다. 

8. Parent 클래스를 상속해서 Child 클래스를 다음과 같이 작성했습니다. 컴파일 에러가 발생하지 않도록 수정해 보세요.
```java
public class Parent {
	public String name;

	public Parent(String name){
		this.name = name;
	}
}

public class Child extends Parent {
	private int stdNo;

	public Child(String name, int stdNo){
		this.name = name;
		this.stdNo = stdNo;
	}
}
```

9. 다음은 Soundable 인터페이스 입니다. sound() 추상 메소드는 객체의 소리를 리턴 합니다. 아래와 같이 Cat과 Dog 객체를 주고 실행했을 때 "야옹" "멍멍"이 출력되도록 Cat과 Dog 클래스를 작성해 보세요.
``` java
public interface Soundable {
	String sound();
}

public class SoundableExample {
	private static void printSound(Soundable s) {
		System.out.println(s.sound());
	}
	
	public static void main(String[] args) {
		printSound(new Cat());
		printSound(new Dog());
	}
}

public class Cat implements Soundable {
	public String sound(){
		return "야옹";
	}
}

public class Dog {

}
```


