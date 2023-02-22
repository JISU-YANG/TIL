JAVA 40 LEVEL
# Lv.37 OOP

> JAVA에서는 보통 객체지향 프로그래밍(Object-Oriented Programming)을 하며 C의 절차지향 프로그래밍과 자주 대조된다.

세상의 모든 것을 객체(Object)로 보고 구현을 한다.

### 객체지향(OOP)의 3가지 특징
  - 은닉화(Encapsulation)
    - Member Field를 Private으로 선언(데이터 은닉화)
    - get(), set()을 사용한다.
  - 계층구조(Inheritance)
    - 인터페이스는 계층구조로 생각하지 않는다.
    - 계층구조 관계에서만 Override할 수 있다.
    - Override 할 수 없는 조건
       - Final
       - 부모의 생성자
       - Private
       - Static
  - 다형성(Polymorhism)
    - 캐스팅(casting)을 통해 다양한 형태(type)을 지닐 수 있다.
    - 다형성 발생 원리 3단계
      - 상위 클래스의 이름으로 하위 클래스를 생성한다.
    (다른 하위 클래스 타입으로 다운 캐스팅할 경우 ClassCastException이 발생한다.)
      - 상위 클래스 타입으로 하위 클래스를 참조한다.
      - 상위 클래스의 메소드로 자식의 메소드를 실행한다.
    (추상 메소드의 Override, VMI)