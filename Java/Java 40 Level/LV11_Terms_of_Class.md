```java
// 패키지 라인
// 1. 소문자로 작성 2. 문단의 가장 첫 라인
package noly.poly;
// ---

// import 영역
// ---

// {} == 중괄호 == Block == Body == 
// 논리적인 로직이 들어있는 영역
public Class Feature_Explain{
// Member Field (Member == 나의 것)
    
    // Member Variable
    private int a; // 멤버 변수를 선언 (인스턴스화할 때에 타입에 맞는 기본 값이 대입된다.)
    private static float f = 3.14f; // 멤버 변수를 (직접) 초기화 + Static Variable
    public String str = "홍길동"; // Instance Variable (인스턴스를 통해 접근 가능하기 때문)

    // A a = new A();
    // 선언 = 인스턴스화;
    // 참조형 타입의 기본 값은 null(주소가 없는 상태를 타내는 예약어)이다.
    
    // 생성자의 접근제한자가 private이면 외부에서 접근이 불가능하다. 주로 싱글톤 패턴에서 볼 수 있다.
    public Feature_Explain(){

    }

    // Member Method
    private void make(int param) { // 외부에서 아규먼트가 파라미터 변수에 바인딩된다.
    int a = 10; // 메서드 안에 있는 변수는 지역변수(Local Variable)
    // 메서드 안에서 변수의 우선순위
    // 1. 지역변수 2. 맴버필드(this 예약어로 변경가능)
    // 위치에 따라 우선순위가 변경되므로 호출시 주의
    this.a = 100;

    // int i = 0; 신텍스를 벗어나 로컬변수로 사용할 수도 있다.
    for(int i = 0; i < 10 i++){
        System.out.println(this.a);
    }


    }
}

```