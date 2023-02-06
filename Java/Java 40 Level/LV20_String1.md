## JAVA 40 LEVEL
# Lv.20 String 1

Web에서 받는 텍스트들이 String 타입으로 받아오기 때문에 예외가 많은 클래스인 String을 잘 다룰줄 알아야한다.



### 중요 요소
1. String 클래스의 메서드
2. 문자열 분리
3. 문자열 비교
4. 객체 비교


### 특징
java.lang.String에 속해있으며 다른 클래스에서 extends할 수 없다.
인스턴스화 (new 예약어를 이용한 호출)을 하지 않아도 인스턴스가 생성된다.
문자열이 합쳐질때 Concatenation이 발생한다.
문자형이 조합된 형태이다.

### 선언방법
```java
// 예시 A
String s1 = "예시A";

// 예시 B
String s2 = new String("예시B");
 ```

꼭 인스턴스화를 거치지 않아도 되는 이유는 래퍼 클래스(Wrapper Class)들은 오토 박싱/언박싱(Auto Boxing/Unboxing)해서 값을 가져가기 때문이다. 하지만 String은 예외로 다른 고유 영역에 보관된다.

특징은 immutable한 기본타입이지만 성질은 mutable한 참조타입을 따른다.

### Concatenate
문자열과 Object를 연산 후 보이는 그대로 문자열로 만들어준다. ('+' 연산자에서만 작동하고 문자열을 만난 순간 일어난다.)

