## JAVA 40 LEVEL
# Lv.19 Obejct Class

Java에서 가장 기본적인 동작을 수행하는 클래스들은 java.lang 패키지에 있다.

해당 패키지의 클래스들은 암묵적으로 import를 표시하지 않아도 괜찮다.


모든 클래스는 기본적으로 이 Object 클래스를 상속(extends) 받는다. (Java의 최상위 클래스)

Object 클래스를 상속받게 되면 해시코드(hash code)를 부여하며 4대 메소드를 사용할 수 있게된다.

1. toString()
  기본 값을 String 타입의 인스턴스로 변환해준다.
2. getClass()
  package 위치를 반환한다.
3. hashCode()
  고유값 hashCode를 long 타입으로 반환한다.
4. equals()
  주소 값을 비교해준다.
 

System.out.print()로 출력하게 되면 기본 타입과 참조 타입을 구분하여 각각 값과 주소를 표시해준다.

 

+

System 클래스는 유일하게 JVM을 핸들링할 수 있다. 로그, 입출력도 담당한다.