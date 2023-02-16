JAVA 40 LEVEL
# Lv.28 Array

### 특징
- 하나의 변수명이다.
- index를 통해 값을 가지고 있다.
- 선언된 1개의 타입만 입력할 수 있다.
- 클래스가 존재하지 않는다.
- java.util.Arrays를 이용하면 배열에 기능을 추가해 사용할 수 있다.
- 선언된 객체는 공간을 갖지만 타입에 따라 초기 값이 달라진다.

### 예외
- 다양한 타입을 입력하고 싶으면 Object 타입을 이용한다. 하지만 명시적으로 알 수 없기 때문에 Generic이 JDK 1.5부터 추가되었다.
- 범위가 벗어난 index를 호출하면 indexOutBoundaryException이 발생한다.

### 선언
```java
class ex(){
    // 공간과 값을 선언
    int []  num1 = {1, 2, 3};

    // 공간만 선언
    int [] num2 = new int[3];

    // 인스턴스화
    int [] num3 = new int[]{1,2,3};
}
```
